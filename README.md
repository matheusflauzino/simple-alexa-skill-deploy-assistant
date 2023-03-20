# Exemplo simples de Skill Alexa

<div align="center">

![Skill Assistente de Deploy](./assets/rocket-large.png)

Exemplo de desenvolvimento de uma Skill simples para Amazon Alexa.
</div>


## Descrição

Pergunte para a sua Alexa se hoje é um dia bom para o deploy do seu sistema ou microserviço. Ela irá responder, dependendo do dia e horário se você deve ou não fazer deploy. Essa skill é baseada no site https://shouldideploy.today/. Algumas respostas podem conter o idioma inglês.

Para fazer instalação da skill, basta procurar na loja da Amazon por "Assistente de Deploy", ou acessar [aqui](https://www.amazon.com.br/dp/B0BZ1GH72J/ref=sr_1_1?qid=1679342047&rnid=17938239011&s=alexa-skills&sr=1-1) e fazer a instalação.

## Desenvolvimento

A Skill, basicamente é dividia em duas partes, a lambda que realiza o processamento das ações (comandos/vocabulário de acionamento) e as ações/interações.

- Em `skill-package/interactionModels/custom/pt-BR.json` temos um "vocabulário de interações" que a sua skill vai responder conforme comandos fornecido pelo usuário;
- Em `lambda/index.js` é possível ver o processamento das interações realizadas pelos usuários. De forma bem resumida, é a ligação entre os comandos do usuário com o método que será acionado pela lambda, que vai ficar a cargo da SDK da Alexa.