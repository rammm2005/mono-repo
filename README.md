# Monorepo

![pnpm](https://img.shields.io/badge/pnpm-workspaces-yellow?style=flat-square&logo=pnpm)
![TypeScript](https://img.shields.io/badge/TypeScript-blue?style=flat-square&logo=typescript)
![Next.js](https://img.shields.io/badge/Next.js-black?style=flat-square&logo=next.js)
![PayloadCMS](https://img.shields.io/badge/Payload-Backend-red?style=flat-square&logo=payloadcms)

> Monorepo ini berisi aplikasi **web publik** dan **admin dashboard**, beserta **paket bersama** seperti UI components, konfigurasi, dan utilitas. Dengan struktur ini, pengembangan lintas platform menjadi lebih terorganisir dan efisien.

---

## 📁 Struktur Direktori

```
travel-monorepo/
├── apps/
│ ├── web/ # Frontend website (Next.js)
│ └── admin/ # Admin dashboard (Payload CMS)
├── packages/
│ ├── ui/ # Shared UI components (React + ShadCN UI)
│ ├── config/ # Shared konfigurasi (env, tailwind, dsb)
│ └── utils/ # Fungsi-fungsi bersama
├── .gitignore
├── package.json
└── README.md

```

## 🚀 Tech Stack

- **Frontend Web:** Next.js, TypeScript, Styled Components, ShadCN UI, Tanstack React Query
- **Mobile App:** Android (Kotlin, MVVM)
- **Backend:** Payload CMS (Node.js, Express), PostgreSQL, Redis
- **Monorepo:** pnpm, TypeScript project references

## 🛠 Instalasi

### 1. Clone Repository

```bash
git clone https://github.com/rammm2005/mono-repo.git
cd monorepo
```

#### Install Dependencies

```
pnpm install
```

#### Setup Envoriment Variable

Buat file .env di root dan di masing-masing app (apps/web/.env, apps/backend/.env, dll). Contoh:

```
# apps/backend/.env
DATABASE_URL=postgres://user:pass@localhost:5432/travel
PAYLOAD_SECRET=secret123
REDIS_URL=redis://localhost:6379

```

```
# apps/web/.env
NEXT_PUBLIC_API_URL=http://localhost:3001/api

```

#### 📦 Scripts

Semua perintah dijalankan dari root monorepo menggunakan pnpm.

```
# Jalankan web app
pnpm --filter web dev

# Jalankan backend Payload CMS
pnpm --filter backend dev

# Build semua project
pnpm build

# Jalankan lint di semua apps
pnpm lint
```

### 🧪 Unit Testing

```
pnpm test

```

## 🧑‍💻 Kontributor

    I Putu Rama Dita – @rama – Developer, Designer
