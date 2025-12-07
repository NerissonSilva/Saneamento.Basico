# Projeto Full Stack com Login Social

Backend (Node.js + Express) e Frontend (HTML/CSS/JS) com autenticação Google OAuth.

## 🚀 Uma Única URL Pública

Frontend e backend servidos juntos em **uma única URL** no Render!

## Deploy no Render

### 1. Configurar Google OAuth

1. Acesse [Google Cloud Console](https://console.cloud.google.com/)
2. Crie um novo projeto
3. Ative a Google+ API
4. Crie credenciais OAuth 2.0
5. Adicione a URL autorizada:
   - `https://seu-app.onrender.com/api/auth/google/callback`

### 2. Deploy

1. Conecte seu repositório ao Render
2. O Render detectará automaticamente o `render.yaml`
3. Configure as variáveis de ambiente no dashboard:
   - `GOOGLE_CLIENT_ID`
   - `GOOGLE_CLIENT_SECRET`
   - `GOOGLE_CALLBACK_URL`

### 3. Atualizar Google OAuth

Após o deploy, atualize no Google Cloud Console:
- Authorized redirect URIs: `https://seu-app.onrender.com/api/auth/google/callback`

## 🛠️ Desenvolvimento Local

```bash
cd backend
npm install
# Configure as variáveis no .env
npm run dev
```

Acesse: `http://localhost:3000`

## 📦 Estrutura

```
├── backend/          # API Node.js (serve o frontend também)
│   ├── server.js     # Servidor Express
│   ├── package.json
│   └── .env
├── frontend/         # Site estático (servido pelo backend)
│   ├── index.html
│   ├── styles.css
│   └── app.js
└── render.yaml       # Configuração Render (1 serviço apenas)
```

## 🌐 Rotas

- `/` - Frontend (index.html)
- `/api` - API info
- `/api/health` - Health check
- `/api/auth/google` - Login Google
- `/api/auth/user` - Dados do usuário
- `/api/auth/logout` - Logout

## ✅ Compatibilidade

- ✅ Linux (Ubuntu, Debian, etc)
- ✅ Render.com
- ✅ Node.js 18+
- ✅ Deploy sem falhas
