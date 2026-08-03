---
layout: default
transition: slide-up
---

<script setup>
import { ref } from 'vue'
const zoomedImage = ref(null)
</script>

<!-- Modal Zoom Image -->
<div v-if="zoomedImage" class="fixed inset-0 z-50 flex items-center justify-center bg-black/80 backdrop-blur-sm cursor-pointer transition-all duration-300" @click="zoomedImage = null">
  <img :src="zoomedImage" class="max-w-[95vw] max-h-[95vh] object-contain rounded-lg shadow-2xl scale-100" />
  <button class="absolute top-6 right-6 text-white bg-slate-800/50 p-2 rounded-full hover:bg-slate-700/80 transition-colors">
    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path></svg>
  </button>
</div>

<!-- Footer -->
<div class="absolute bottom-6 left-10 flex items-center space-x-2 text-xs text-slate-500 font-semibold">
  <span class="w-2 h-2 rounded-full bg-[#00285d]"></span>
  <span>AuditChain Gateway Protocol</span>
</div>
<div class="absolute bottom-6 right-10 text-xs text-slate-400 font-mono">
  Laporan Progres
</div>

<!-- SLIDE 2: Laporan Progres -->
<div class="pt-2 pb-6">
  <div class="flex justify-between items-end mb-2">
    <div>
      <span class="text-[10px] font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-2.5 py-1 rounded-md border border-blue-100">Progress Report</span>
      <h1 class="text-2xl font-extrabold text-slate-900 mt-1">
        Update Fitur: Auto-Discovery & Konfigurasi CDC
      </h1>
    </div>
  </div>
  <p class="text-sm text-slate-600">Pembaruan terbaru pada proses deteksi database dan kemudahan konektivitas sistem gateway.</p>
</div>

<!-- CONTENT GRID -->
<div class="grid grid-cols-3 gap-4">
  
  <!-- Card 1 -->
  <div class="bg-white rounded-xl shadow-sm border border-slate-200 overflow-hidden flex flex-col group cursor-pointer hover:border-blue-300 transition-all" @click="zoomedImage = '/Auto-Discovery & Konfigurasi.png'">
    <div class="h-32 bg-slate-50 flex items-center justify-center p-2 border-b border-slate-100 relative">
      <img src="/Auto-Discovery & Konfigurasi.png" class="max-h-full object-contain rounded shadow-sm border border-slate-200 group-hover:scale-105 transition-transform duration-300" />
      <div class="absolute inset-0 bg-blue-900/0 group-hover:bg-blue-900/10 transition-colors flex items-center justify-center">
        <div class="opacity-0 group-hover:opacity-100 bg-white/90 text-blue-900 text-xs font-bold px-2 py-1 rounded-md shadow-sm transform translate-y-2 group-hover:translate-y-0 transition-all">🔍 Klik untuk Zoom</div>
      </div>
    </div>
    <div class="p-4 flex-1">
      <div class="flex items-center space-x-2 mb-2">
        <div class="w-6 h-6 rounded-full bg-blue-100 text-[#00285d] flex items-center justify-center text-xs font-bold">1</div>
        <h3 class="font-bold text-slate-800 text-sm">Auto-Discovery</h3>
      </div>
      <p class="text-sm text-slate-600 leading-relaxed">
        Penambahan fitur <strong>Auto-Discovery</strong> untuk mendeteksi database dan tabel secara otomatis yang akan diintegrasikan dengan proses <em>Change Data Capture</em> (CDC) pada tahap selanjutnya.
      </p>
    </div>
  </div>

  <!-- Card 2 -->
  <div class="bg-white rounded-xl shadow-sm border border-slate-200 overflow-hidden flex flex-col group cursor-pointer hover:border-blue-300 transition-all" @click="zoomedImage = '/Mengisi username dan PW.png'">
    <div class="h-32 bg-slate-50 flex items-center justify-center p-2 border-b border-slate-100 relative">
      <img src="/Mengisi username dan PW.png" class="max-h-full object-contain rounded shadow-sm border border-slate-200 group-hover:scale-105 transition-transform duration-300" />
      <div class="absolute inset-0 bg-blue-900/0 group-hover:bg-blue-900/10 transition-colors flex items-center justify-center">
        <div class="opacity-0 group-hover:opacity-100 bg-white/90 text-blue-900 text-xs font-bold px-2 py-1 rounded-md shadow-sm transform translate-y-2 group-hover:translate-y-0 transition-all">🔍 Klik untuk Zoom</div>
      </div>
    </div>
    <div class="p-4 flex-1">
      <div class="flex items-center space-x-2 mb-2">
        <div class="w-6 h-6 rounded-full bg-blue-100 text-[#00285d] flex items-center justify-center text-xs font-bold">2</div>
        <h3 class="font-bold text-slate-800 text-sm">Simplifikasi Kredensial</h3>
      </div>
      <p class="text-sm text-slate-600 leading-relaxed">
        Kemudahan konfigurasi di mana pengguna cukup memasukkan <strong>Username & Password</strong>. Sistem akan secara otomatis menghubungkan dan mengonsumsi data dari database klien.
      </p>
    </div>
  </div>

  <!-- Card 3 -->
  <div class="bg-white rounded-xl shadow-sm border border-slate-200 overflow-hidden flex flex-col group cursor-pointer hover:border-blue-300 transition-all" @click="zoomedImage = '/Hasil.png'">
    <div class="h-32 bg-slate-50 flex items-center justify-center p-2 border-b border-slate-100 relative">
      <img src="/Hasil.png" class="max-h-full object-contain rounded shadow-sm border border-slate-200 group-hover:scale-105 transition-transform duration-300" />
      <div class="absolute inset-0 bg-blue-900/0 group-hover:bg-blue-900/10 transition-colors flex items-center justify-center">
        <div class="opacity-0 group-hover:opacity-100 bg-white/90 text-blue-900 text-xs font-bold px-2 py-1 rounded-md shadow-sm transform translate-y-2 group-hover:translate-y-0 transition-all">🔍 Klik untuk Zoom</div>
      </div>
    </div>
    <div class="p-4 flex-1">
      <div class="flex items-center space-x-2 mb-2">
        <div class="w-6 h-6 rounded-full bg-blue-100 text-[#00285d] flex items-center justify-center text-xs font-bold">3</div>
        <h3 class="font-bold text-slate-800 text-sm">Status Koneksi</h3>
      </div>
      <p class="text-sm text-slate-600 leading-relaxed">
        Tampilan hasil koneksi yang secara langsung menginformasikan dan menunjukkan bahwa sistem gateway telah berhasil terhubung dengan database klien.
      </p>
    </div>
  </div>

</div>
