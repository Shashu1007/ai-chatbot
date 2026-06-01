<div align="center">

# 💬 ai-chatbot — Production-Ready AI Chat Platform

**A Next.js 14 + Vercel AI SDK chatbot with streaming responses, persistent chat history, and a polished shadcn/ui interface.**

[![Live Demo](https://img.shields.io/badge/Live_Demo-00C7B7?style=for-the-badge&logo=vercel&logoColor=white)](https://ai-chatbot-ruby-iota.vercel.app/)
[![Next.js](https://img.shields.io/badge/Next.js_14-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)](https://nextjs.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![AI SDK](https://img.shields.io/badge/Vercel_AI_SDK-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://sdk.vercel.ai)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

</div>

---

## 🚀 Live Demo

**Try it now → [ai-chatbot-ruby-iota.vercel.app](https://ai-chatbot-ruby-iota.vercel.app/)**

> _Add a screenshot or GIF here once you have one — save it to `docs/screenshots/demo.gif` and reference `![Demo](docs/screenshots/demo.gif)`_

---

## ✨ Features

- 🧠 **Multi-model support** — xAI Grok (default), OpenAI, Anthropic, Fireworks, Cohere — switch in one line
- ⚡ **Streaming responses** with React Server Components & Server Actions
- 💾 **Persistent chat history** powered by Neon Serverless Postgres
- 📎 **File attachments** stored on Vercel Blob
- 🔐 **Auth.js authentication** — email + OAuth providers
- 🎨 **shadcn/ui + Tailwind CSS** — accessible, themeable Radix primitives
- 🧪 **Playwright e2e tests** ready to wire into CI
- 🏗️ **App Router architecture** with route-based code splitting

---

## 🧰 Tech Stack

| Layer            | Tools                                                    |
| ---------------- | -------------------------------------------------------- |
| **Framework**    | Next.js 14 (App Router), React 19, TypeScript            |
| **AI**           | Vercel AI SDK, xAI / OpenAI / Anthropic providers        |
| **UI**           | Tailwind CSS, shadcn/ui, Radix UI                        |
| **Database**     | Neon Postgres + Drizzle ORM                              |
| **Storage**      | Vercel Blob (file uploads)                               |
| **Auth**         | Auth.js (NextAuth v5)                                    |
| **Tooling**      | pnpm, Biome (lint/format), Playwright (e2e)              |
| **Deployment**   | Vercel                                                   |

---

## 🏁 Quick Start

### Prerequisites
- Node.js **18+**
- `pnpm` (`npm i -g pnpm`)
- A free Vercel account (for env pull) or your own `.env`

### 1 · Clone & install
```bash
git clone https://github.com/Shashu1007/ai-chatbot.git
cd ai-chatbot
pnpm install
```

### 2 · Configure environment
Copy `.env.example` → `.env.local` and fill in:

```env
# AI provider (choose one)
XAI_API_KEY=...
# OPENAI_API_KEY=...
# ANTHROPIC_API_KEY=...

# Auth
AUTH_SECRET=...                # openssl rand -base64 32

# Database
POSTGRES_URL=postgres://...    # from Neon / Vercel Postgres

# File storage
BLOB_READ_WRITE_TOKEN=...      # from Vercel Blob
```

> 💡 **Easier path:** `pnpm dlx vercel link && pnpm dlx vercel env pull` — pulls all secrets straight from your Vercel project.

### 3 · Run
```bash
pnpm dev
```
Visit **http://localhost:3000**. 🎉

### 4 · Deploy to Vercel
```bash
pnpm dlx vercel
```

---

## 🧪 Testing

```bash
pnpm test             # Playwright e2e suite
pnpm lint             # Biome lint + format check
pnpm build            # Production build
```

---

## 📁 Project Structure

```
ai-chatbot/
├── app/                  # Next.js App Router pages & layouts
├── components/           # Reusable React components (chat UI, sidebar, etc.)
├── lib/                  # AI helpers, db client, auth config
├── hooks/                # Custom React hooks
├── artifacts/            # Generated artifacts (canvas, code, sheet)
├── public/               # Static assets
├── tests/                # Playwright e2e tests
├── drizzle.config.ts     # Drizzle ORM config
├── middleware.ts         # Auth + routing middleware
└── next.config.ts
```

---

## 🔄 Switching AI Providers

Edit `lib/ai/models.ts`:

```ts
import { openai } from '@ai-sdk/openai';
// import { anthropic } from '@ai-sdk/anthropic';

export const chatModel = openai('gpt-4o-mini');
```

That’s it — the rest of the app is provider-agnostic thanks to the AI SDK.

---

## 🗺️ Roadmap

- [ ] Voice input (Whisper) & TTS output
- [ ] Multi-modal: image + PDF understanding
- [ ] Per-conversation system prompts (“Personas”)
- [ ] Cost dashboard with token analytics
- [ ] Shareable read-only chat links

---

## 🤝 Contributing

PRs welcome! Please:
1. Fork the repo & create a feature branch
2. Run `pnpm lint && pnpm test`
3. Open a PR with a clear description + screenshot

---

## 📄 License

Released under the [MIT License](LICENSE).

---

<div align="center">

**Built by [Shashank R](https://github.com/Shashu1007)**
🐙 [GitHub](https://github.com/Shashu1007) · 💼 [LinkedIn](https://linkedin.com/in/shashank1007) · 📧 sshashu777@gmail.com

⭐ _If this saved you a weekend, a star would mean a lot._

</div>
