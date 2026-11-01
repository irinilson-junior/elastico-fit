# Elástico Fit: como publicar na Vercel

Esta pasta já é o site completo. Não precisa instalar nem compilar nada.

Arquivos: `index.html` (o app), `sw.js` (modo offline), `manifest.webmanifest` (nome e ícone do app), `vercel.json` e a pasta `icons`.

## Caminho 1: GitHub + painel da Vercel (sem terminal)

1. Crie uma conta em github.com e um repositório novo, por exemplo `elastico-fit`.
2. No repositório, clique em **Add file > Upload files**, arraste TODO o conteúdo desta pasta (incluindo a pasta `icons`) e clique em **Commit changes**.
3. Entre em vercel.com com a conta do GitHub, clique em **Add New > Project** e importe o repositório.
4. Em **Framework Preset**, deixe **Other**. Não preencha Build Command nem Output Directory. Clique em **Deploy**.
5. Em cerca de um minuto a Vercel mostra o endereço, algo como `elastico-fit.vercel.app`.

## Caminho 2: terminal (Vercel CLI)

1. Instale o Node.js (nodejs.org).
2. No terminal: `npm i -g vercel`
3. Entre na pasta do app (`cd elastico-fit-pwa`) e rode `vercel`. Faça o login e aceite as perguntas padrão.
4. Para publicar de verdade: `vercel --prod`

## Instalar no celular

- **Android (Chrome):** abra o endereço, toque no menu de três pontos e em **Instalar app**.
- **iPhone (Safari):** abra o endereço, toque em **Compartilhar** e em **Adicionar à Tela de Início**.

## Atualizar o app depois

1. Troque os arquivos (no GitHub, pelo Upload files, ou rodando `vercel --prod`).
2. Abra `sw.js` e aumente o número em `CACHE` (de `elastico-fit-v1` para `elastico-fit-v2`). Sem isso, quem já instalou continua vendo a versão antiga.

## Bom saber

- O histórico de treinos fica salvo no navegador de cada aparelho. Em outro celular ele começa vazio.
- Os vídeos abrem buscas no YouTube e precisam de internet. O resto do app funciona offline depois da primeira visita.
- A Vercel dá um endereço gratuito `.vercel.app`. Domínio próprio é opcional, em Settings > Domains.
