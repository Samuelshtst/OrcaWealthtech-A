# AGENTS.md: struktur proyek
 
## Struktur
- Kelompokkan fitur per folder  (contoh: auth, payment).
- Nama folder product/<fitur>/ HARUS sama dengan modules/<fitur>/.
 
## Konteks umum (baca dulu)
- product/_general/prd.md
- product/_general/brand-guideline.md
- product/_general/tech-stack.md

## Konteks fitur: product/auth/
- us1-register.md (user story)
- uf1-register.md (user flow)
- wf1-register.md (wireframe)
- mo1-register.png (mockup)
- dt1-register.md (data)
 
## Output
- Tulis kode di modules/<fitur>/, sesuai struktur product/.
- Baca semua dokumen fitur sebelum menulis kode.

## Database (schema-first)
- Satu db/schema.prisma untuk SEMUA fitur. Jangan membuat skema per fitur.
- Baca semua product/*/dt*.md.
- Atur sendiri tabel dan relasinya:
  normalisasi (hindari data ganda),
  tentukan kunci utama dan kunci asing.
- Tambahkan kolom teknis yang perlu (passwordHash, createdAt).

## Setelah skema berubah
- Jalankan: npx prisma migrate dev --name <deskripsi-singkat>
- Jangan edit migrasi yang sudah jalan.
- Laporkan tabel yang dibuat atau diubah.
 
## Batasan
- Jangan ubah tabel yang dipakai fitur lain tanpa menyebut alasannya.
