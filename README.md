# Casos-de-teste

Shopping

![image](https://github.com/user-attachments/assets/98ba7795-a9e6-42fe-9cac-a3d878788fca)


## Fluxo

![image](https://github.com/user-attachments/assets/9dcbdac6-13e6-4cd4-a71a-a8568de8c530)


## User Case 1
Descrição:
Como um usuário da loja virtual, quero acessar a página de login, para visualizar claramente as opções de entrar, criar conta e redefinir senha.

Requisitos complementares
Atores:

Usuário visitante (não autenticado)

Sistema da loja virtual (frontend e backend)

Interface:

Página de login com design responsivo

Botões: “Entrar”, “Criar nova conta”, “Esqueci minha senha”

Feedback visual para ações (ex: hover, foco, mensagens de erro)

Dados:

Não exige entrada de dados nessa etapa

Deve apenas exibir caminhos para ações posteriores

Plataforma/Ambiente:

Navegador web moderno (desktop e mobile)

Framework frontend (ex: React, Vue, etc.)

Integração com backend para redirecionamento e roteamento de telas



## User Case 2

Descrição:
Como um usuário da loja virtual, quero preencher o formulário de criação de conta quando clicar no botão de “Criar nova conta” na tela de login, para registrar uma nova conta com meus dados pessoais.

Requisitos complementares

Atores:

Usuário visitante

Sistema de autenticação (serviço de backend)

Banco de dados de usuários

Interface:

Formulário com campos:

Nome completo

E-mail (único)

Senha e confirmação de senha

Validações visuais (ex: senha fraca, e-mail inválido)

Botão de submissão com feedback (carregando/sucesso/erro)

Dados:

Dados inseridos pelo usuário devem ser validados:

E-mail com formato válido e não duplicado

Senha com política mínima (ex: 8+ caracteres)

Os dados devem ser criptografados antes do armazenamento (ex: senha com bcrypt)

Plataforma/Ambiente:

Ambiente web responsivo (navegador desktop/mobile)

Backend com API REST ou GraphQL para cadastro

Banco de dados relacional ou NoSQL

Proteção contra bots (reCAPTCHA, por exemplo)


### Cenarios

Scenario: Acessar a tela de cadastro a partir da tela de login
    Given que o usuário está na tela de login da loja virtual
    When o usuário clica no link "Criar nova conta"
    Then o sistema deve redirecionar o usuário para a tela de cadastro
    And a tela deve exibir os campos "Nome completo", "E-mail", "Senha" e "Confirmar senha"
    And o botão "Cadastrar" deve estar visível e habilitado



Feature: Cadastro de nova conta

  Scenario: Realizar cadastro com dados válidos
    Given que o usuário está na tela de cadastro
    And preenche "Nome completo" com "Maria Souza"
    And preenche "E-mail" com "maria.souza@email.com"
    And preenche "Senha" com "Segura@123"
    And preenche "Confirmar senha" com "Segura@123"
    When o usuário clica no botão "Cadastrar"
    Then o sistema deve criar a conta do usuário
    And redirecionar para a área autenticada
    And exibir a mensagem "Conta criada com sucesso"

Variação do cenário:

Caso de Teste 2 – Cadastro com dados válidos
ID: CT-UC02-002

Título: Realizar cadastro com sucesso usando dados válidos

Pré-condições: Usuário na tela de cadastro

Passos:

Preencher “Nome completo” com "Maria Souza"

Preencher “E-mail” com "maria.souza@email.com"

Preencher “Senha” com "Segura@123"

Preencher “Confirmar senha” com "Segura@123"

Clicar no botão “Cadastrar”

Dados de entrada: Nome, E-mail, Senha, Confirmação de senha

Resultado esperado:

O sistema deve validar os dados

Criar o cadastro do usuário

Redirecionar para a área autenticada ou página de boas-vindas

Exibir uma mensagem como “Conta criada com sucesso!”



