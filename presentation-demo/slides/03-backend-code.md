---
layout: default
transition: slide-left
---

<script setup>
import { ref } from 'vue'
const zoomImage = ref(null)
</script>

<!-- Footer -->
<div class="absolute bottom-6 left-10 flex items-center space-x-2 text-xs text-slate-500 font-semibold">
<span class="w-2 h-2 rounded-full bg-[#00285d]"></span>
<span>AuditChain Gateway Protocol</span>
</div>
<div class="absolute bottom-6 right-10 text-xs text-slate-400 font-mono">
Sprint 2026
</div>

<!-- SLIDE 3: Visual Progress Optimization -->
<div class="pt-2 pb-10">

<div class="mb-3">
<span class="text-[10px] font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-2.5 py-1 rounded-md border border-blue-100">Progress Report</span>
<h1 class="text-xl font-extrabold text-slate-900 mt-1">
Progress & Optimasi Antarmuka Audit Log
</h1>
</div>

<div class="grid grid-cols-2 gap-4">

<!-- Feature 1: Unifikasi Dynamic Table Select -->
<div class="bg-white p-3.5 rounded-xl border border-slate-200 shadow-sm space-y-2.5">
  <div>
    <div class="text-xs font-bold text-slate-800 flex items-center gap-1.5">
      <span class="w-2 h-2 rounded-full bg-[#00285d]"></span>
      1. Unifikasi Select Table ("All Tables")
    </div>
    <p class="text-[10px] text-slate-500 mt-0.5 leading-snug">
      Menyatukan filter tabel ke <strong>All Transaction History</strong>. Mencegah redundansi UI karena data dipusatkan dalam 1 tabel query terintegrasi (alasan data inventory).
    </p>
  </div>
  
  <div class="grid grid-cols-2 gap-2 pt-1">
    <div class="space-y-1">
      <span class="text-[9px] font-bold text-slate-500 uppercase tracking-wider flex items-center justify-between">
        <span>Data Inventory (Awal)</span>
        <span class="text-[8px] text-slate-400 font-normal">🔍 Click Zoom</span>
      </span>
      <div 
        @click="zoomImage = { src: '/before-data-inventory.png', title: 'Data Inventory (Tampilan Awal)' }"
        class="rounded-lg overflow-hidden border border-slate-200 shadow-xs cursor-zoom-in group relative"
      >
        <img src="/before-data-inventory.png" class="w-full h-28 object-cover object-top group-hover:scale-105 transition-transform duration-300" />
        <div class="absolute inset-0 bg-slate-900/0 group-hover:bg-slate-900/10 transition-colors flex items-center justify-center">
          <span class="opacity-0 group-hover:opacity-100 bg-slate-900/80 text-white text-[9px] px-2 py-0.5 rounded-full backdrop-blur-xs font-mono transition-opacity">Zoom 🔍</span>
        </div>
      </div>
    </div>
    <div class="space-y-1">
      <span class="text-[9px] font-bold text-blue-700 uppercase tracking-wider flex items-center justify-between">
        <span>Unified Select Table (Hasil)</span>
        <span class="text-[8px] text-blue-400 font-normal">🔍 Click Zoom</span>
      </span>
      <div 
        @click="zoomImage = { src: '/after-alltables-all-trancsaction.png', title: 'Unified Select Table (All Transaction History)' }"
        class="rounded-lg overflow-hidden border border-blue-200 shadow-xs cursor-zoom-in group relative"
      >
        <img src="/after-alltables-all-trancsaction.png" class="w-full h-28 object-cover object-top group-hover:scale-105 transition-transform duration-300" />
        <div class="absolute inset-0 bg-blue-900/0 group-hover:bg-blue-900/10 transition-colors flex items-center justify-center">
          <span class="opacity-0 group-hover:opacity-100 bg-blue-900/80 text-white text-[9px] px-2 py-0.5 rounded-full backdrop-blur-xs font-mono transition-opacity">Zoom 🔍</span>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- Feature 2: Sorting Kronologis -->
<div class="bg-white p-3.5 rounded-xl border border-slate-200 shadow-sm space-y-2.5">
  <div>
    <div class="text-xs font-bold text-slate-800 flex items-center gap-1.5">
      <span class="w-2 h-2 rounded-full bg-emerald-600"></span>
      2. Sorting Kronologis (Newest / Oldest First)
    </div>
    <p class="text-[10px] text-slate-500 mt-0.5 leading-snug">
      Fitur pengurutan data transaksi audit (<code class="text-[9px] bg-slate-100 px-1 rounded text-emerald-700 font-mono">DESC</code> / <code class="text-[9px] bg-slate-100 px-1 rounded text-emerald-700 font-mono">ASC</code>) yang tersinkronisasi dengan Date Range Window (<strong class="text-slate-600">FROM - TO</strong>).
    </p>
  </div>

  <div class="grid grid-cols-2 gap-2 pt-1">
    <div class="space-y-1">
      <span class="text-[9px] font-bold text-emerald-700 uppercase tracking-wider flex items-center justify-between">
        <span>Newest First (Terbaru)</span>
        <span class="text-[8px] text-emerald-500 font-normal">🔍 Click Zoom</span>
      </span>
      <div 
        @click="zoomImage = { src: '/newest-first.png', title: 'Sorting Mode: Newest First (Terbaru)' }"
        class="rounded-lg overflow-hidden border border-emerald-200 shadow-xs cursor-zoom-in group relative"
      >
        <img src="/newest-first.png" class="w-full h-28 object-cover object-top group-hover:scale-105 transition-transform duration-300" />
        <div class="absolute inset-0 bg-emerald-900/0 group-hover:bg-emerald-900/10 transition-colors flex items-center justify-center">
          <span class="opacity-0 group-hover:opacity-100 bg-emerald-900/80 text-white text-[9px] px-2 py-0.5 rounded-full backdrop-blur-xs font-mono transition-opacity">Zoom 🔍</span>
        </div>
      </div>
    </div>
    <div class="space-y-1">
      <span class="text-[9px] font-bold text-amber-700 uppercase tracking-wider flex items-center justify-between">
        <span>Oldest First (Terlama)</span>
        <span class="text-[8px] text-amber-500 font-normal">🔍 Click Zoom</span>
      </span>
      <div 
        @click="zoomImage = { src: '/oldest-first.png', title: 'Sorting Mode: Oldest First (Terlama)' }"
        class="rounded-lg overflow-hidden border border-amber-200 shadow-xs cursor-zoom-in group relative"
      >
        <img src="/oldest-first.png" class="w-full h-28 object-cover object-top group-hover:scale-105 transition-transform duration-300" />
        <div class="absolute inset-0 bg-amber-900/0 group-hover:bg-amber-900/10 transition-colors flex items-center justify-center">
          <span class="opacity-0 group-hover:opacity-100 bg-amber-900/80 text-white text-[9px] px-2 py-0.5 rounded-full backdrop-blur-xs font-mono transition-opacity">Zoom 🔍</span>
        </div>
      </div>
    </div>
  </div>
</div>

</div>

<!-- Interactive Modal Lightbox for Image Zoom -->
<Teleport to="body">
  <div 
    v-if="zoomImage" 
    class="fixed inset-0 z-[9999] bg-slate-950/85 backdrop-blur-md flex flex-col items-center justify-center p-6 cursor-zoom-out animate-fade-in"
    @click="zoomImage = null"
  >
    <div class="relative max-w-5xl max-h-[85vh] flex flex-col items-center bg-slate-900 border border-slate-700/80 rounded-2xl shadow-2xl overflow-hidden p-3 space-y-2" @click.stop>
      <div class="w-full flex items-center justify-between px-3 py-1 border-b border-slate-800 text-slate-200">
        <span class="text-xs font-bold font-mono text-emerald-400">{{ zoomImage.title }}</span>
        <button 
          @click="zoomImage = null" 
          class="text-xs text-slate-400 hover:text-white bg-slate-800 hover:bg-slate-700 px-2.5 py-1 rounded-lg transition-colors font-mono"
        >
          Tutup ✕
        </button>
      </div>
      <div class="overflow-auto max-h-[75vh] w-full flex items-center justify-center rounded-xl bg-slate-950 p-2">
        <img :src="zoomImage.src" class="max-w-full max-h-[72vh] object-contain rounded-lg shadow-md" />
      </div>
    </div>
  </div>
</Teleport>

</div>
