## Framework
- Gunakan Next.js (App Router) + TypeScript.
 
## Database
- Lokal: SQLite.
- Server (Vercel): PostgreSQL (Supabase).
- URL koneksi hanya lewat DATABASE_URL.
- Beda provider: ubah provider di schema,
  lalu buat ulang migrasi.

## ORM
- Gunakan Prisma, schema-first:
  ubah skema dulu, lalu migrasi.
- Satu db/schema.prisma untuk semua fitur;
  agent menormalisasi tabel sendiri.
 
## Struktur
- Folder per fitur: product/<fitur>/
  dan modules/<fitur>/.
 
## Standar
- Tailwind CSS, Zod, ESLint + Prettier.
- Auth: JWT di cookie httpOnly.
- Rahasia hanya di .env.