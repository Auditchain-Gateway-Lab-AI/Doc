---
theme: default
highlighter: shiki
lineNumbers: false
colorSchema: light
transition: slide-left
aspectRatio: 16/10
title: Template Laporan Progres
layout: center
class: cover-slide
---

<style>
/* Memaksa background putih untuk slide SELAIN cover */
:root { --slidev-body-bg: #ffffff !important; }
html, body, #app { background-color: #ffffff !important; }

/* CSS khusus untuk Cover Slide dengan warna Navy (#00285d) */
.cover-slide {
  background: linear-gradient(135deg, #00285d 0%, #00193a 50%, #00285d 100%) !important;
  color: #FFFFFF !important;
  position: relative;
  overflow: hidden;
  padding: 0 !important;
}

/* Siluet dan Garis Cahaya (Streaks) Lebar Diagonal ala Kaca */
.cover-slide::before {
  content: '';
  position: absolute;
  top: -50%; left: -50%; width: 200%; height: 200%;
  background: linear-gradient(
    -45deg, 
    transparent 40%, 
    rgba(255,255,255,0.06) 45%, 
    rgba(255,255,255,0.15) 48%, 
    rgba(255,255,255,0.03) 50%, 
    rgba(0,0,0,0.3) 55%, 
    transparent 60%,
    rgba(255,255,255,0.08) 65%,
    transparent 70%
  );
  pointer-events: none;
  z-index: 1;
}
.cover-slide::after {
  content: '';
  position: absolute;
  top: 0; left: 0; width: 100%; height: 100%;
  /* Memberikan efek vignette (gelap di ujung) agar siluet lebih dramatis */
  background: radial-gradient(circle at top left, rgba(255,255,255,0.15) 0%, transparent 50%, rgba(0,0,0,0.5) 100%);
  pointer-events: none;
  z-index: 1;
}
</style>

<!-- Header Kiri Atas & Kanan Atas -->
<div class="absolute top-10 left-12 text-sm text-white/60 tracking-wide font-light">
  AuditChain Development Team
</div>
<div class="absolute top-10 right-12 text-sm text-white/60 tracking-wide font-light">
  2026
</div>

<!-- Bagian Tengah (Logo) -->
<div class="flex flex-col items-center justify-center w-full h-full relative z-10">
  
  <!-- LOGO AUDITCHAIN -->
  <img src="/logo.png" class="h-48 object-contain hover:scale-105 transition-all duration-500 bg-white p-6 rounded-3xl shadow-2xl" />
  
  <div class="mt-8 text-white/90 font-light tracking-widest text-2xl text-center uppercase">
    Laporan Progress <br/> Auditchain Gateway
  </div>

</div>

<!--
HALAMAN SAMPUL (COVER)
Cara edit: Ganti teks header di atas, dan masukkan file logo ke folder 'public/'.
-->

---
layout: default
---

# 📝 Ringkasan Pencapaian (Sprint Ini)

Berikut adalah target yang berhasil diselesaikan pada minggu ini:

- ✅ **[Fitur 1]**: Penjelasan singkat tentang apa yang sudah selesai.
- ✅ **[Fitur 2]**: Penjelasan singkat fitur 2.
- 🚧 **[Fitur 3]**: (On-Progress) Masih dalam tahap pengembangan...

<br>

> **Catatan Eksekutif:** 
> [Tulis ringkasan singkat atau keputusan penting untuk petinggi di sini]

<!--
SLIDE RINGKASAN
Gunakan slide ini untuk poin-poin utama yang sudah dicapai (high-level).
Jangan terlalu teknis di halaman ini.
-->

---
layout: two-cols
---

# 💻 Pembaruan Kode / API
*[Tulis Nama Modul yang Diperbarui]*

- **Pembaruan:**
  [Jelaskan apa yang diubah pada kode/sistem]
- **Efisiensi:**
  [Sebutkan jika ada peningkatan performa/keamanan]

::right::

<div class="px-6 py-12">
  <div class="bg-white rounded-2xl shadow-xl p-6 border border-gray-100 hover:-translate-y-1 transition-transform">
    <div class="flex items-center space-x-2 mb-4">
      <div class="w-3 h-3 rounded-full bg-red-400"></div>
      <div class="w-3 h-3 rounded-full bg-yellow-400"></div>
      <div class="w-3 h-3 rounded-full bg-green-400"></div>
      <span class="text-xs text-gray-400 ml-2 font-mono">[NAMA_FILE.go/.js]</span>
    </div>
    
```go {1-2|3-4|all}
// [GANTI DENGAN KODE ANDA DI SINI]
func ContohFungsi() {
    // Baris ini akan tersorot saat di-klik (animasi)
    fmt.Println("Progres Selesai!")
}
```
  </div>
</div>

<!--
SLIDE KODE
Ganti 'go' dengan bahasa Anda (js, python, dll).
Ganti angka {1-2|3-4|all} untuk mengatur baris mana yang ingin disorot saat presentasi.
-->

---
layout: default
---

# 🖼️ Tangkapan Layar / Arsitektur

Berikut adalah visualisasi hasil pengerjaan minggu ini:

<div class="flex justify-center mt-8">
  <div class="p-1 rounded-2xl shadow-xl border border-gray-200">
    <!-- GANTI GAMBAR DI BAWAH INI -->
    <!-- Cara: Taruh file gambar di folder `public/`, lalu panggil seperti contoh di bawah -->
    <!-- <img src="/gambar-saya.png" class="rounded-xl w-[600px]" /> -->
    
    <div class="bg-gray-50 rounded-xl p-12 text-center text-gray-400 border border-dashed border-gray-300 w-[600px]">
        <h2 class="text-xl font-bold">🖼️ Taruh Screenshot Anda Di Sini</h2>
    </div>
  </div>
</div>

<!--
SLIDE GAMBAR
Cara memasukkan gambar:
1. Buat folder bernama 'public' di dalam folder presentation-demo.
2. Masukkan gambar Anda ke folder public tersebut.
3. Hapus kotak abu-abu di atas, dan aktifkan kode <img src="...">.
-->

---
layout: center
class: text-center
---

# 🚀 Langkah Selanjutnya & Kendala

<div class="text-left mt-8 bg-red-50 p-6 rounded-xl border border-red-100 text-red-800 shadow-sm max-w-2xl mx-auto">
  <h3 class="font-bold text-lg mb-2">⚠️ Kendala (Blocker):</h3>
  <ul class="list-disc pl-5">
    <li>[Tulis masalah atau dukungan yang dibutuhkan dari petinggi]</li>
    <li>[Kendala 2, jika ada]</li>
  </ul>
</div>

<div class="text-left mt-4 bg-green-50 p-6 rounded-xl border border-green-100 text-green-800 shadow-sm max-w-2xl mx-auto">
  <h3 class="font-bold text-lg mb-2">🎯 Target Sprint Depan:</h3>
  <ul class="list-disc pl-5">
    <li>[Tulis rencana fitur untuk minggu depan]</li>
  </ul>
</div>

<!--
SLIDE BLOCKER & TARGET
Ini adalah slide paling penting untuk manajemen agar mereka tahu apa masalahnya dan rencana selanjutnya.
-->

---
layout: center
class: text-center
---

# Terima Kasih! 🎉

<div class="text-gray-500 mt-4">Ada Pertanyaan?</div>

<!--
SLIDE PENUTUP
-->
