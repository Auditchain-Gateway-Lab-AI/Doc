---
layout: default
transition: slide-left
---

<!-- Footer -->
<div class="absolute bottom-6 left-10 flex items-center space-x-2 text-xs text-slate-500 font-semibold">
<span class="w-2 h-2 rounded-full bg-[#00285d]"></span>
<span>AuditChain Gateway Protocol</span>
</div>
<div class="absolute bottom-6 right-10 text-xs text-slate-400 font-mono">
Sprint 2026
</div>

<!-- Lightbox Overlay -->
<div
  v-if="lightbox"
  class="fixed inset-0 z-50 flex items-center justify-center"
  style="background: rgba(0,0,0,0.88);"
  @click="lightbox = null"
>
  <button
    class="absolute top-4 right-6 text-white text-3xl font-bold leading-none opacity-70 hover:opacity-100 transition-opacity"
    @click.stop="lightbox = null"
  >✕</button>
  <img
    :src="lightbox"
    class="max-w-[90vw] max-h-[88vh] rounded-xl shadow-2xl object-contain"
    @click.stop
  />
  <p class="absolute bottom-5 text-white text-xs opacity-50">Klik di luar gambar untuk menutup</p>
</div>

<!-- SLIDE: Frontend Update -->
<div class="pt-2 pb-10">

<div class="mb-4">
  <span class="text-xs font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-3 py-1 rounded-md border border-blue-100">Progress Report: Frontend</span>
  <h1 class="text-2xl font-black text-slate-900 mt-1.5">
    Update Antarmuka & Fitur Frontend
  </h1>
  <p class="text-sm text-slate-600 mt-1 leading-relaxed">
    Peningkatan UI pada <strong>Admin Portal</strong> dan <strong>Gateway Portal</strong> — mencakup manajemen CDC, monitoring user, serta dukungan <i>dark mode</i>.
  </p>
</div>

<!-- 4-image grid -->
<div class="grid grid-cols-4 gap-3">

  <!-- Card 1: Admin Client Users CDC -->
  <div class="bg-slate-50 rounded-xl border border-slate-200 shadow-sm flex flex-col overflow-hidden relative group">
    <div class="absolute top-0 w-full h-0.5 bg-[#00285d]"></div>
    <div
      class="flex-1 overflow-hidden cursor-zoom-in relative"
      @click="lightbox = '/admin-clientusers-cdc-menu.png'"
    >
      <img src="/admin-clientusers-cdc-menu.png" class="w-full h-[150px] object-cover object-top transition-transform duration-300 group-hover:scale-105" />
      <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-all duration-200 flex items-center justify-center">
        <span class="text-white text-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-200 drop-shadow-lg">🔍</span>
      </div>
    </div>
    <div class="p-2.5 border-t border-slate-200 bg-white">
      <span class="text-[9px] font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-1.5 py-0.5 rounded border border-blue-100">Admin Portal</span>
      <p class="text-[10px] font-bold text-slate-800 mt-1 leading-tight">Client Users CDC</p>
      <p class="text-[9px] text-slate-500 mt-0.5 leading-relaxed">Halaman manajemen user yang terdeteksi dari database client via CDC. Menampilkan <i>Watched Tables</i> dan status connector per-client.</p>
    </div>
  </div>

  <!-- Card 2: Dark Mode -->
  <div class="bg-slate-50 rounded-xl border border-slate-200 shadow-sm flex flex-col overflow-hidden relative group">
    <div class="absolute top-0 w-full h-0.5 bg-indigo-500"></div>
    <div
      class="flex-1 overflow-hidden flex items-center justify-center bg-slate-100 cursor-zoom-in relative"
      @click="lightbox = '/darkmode-page.png'"
    >
      <img src="/darkmode-page.png" class="w-full h-[150px] object-contain transition-transform duration-300 group-hover:scale-105" />
      <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-all duration-200 flex items-center justify-center">
        <span class="text-white text-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-200 drop-shadow-lg">🔍</span>
      </div>
    </div>
    <div class="p-2.5 border-t border-slate-200 bg-white">
      <span class="text-[9px] font-bold uppercase tracking-wider text-indigo-700 bg-indigo-50 px-1.5 py-0.5 rounded border border-indigo-200">New Feature</span>
      <p class="text-[10px] font-bold text-slate-800 mt-1 leading-tight">Dark / Light / System Mode</p>
      <p class="text-[9px] text-slate-500 mt-0.5 leading-relaxed">Pilihan tema tampilan — <i>Dark</i>, <i>Light</i>, atau mengikuti preferensi sistem — tersedia di menu profil user.</p>
    </div>
  </div>

  <!-- Card 3: Web Users List -->
  <div class="bg-slate-50 rounded-xl border border-slate-200 shadow-sm flex flex-col overflow-hidden relative group">
    <div class="absolute top-0 w-full h-0.5 bg-emerald-500"></div>
    <div
      class="flex-1 overflow-hidden cursor-zoom-in relative"
      @click="lightbox = '/web-user-menu.png'"
    >
      <img src="/web-user-menu.png" class="w-full h-[150px] object-cover object-top transition-transform duration-300 group-hover:scale-105" />
      <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-all duration-200 flex items-center justify-center">
        <span class="text-white text-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-200 drop-shadow-lg">🔍</span>
      </div>
    </div>
    <div class="p-2.5 border-t border-slate-200 bg-white">
      <span class="text-[9px] font-bold uppercase tracking-wider text-emerald-700 bg-emerald-50 px-1.5 py-0.5 rounded border border-emerald-200">Gateway Portal</span>
      <p class="text-[10px] font-bold text-slate-800 mt-1 leading-tight">Web Users Monitoring</p>
      <p class="text-[9px] text-slate-500 mt-0.5 leading-relaxed">Dashboard monitoring user yang terdeteksi dari database client, lengkap dengan identity coverage, status, dan riwayat aktivitas.</p>
    </div>
  </div>

  <!-- Card 4: Web Users Detail -->
  <div class="bg-slate-50 rounded-xl border border-slate-200 shadow-sm flex flex-col overflow-hidden relative group">
    <div class="absolute top-0 w-full h-0.5 bg-emerald-500"></div>
    <div
      class="flex-1 overflow-hidden cursor-zoom-in relative"
      @click="lightbox = '/web-user-menu-2.png'"
    >
      <img src="/web-user-menu-2.png" class="w-full h-[150px] object-cover object-top transition-transform duration-300 group-hover:scale-105" />
      <div class="absolute inset-0 bg-black/0 group-hover:bg-black/20 transition-all duration-200 flex items-center justify-center">
        <span class="text-white text-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-200 drop-shadow-lg">🔍</span>
      </div>
    </div>
    <div class="p-2.5 border-t border-slate-200 bg-white">
      <span class="text-[9px] font-bold uppercase tracking-wider text-emerald-700 bg-emerald-50 px-1.5 py-0.5 rounded border border-emerald-200">Gateway Portal</span>
      <p class="text-[10px] font-bold text-slate-800 mt-1 leading-tight">Detail Panel — Web User</p>
      <p class="text-[9px] text-slate-500 mt-0.5 leading-relaxed">Panel samping menampilkan identitas lengkap user: username, email, role, action type (INSERT/UPDATE/DELETE), audit log ID, dan resource.</p>
    </div>
  </div>

</div>

<!-- Summary bar -->
<div class="mt-3 bg-slate-50 px-4 py-2 rounded-lg border border-slate-200 flex items-center gap-3 shadow-sm">
  <span class="w-2 h-2 rounded-full bg-emerald-500 flex-shrink-0 animate-pulse"></span>
  <p class="text-[10px] text-slate-700 font-medium leading-snug">
    Kedua portal kini memiliki UI yang konsisten dengan dukungan <strong>dark mode</strong>, halaman <strong>Client Users CDC</strong> (Admin), dan halaman <strong>Web Users</strong> (Gateway) yang siap digunakan untuk demo.
  </p>
  <span class="ml-auto text-[9px] text-slate-400 italic flex-shrink-0">🔍 klik gambar untuk perbesar</span>
</div>

</div>

<script setup>
import { ref } from 'vue'
const lightbox = ref(null)
</script>
