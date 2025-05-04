# trabalho_furia

Chat Web - TEAM FURIA


📌 Visão Geral
Bem-vindo ao TEAM FURIA Chat, um sistema de bate-papo interativo em tempo real!
🚀 Tecnologias Utilizadas
•	Node.js e Express
•	WebSockets com Socket.io
•	dotenv para gerenciamento de variáveis de ambiente
🔧 Instalação
Para configurar o ambiente, siga os passos abaixo:
git clone <URL_DO_REPOSITORIO>
cd trabalho_furia
npm install





## ⚙️ Configuração do Ambiente 

Crie um arquivo .env com suas variáveis de ambiente:

PORT=3000
DB_HOST=localhost
SECRET_KEY=super_secreto

No código, carregue as variáveis:
require('dotenv').config();
const port = process.env.PORT || 3000;

## 🚀 ** Inicialização do Servidor **
Para iniciar o servidor:

node src/server.js

(Obs: dentro da JSON, use o seguinte código:) 
{
  "name": "trabalho_furia",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "start": "node src/server.js",
    "dev": "node --watch src/server.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "description": "",
  "dependencies": {
    "dotenv": "^16.5.0",
    "ws": "^8.18.1"
  }
}

Pode ativa-lo pelo console com:

cd backend 
npm run dev

O comando irá rodar automaticamente o servidor, estabelecendo uma conexão para você testar



## 🔗** WebSockets - Comunicação em Tempo Real **
Implementação do servidor com Socket.io:


const io = require('socket.io')(server);

io.on('connection', (socket) => {
    console.log('Usuário conectado:', socket.id);

    socket.on('mensagem', (msg) => {
        io.emit('mensagem', msg);
    });

    socket.on('disconnect', () => {
        console.log('Usuário desconectado:', socket.id);
    });
});


## 🛡️ Segurança e Melhores Práticas
- Uso de variáveis de ambiente para evitar exposição de dados sensíveis.
- Proteção contra ataques XSS e CSRF.
- Implementação de autenticação segura.

## 📌 Futuras Melhorias
- Adição de suporte avançado a WebSockets.
- Melhorias na experiência do usuário.
- Integração com banco de dados para histórico de mensagens.
