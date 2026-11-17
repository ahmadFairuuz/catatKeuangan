# Requirement - Financial Tracking Web App

## Overview
Web aplikasi pencatatan keuangan yang dapat diakses di Android dan iOS dengan deploy gratis ke Vercel. Database: Neon PostgreSQL (serverless, free tier).

## Fitur Utama
- CRUD transaksi keuangan (Create, Read, Update — Delete nanti)
- Type transaksi: `expense` | `income`
- Kategori expense: `makan` | `transport` | `paket` | `lainnya`
- Kategori income: `gaji` | `bonus` | `lainnya`
- Dashboard ringkasan: total expense, total income, balance
- Riwayat transaksi terfilter per kategori & type
- Grafik pengeluaran per kategori (pie/bar chart)
- Filter rentang tanggal (bulan/tahun)
- Desain mobile-first, responsive 360px+ tanpa horizontal scroll

## Teknologi
- Frontend: React + Vite + Tailwind CSS
- Database: Neon PostgreSQL (serverless, scale-to-zero)
- ORM: Drizzle ORM (ringan, type-safe)
- Deploy: Vercel (free tier)
- Chart: Recharts (ringan, React-native)

## Data Model
```typescript
interface Transaksi {
  id: string;           // uuid / nanoid
  tanggal: string;      // ISO 8601: "2026-11-17"
  type: "expense" | "income";
  kategori: "makan" | "transport" | "paket" | "lainnya" | "gaji" | "bonus";
  nominal: number;      // integer (rupiah, tanpa desimal)
  catatan?: string;     // optional
  createdAt: string;    // ISO timestamp
  updatedAt: string;    // ISO timestamp
}
```

## Validasi Input
- `nominal`: wajib, integer > 0
- `type`: wajib, enum expense | income
- `kategori`: wajib, sesuai enum per type
- `tanggal`: wajib, valid ISO date

## Aksesibilitas
- Responsive design untuk mobile (Android/iOS)
- Breakpoint minimum 360px tanpa horizontal scroll
- Font size minimum 16px untuk readability pada mobile
- Touch-friendly area minimum 44px untuk tombol dan input

## Batasan
- Free tier Vercel (limit bandwidth, function minutes)
- Neon free: 0.5GB storage, auto-suspend after 5 min idle
- Single-user (belum ada auth/multi-device sync)

## Catatan Desain (taste guardrails)
- **No Inter font** — gunakan Geist atau sistem font stack.
- **No emoji** di label atau chart tooltip.
- **Warna amber** untuk harga/nominal, bukan merah atau hijau (mudah dibaca di theme dark/light).
- Grid layout: desktop 3 kolom, mobile 1 kolom per baris.
