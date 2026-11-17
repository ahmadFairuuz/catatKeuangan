# Requirement - Financial Tracking Web App

## Overview
Web aplikasi pencatatan keuangan yang dapat diakses di Android dan iOS dengan deploy gratis ke Vercel.

## Fitur Utama
- Pencatatan transaksi keuangan
- Kategori transaksi: makan, transport, paket/olshop
- Dashboard ringkasan
- Riwayat transaksi

## Teknologi
- Frontend: React + Vite + Tailwind CSS
- Deploy: Vercel (free tier)
- Penyimpanan: localStorage (client-side) atau Supabase free tier

## Aksesibilitas
- Responsive design untuk mobile (Android/iOS)
- Bisa diakses melalui browser mobile

## Batasan
- Free tier Vercel (limit bandwidth, function minutes)
- localStorage hanya tersimpan per-browser (bukan sinkron multi-device)
- Supabase: free tier dengan 500MB storage, 1GB bandwidth per bulan