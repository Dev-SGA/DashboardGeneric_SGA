# SGA — Generic Athlete Dashboard

App Next.js (Vercel) com um dashboard genérico de estatísticas individuais de atleta, pronto para ser personalizado por cliente. Tema escuro SGA, Source Sans 3 e Good Times.

## Estrutura

- **3 partidas** na mesma navegação (setas e botões). **Season** soma as três e abre os mesmos cards, com a chave **Total / Per game**.
- Card **Stats**: general passing (accurate, inaccurate e %), duelos ofensivos e defensivos e interceptações com recuperações.
- **Goals & Assists**, **Pass Results** (under / not under pressure), **Possessions** e exportação para PDF.
- Sem foto, nome ou escudo: o card do atleta mostra placeholders até você preencher os dados.

## Dados

Edite `data/gameStats.json`:

- `player.name`, `player.club`, `player.clubLogo`, `player.photo` — deixe `""` para manter os placeholders. Fotos vão em `public/player/`, escudos em `public/clubs/`.
- `matches[]` — um objeto por partida: `label` / `shortLabel`, `logo` do adversário (ou `""`), `goals`, `assists`, `passesUnderPressure`, `passResults`, `possessions`, `duels` e `videos` (label + url do clipe; url vazia esconde o link).
- `meta.session` — rótulo da sessão usado no nome do PDF exportado.

## Desenvolvimento

```bash
npm install
npm run dev
```

Abra [http://localhost:3000](http://localhost:3000).

## Deploy (Vercel)

O `vercel.json` já está configurado para Next.js — basta importar o repositório na Vercel.
