# Discord Plus 2 — v0.2.0

Projeto inicial com React, Vite, Express e login OAuth2 oficial do Discord.

## Rodar localmente
1. Instale Node.js 20 ou superior.
2. Execute `npm install`.
3. Copie `.env.example` para `.env` e preencha as variáveis.
4. Configure no Discord Developer Portal o Redirect URI exatamente igual a `DISCORD_REDIRECT_URI`.
5. Execute `npm run build` e `npm start`.

## Deploy no Render
Crie um serviço Web apontando para este repositório:
- Build Command: `npm install && npm run build`
- Start Command: `npm start`
- Environment: Node
- Adicione as variáveis de ambiente do `.env.example` no painel do Render.
- Depois de obter a URL pública do Render, atualize `FRONTEND_URL` e `DISCORD_REDIRECT_URI` e cadastre o Redirect URI público no Discord Developer Portal.

Nunca envie `.env` ou Client Secret ao GitHub. Use apenas variáveis privadas da hospedagem.

O login usa apenas os escopos `identify email`. Não acessa presença, horas em chamadas, transmissões ou insígnias do Discord.
