# Projeto de Gerenciamento de Locações

## Objetivo
Visando solucionar um problema relatado por uma pessoa do meu convívio particular, esta aplicação tem como intuito auxiliar locadores e locatários ao controlar seus imóveis e fornecer para ambas as partes informações simples, claras e concisas.

Através deste, um locador pode cadastrar novos locatários, gerar e confirmar pagamentos (por enquanto por inserção manual), acessar as solicitações de manutenção, bem como obter o histórico de atividades.

Este projeto foi iniciado em 2021 com o objetivo pessoal de aprofundar meus conhecimentos em React.js; entretanto, mesmo tendo feito toda a aplicação backend em C#, o meu irmão (que realizou o desenvolvimento backend da aplicação) ingressou no mercado e não pudemos realizar a integração. Em contrapartida, a nova versão desta aplicação conta com recursos novos, não planejados em oportunidade anterior.

## Funcionalidades
### Administrador
O locador do imóvel pode:
- Cadastrar imóveis para aluguel em quatro categorias (casa, apartamento, ponto comercial ou conjunto habitacional);
- Adicionar locatários (cabendo aos mesmos a alteração de sua senha) no ato de vincular locação. Cabe ressaltar que o mesmo locatário pode assumir mais de uma locação;
- Visualizar informações gerais sobre cada locação, bem como o contrato firmado com o locatário;
- Editar informações de cada imóvel, bem como deletar (apenas quando TODAS AS LOCAÇÕES estiverem desocupadas);
- Visualizar as solicitações para manutenção para cada imóvel, havendo chat com o usuário e podendo encerrar tal pedido especificando o valor gasto;
- Visualizar o faturamento de todos os imóveis cadastrados, uma vez sinalizado pelo botão "Faturar" em "Propriedades". Com isso, há a listagem de inquilinos, um breve relatório sobre o imóvel e o seu faturamento, bem como o status para cada inquilino (se pagou ou não). Por enquanto, o locador precisa informar manualmente se foi pago, assim como pode mudar a forma de pagamento;
- Acessar os registros realizados para cada imóvel, filtrado pela categoria (usuário, imóvel, manutenção, faturamento, contrato e locação) e pelo mês de registro.

### Locatário
O locatário pode:
- Visualizar as informações gerais sobre o imóvel alugado (como endereço e status de pagamento);
- Gerar uma solicitação para manutenção, acessar cada registro aberto em seu usuário, bem como conversar por chat em tempo real com o proprietário;
- Visualizar os débitos e o histórico de pagamentos em meses anteriores.

### Ambos
Todos os perfis levantados acima possuem funcionalidades em comum. São elas:
- Alterar seus dados cadastrais (limitado a telefone);
- Redefinir senha (é enviado um código para o e-mail cadastrado, temporariamente em um e-mail pessoal).

## Recursos utilizados
### Frontend
Utilizamos:
- React.js com Typescript
- Material UI
- Socket.io-client (para comunicação realtime no chat de manutenção)
- Moment
- Axios (integração com backend)
- Redux (gerenciamento de estado)
- React iMask (máscara para inputs específicos, como CPF, telefone e CEP)
- React Countup (efeito de counter para valores no Dashboard)
- React Chartjs 2 (gráficos)

### Backend
Utilizamos:
- ExpressJS com Typescript
- Knex.js (typeORM baseado em PostgreSQL)
- Moment
- Nodemailer (para envio de informações para redefinição de senha)
- Socket.io (cria comunicação para recursos realtime, como chat)
- Passport (credenciais para login)
- Bcrypt (criptografia de senha)
- Body Parser
- Consign
- Cors

## Resultado final
### Dashboard
![Dashboard](/assets/Dashboard.gif)

### Faturamento
![Faturamento](/assets/Faturamento.gif)

### Propriedades
![Propriedades](/assets/Propriedades.gif)

### Logs
![Logs](/assets/Logs.gif)

### Tela de usuário
![Tela_usuario](/assets/Usuario%20-%20Tela%20Inicial.gif)

## Pontos de melhoria
- Há a intenção de expandir as mensagens de e-mail para novas mensagens de manutenção;
- Planos para utilizar e-mail profissional (atualmente estou utilizando um endereço eletrônico pessoal);
- Expansão da aplicação a nível comercial (planos freemium).

## Agradecimentos
- Matheus Lara, Prudente e Wegner (colegas de trabalho) pelo esclarecimento de dúvidas pontuais;
- Peterson Azevedo, Caio Itallo e desenvolvedores anônimos do r/brdev (comunidade no Reddit), pelas sugestões sobre o deploy da aplicação;
- Mateus Souza, pela assistência em assuntos cuja lógica foi mais complicada;
- Beatriz Chiarelli, pelas "críticas destrutivas" na parte de estilização do portal web;
- Stackoverflow, por tudo 😂

"# projeto-aluguel-2.0-overview" 
