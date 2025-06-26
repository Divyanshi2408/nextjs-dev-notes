# 🔀 03. Routing in Next.js

---

## 🗂️ Two Routing Systems in Next.js

### ✅ Pages Router (`/pages`)
- Classic and still widely used
- Each file in `/pages` becomes a route
- API routes live in `/pages/api`

### ✅ App Router (`/app` - introduced in Next.js 13)
- Layout-based, component-driven structure
- Uses `page.tsx`, `layout.tsx`, `loading.tsx`, etc.
- Encourages **Server Components** by default

---

## 📁 Pages Router Basics

### 🔹 Static Routes
```
pages/
├── index.tsx → /
├── about.tsx → /about
├── contact.tsx → /contact
```
### 🔹 Dynamic Routes

Use square brackets:

```bash
pages/
├── blog/
│   ├── [slug].tsx   → /blog/my-first-post
```

Get dynamic values using useRouter:
```
import { useRouter } from 'next/router';

const BlogPost = () => {
  const router = useRouter();
  const { slug } = router.query;

  return <h1>Post: {slug}</h1>;
};
```

## 📁 App Router Basics

## 🔹 File Conventions

| File              | Purpose                                |
|-------------------|----------------------------------------|
| `page.tsx`        | Defines the route content               |
| `layout.tsx`      | Persistent layout for the route         |
| `loading.tsx`     | Loading UI for async boundaries         |
| `error.tsx`       | Route-level error boundary              |
| `not-found.tsx`   | Custom 404 for that route group         |

🔹 Example Structure
```
app/
├── dashboard/
│   ├── layout.tsx
│   ├── page.tsx          → /dashboard
├── settings/
│   ├── page.tsx          → /settings
```

## 🔗 Navigation in Both Routers
Use the <Link> component:

```
import Link from 'next/link';

<Link href="/about">Go to About</Link>
```

In App Router, use the usePathname() or useRouter() hook from next/navigation.

## 🧠 Nested Routes
Pages Router:
```
pages/
├── blog/
│   ├── [slug].tsx
App Router:
Copy
Edit
app/
├── blog/
│   ├── page.tsx
```
You can also nest layouts:

```
app/
├── dashboard/
│   ├── layout.tsx
│   └── settings/
│       └── page.tsx   → /dashboard/settings
```

## ✅ Summary

| Concept         | Description                                              |
|------------------|----------------------------------------------------------|
| Pages Router     | Classic file-based routing in `/pages`                  |
| App Router       | Modern layout-based routing in `/app`                   |
| Dynamic Routes   | Use `[param].tsx` to capture route variables            |
| Navigation       | Use `<Link>` for client-side navigation                 |
| Nested Routing   | Create folders with `page.tsx` and `layout.tsx`         |
