# 📘 01. Introduction to Next.js

---

## 🧠 What is Next.js?

**Next.js** is a powerful React framework for building full-stack web applications.

> ✅ Built by Vercel, it enables server-side rendering (SSR), static site generation (SSG), routing, API routes, and much more out-of-the-box.

### 🔧 Features:
- File-based routing
- Server-side rendering (SSR)
- Static site generation (SSG)
- Built-in API routes
- Image optimization
- Middleware and Edge functions
- TypeScript & Tailwind support

---

## ⚔️ Next.js vs React vs CRA

| Feature              | React (CRA)        | Next.js            |
|----------------------|--------------------|---------------------|
| Routing              | Manual (React Router) | Built-in (File-based) |
| SSR / SSG            | ❌ Not supported    | ✅ Supported         |
| API Routes           | ❌ Not included     | ✅ Built-in backend  |
| SEO Optimization     | ❌ Hard to manage   | ✅ Built-in via SSR  |
| Performance          | Depends on setup   | Optimized by default|
| Deployment           | Manual              | Vercel-ready        |

> CRA (Create React App) is ideal for SPAs. Next.js is better for scalable, SEO-optimized apps.

---

## 🔄 CSR vs SSR vs SSG vs ISR

| Rendering Type | Description | When to Use |
|----------------|-------------|-------------|
| **CSR** (Client-Side Rendering) | Content rendered in browser using JS | Dashboards, Authenticated apps |
| **SSR** (Server-Side Rendering) | Content rendered on server at request | Dynamic content, SEO pages |
| **SSG** (Static Site Generation) | HTML pre-rendered at build time | Blogs, Docs, Landing pages |
| **ISR** (Incremental Static Regeneration) | SSG + revalidates stale pages in background | Content that updates regularly |

---

## 🎯 When and Why to Use Next.js?

✅ Use Next.js when:
- You want fast, SEO-friendly pages (e.g., blogs, e-commerce)
- You need SSR/SSG out-of-the-box
- You want full control (routing, data fetching, APIs) in one framework
- You’re building scalable production-ready React apps

🚫 Don’t use Next.js if:
- You only need a small SPA with no routing/SEO concerns
- You want full manual control of the build setup (then use CRA + Vite)

---

## ✅ Summary

| Concept         | Description                                                  |
|------------------|--------------------------------------------------------------|
| What is Next.js  | React framework with built-in SSR, routing, APIs             |
| CRA vs Next.js   | CRA is SPA-only, Next.js is full-featured & production-ready |
| Rendering Modes  | CSR, SSR, SSG, ISR — based on page needs                     |
| When to Use      | SEO, performance, scalability, hybrid static/dynamic apps    |

