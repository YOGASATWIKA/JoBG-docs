---
tags: [keputusan]
status: diterima
tanggal: 2026-11-21
---
# ADR-001: Struktur Repository

## Konteks
JoBG terdiri dari bagian untuk pengguna (Portal Kandidat, Dashboard HR) dan bagian inti (Inti JoBG, Asisten AI, Pintu MCP). Rencana awal adalah satu repository (monorepo).

## Pilihan yang dipertimbangkan
1. Satu repository untuk semua (monorepo)
2. **Tiga repository: backend, frontend, dan dokumen**

## Keputusan
Pilihan 2:
- **JoBG-BE**: Inti JoBG, Asisten AI internal, Pintu MCP, Penjaga Akses
- **JoBG-FE**: Portal Kandidat & Dashboard HR
- **JoBG-docs**: seluruh dokumen perencanaan (folder induk `job-portal/`)
- **Pintu MCP berada di backend**, sesuai prinsip "satu otak, banyak pintu" di [[Gambaran Sistem]].

Struktur lokal:
```
job-portal/         ← github.com/YOGASATWIKA/JoBG-docs
├── docs/           ← dokumen perencanaan
└── apps/
    ├── JoBG-BE/    ← github.com/YOGASATWIKA/JoBG-BE
    └── JoBG-FE/    ← github.com/YOGASATWIKA/JoBG-FE
```

## Konsekuensi
- ➕ Setiap repository lebih fokus & mudah dipamerkan terpisah di portofolio.
- ➖ Perubahan yang menyentuh BE & FE harus dikoordinasikan di dua tempat.
- ➕ Dokumen perencanaan bisa dipamerkan sebagai bagian portofolio.
