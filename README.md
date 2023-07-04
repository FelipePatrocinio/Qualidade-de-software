# Qualidade-de-software
Neste repositório, você encontrará um conjunto de boas práticas, ferramentas e exemplos que visam auxiliar no desenvolvimento de software com alta qualidade. Utilize-os como referência e busca contínua pela excelência na entrega de seu código.

### 1.0 - Plano de teste / Tela de cadastro

### Introdução

Exemplo: O serviço uma plataforma onde os interessados criam cadastro na plataforma, 
compram o curso desejado a partir daí conseguem acessar a plataforma onde os cursos comprados são vinculados ao seu perfil, 
podendo assim assistir e conforme vão assistindo as aulas os vídeos são marcados como assistido, 
no final de cada módulo há uma ou duas atividades para conclusão de módulo, sendo avaliada por mentores.

### Arquitetura

O framework utilizado para a implementação é baseado em um banco de dados SQL, tudo será desenvolvido em JAVA.

### Funcionalidades
- Tela de cadastro
Ao digitar nome, e-mail, número de telefone e senha e clicar no botão “Conecte-se” o 
usuário deverá ser direcionado para tela seguinte onde irá receber orientações de como 
continuar seu cadastro, deverá verificar em sua caixa de entrada no E-mail cadastrado um 
E-mail de validação da sua conta e então poderá efetuar o login normalmente a partir daí.
A senha deverá ter no mínimo 8 caracteres e deve conter letras e números.
Redirecionar o usuário para a tela seguinte com os próximos passos
Exibir a mensagem de falha em caso de usuário já cadastrado
Exibir mensagem de falha caso as senhas não coincidirem
Exibir mensagem de falha em caso algum campo estiver sem preencher.
- Tela para editar usuário
- Menu
- Página inicial
- Menu AVA

### Comportamento esperado

### Verificações
- Usuário de E-mail novo
- Usuário válido
- Senha válida
- E-mail válido
- Telefone válido.
- Login
Ao digitar Login e senha correto e clicar no botão “login” o sistema deverá redirecionar o usuário para tela inicial da plataforma.
Login do sistema com sucesso
Usuário ou senha incorreta
Por favor, preencha todos os campos em branco.
Ter acesso ao sistema.
Meus cursos
Ao acessar “meus cursos” o usuário terá acesso a todos os módulos e aulas de acordo com a liberação e poderá assistir às aulas em ordem ou não.

### Critérios de aceite

Título: Cadastro de usuário
	
	Caminho feliz
	
	CT001
	Dado que um usuário não cadastrado acesse a página de cadastro
	Quando o usuário inserir nome, Email, CPF, e senha válidos
	Então o cadastro na plataforma é realizado com sucesso
	
	Testes negativos
	
	CT002
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando o usuário inserir um email inválido
	Então o sistema exibe a seguinte mensagem de erro "Email inválido ou por favor digite um Email válido"
	
	CT003
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando o usuário inserir números no campo "nome"
	Então o sistema exibe a seguinte mensagem de erro "Campo nome inválido"
	
	CT004
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando o usuário inserir caracteres no campo "nome"
	Então o sistema exibe a seguinte mensagem de erro "Campo nome inválido"

### Estratégias de teste

Escopo do teste
O plano de teste abrange todas as funcionalidades descritas acima

Serão executados testes em todos os níveis conforme a descrição abaixo;

### Testes de integração 

Serão executados testes de integração em todos os endpoints e esses testes serão de responsabilidade do time de qualidade;
Testes automatizados: Serão realizados testes End-to-end na funcionalidade de login;

### Testes manuais

Todas as funcionalidades serão testadas manualmente pelo time de qualidade seguindo a documentação de Cenários de teste e destes Test Plan
Versão Beta: Será lançada uma versão beta para 20 usuários pré-cadastrados antes do release.
 
### Ambiente e ferramentas
Os testes serão feitos no ambiente de DEV e QA e contém as mesmas configurações do ambiente de produção com uma massa de dados gerada previamente pelo time de qualidade.

Serão utilizadas nos testes as seguintes ferramentas:

### Ferramenta

- POSTMAN
- CYPRESS
- JMETER
- ZEPHYR

### Classificação de Bugs

Os bugs serão classificados com as seguintes severidades:

### Nível de severidade

- Blocker
Bug que bloqueia o teste de uma função ou feature causa crash na aplicação
Botão não funciona impedindo o uso completo da funcionalidade
Bloqueia a entrega

- Grave
Funcionalidade não funciona como esperado
Input incomum causa efeitos irreversíveis

- Moderada
A funcionalidade não atinge certos critérios de aceitação, mas sua funcionalidade em geral não é afetada.
Mensagem de erro ou sucesso não é exibida

- Pequena
Quase nenhum impacto na funcionalidade, porém, atrapalha a experiência.
Erro ortográfico
Pequenos erros de UI.

### Definição de pronto

Será considerada pronta as funcionalidades que passarem pelas verificações e testes descritos neste "Test Plan" 
não apresentarem bugs com a severidade acima de minor, e passarem por uma validação de negócio de responsabilidade do time de produto.

### 2.0 - Cenários e casos de testes / Exemplos

Título: Cadastro de usuário
	
	Cenário positivo
	
	CT001
	Dado que um usuário não cadastrado acesse a página de cadastro
	Quando o usuário inserir nome, Email, CPF, e senha válidos
	Então o cadastro na plataforma é realizado com sucesso
	
	Cenário negativos
	
	CT002
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando o usuário inserir um email inválido
	Então o sistema exibe a seguinte mensagem de erro "Email inválido ou por favor digite um Email válido"
	
	CT003
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando o usuário inserir números no campo "nome"
	Então o sistema exibe a seguinte mensagem de erro "Campo nome inválido"
	
	CT004
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando o usuário inserir caracteres no campo "nome"
	Então o sistema exibe a seguinte mensagem de erro "Campo nome inválido"
	
	CT005
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando o usuário inserir um nome inválido
	Então o sistema exibe a seguinte mensagem de erro "nome inválido ou por favor digite um nome válido"
	
	CT006
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando o usuário inserir um CPF inválido
	Então o sistema exibe a seguinte mensagem de erro "CPF inválido ou por favor digite um CPF válido"
	
	CT007
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando o usuário inserir um Email inválido
	Então o sistema exibe a seguinte mensagem de erro "Campo Email inválido"
	
	CT008
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando o usuário inserir uma senha com menos de 8 digitos
	Então o sistema exibe a seguinte mensagem de erro "A senha deve conter no mínimo 8 digitos".
	
	CT009
	Dado que um usuáro já cadastrado acesse a página de cadastro
	Quando o usuário tentar se cadastrar novamente usando seu CPF ou email
	Então o sistema exibe a seguinte mensagem de erro "Usuário já cadastrado"
	
	CT010
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando o usuário inserir uma senha inválida
	Então o sistema exibe a seguinte mensagem de erro "senha inválida ou por favor digite uma senha válida"
	
	CT011
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando deixa de preencher o campo nome
	E tenta efetuar o cadastro
	Então o sistema exibe a seguinte mensagem de erro " Campo nome obrigatório ou por favor digite seu nome "
	
	CT012
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando deixa de preencher o campo Email
	E tenta efetuar o cadastro
	Então o sistema exibe a seguinte mensagem de erro " Campo Email obrigatório ou por favor digite seu Email "
	
	CT013
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando deixa de preencher o campo CPF
	E tenta efetuar o cadastro
	Então o sistema exibe a seguinte mensagem de erro " Campo CPF obrigatório ou por favor digite seu CPF "
	
	CT014
	Dado que um usuáro não cadastrado acesse a página de cadastro
	Quando deixa de preencher o campo Senha
	E tenta efetuar o cadastro
	Então o sistema exibe a seguinte mensagem de erro " Senha obrigatória ou por favor digite uma senha "
	
	
	Título: Login de usuários
	
	Cenário feliz
	
	CT015
	Dado que acesso a página de login
	Quando insiro minhas credenciais válidas
	Então o login é realizado com sucesso
	
	Cenário negativo
	
	CT016
	Dado que acesso a página de login
	Quando insiro um login inválido
	Então exibir uma mensagem de login inválido
	
	CT017
	Dado que acesso a página de login
	Quando tento me logar sem preencher o campo login
	Então o sistema exibe uma mensagem de "Por favor digite seu login"
	
	CT018
	Dado que acesso a página de login
	Quando insiro uma senha incorreta
	Então o sistema exibe uma mensagem de senha inválida
	
	CT019
	Dado que acesso a página de login
	Quando tento me logar sem preencher o campo senha
	Então o sistema exibe uma mensagem de "Por favor" digite sua senha"
	
	CT020
	Dado que acesso a página de login
	Quando tento me logar sem preencher o campo login e senha
	Então o sistema exibe uma mensagem de "Por favor digite seu login e senha

 ### 3.0 - Reporst Bugs / Exemplo

 	Bugs encontrados:
	
	Bug Encontrado - #BUG001.001 (Campo CPF aceitando letras) – Estado: Aberto
	Encontrado por: Felipe Patrocinio
	Produto: DesafioQA
	Local: Página de cadastro
	Versão: Ambiente produtivo no dia 16/01/2023
	Ambiente de execução: Microsoft Edge - Versão 107.0.1418.56 (Compilação oficial) (64 bits)
	Severidade: Altíssima
	Impacto: Todos os usuários estão conseguindo se cadastrar preenchendo um CPF inválido com letras
	Responsável: @Felipe.PatrocinioQAJr
	Descrição técnica: Ao acessar o Url/cadastro preencher letras no campo CPF e tentar se cadastrar o sistema está aceitando normalmente
	
	Evidência #CT001.001

 ### 4.0 - Códigos GIT que utilizo no meu dia a dia

git checkout -b feature/estoria-001 git    >  Cria a branch com o nome especificado

git pull origin develop  >  Verifica atualização

Git status > Verifica quais arquivos foram ou vão ser modificados.

Git add . > Adiciona os arquivos para a alteração.

git commit -m "Adicionar comentario sobra a modificação" > Realiza o commit com o comentario do que foi feito.

git push 
	
