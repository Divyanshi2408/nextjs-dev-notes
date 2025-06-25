# ⚙️ 02. Project Setup

---

## 🚀 Creating a New Next.js App

Use the official `create-next-app` CLI to scaffold a new project:

```bash
npx create-next-app@latest my-app
```

You’ll be prompted to select options like:

- TypeScript ✅
- App Router (recommended) ✅
- Tailwind CSS (optional)
- ESLint, src/ directory

Or use custom flags:
```
npx create-next-app@latest my-app --typescript --app --tailwind
```

## 📁 Folder Structure Overview
After setup, your project might look like this:

### ✅ App Router (/app directory - Next.js 13+)

```
my-app/
├── app/
│   ├── page.tsx
│   ├── layout.tsx
│   └── (optional folders like dashboard/, auth/, etc.)
├── public/
├── styles/
├── next.config.js
├── tailwind.config.js (if enabled)
├── tsconfig.json
```
### ✅ Pages Router (Classic /pages directory)
```
my-app/
├── pages/
│   ├── index.tsx
│   ├── about.tsx
│   └── api/
│       └── hello.ts
```
⚠️ You should choose App Router for new projects unless you need legacy support.

## 🧠 TypeScript Support
If not selected during setup:
```
touch tsconfig.json
npm install --save-dev typescript @types/react @types/node
Next.js will auto-generate a proper tsconfig.json.
```

## 🛠️ Key Config Files

- tsconfig.json: TypeScript configuration
- next.config.js: Custom Next.js behavior (e.g., redirects, images)
- .env.local: Environment variables
- tailwind.config.js: Tailwind CSS setup

## ✅ Summary

| Concept             | Description                                             |
|---------------------|---------------------------------------------------------|
| `create-next-app`   | CLI to bootstrap a new project                          |
| App Router          | Modern file-based routing with layout support           |
| Pages Router        | Legacy routing system via `/pages`                     |
| TypeScript Support  | Built-in with CLI or manual install                     |
| Config Files        | Control behavior via `tsconfig.json`, `next.config.js`, etc. |

