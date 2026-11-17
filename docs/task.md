# Task - Financial Tracking Web App

## Phase 1: Setup (1 hari)
- [x] Initialize React project dengan Vite
- [x] Konfigurasi Tailwind CSS
- [ ] Test deploy ke Vercel (free tier)
- [ ] Setup Neon PostgreSQL project
- [ ] Setup Drizzle ORM + schema transaksi
- [ ] Setup environment variables (DATABASE_URL)

## Phase 2: UI (2 hari)
- [ ] Buat halaman dashboard utama dengan ringkasan kategori
- [ ] Buat form tambah transaksi dengan dropdown kategori (dynamic per type)
- [ ] Buat halaman riwayat transaksi terfilter per kategori & type
- [ ] Buat halaman edit transaksi
- [ ] Implementasikan desain mobile-first (360px+, touch 44px, font 16px)
- [ ] Theme: Geist font, amber color untuk nominal, no Inter/no emoji

## Phase 3: Logika (3 hari)
- [ ] API routes: GET /api/transaksi, POST /api/transaksi, PATCH /api/transaksi/:id
- [ ] Integrasi Neon + Drizzle untuk CRUD transaksi
- [ ] Fungsi hitung total expense, income, balance per periode
- [ ] Fungsi filter transaksi per kategori & type & rentang tanggal
- [ ] Grafik pengeluaran per kategori (Recharts pie/bar)
- [ ] Validasi input nominal > 0, kategori sesuai type, tanggal valid

## Phase 4: Testing & Deploy (1 hari)
- [ ] Test di browser mobile (Android Chrome, iOS Safari)
- [ ] Fix responsivitas jika perlu
- [ ] Publish ke Vercel dengan URL publik
- [ ] Verifikasi Neon connection di production

## Phase 5: Documentasi (setengah hari)
- [ ] Update README dengan instruksi penggunaan
- [ ] Catatan konfigurasi Vercel + Neon
- [ ] Catatan Drizzle schema & migration
