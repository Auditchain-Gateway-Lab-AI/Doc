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

<!-- SLIDE: Deteksi DB Engine -->
<div class="pt-2 pb-10">

<div class="mb-4">
<span class="text-xs font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-3 py-1 rounded-md border border-blue-100">Progress Report: Fitur Konektivitas</span>
<h1 class="text-2xl font-black text-slate-900 mt-1.5">
Pembaruan Deteksi <i>Database Engine</i> Klien
</h1>
</div>

<p class="text-sm text-slate-600 leading-relaxed mb-6 max-w-3xl">
Sistem <i>Gateway</i> kini telah ditingkatkan dengan kapabilitas untuk mendeteksi, mencatat, dan menyesuaikan konfigurasi secara otomatis berdasarkan jenis <strong>Database Engine</strong> yang digunakan oleh klien.
</p>

<div class="grid grid-cols-2 gap-8">
  
<div>
<div class="text-sm font-bold text-slate-800 border-b border-slate-200 pb-2 mb-4">
Dukungan Multi-Database Aktif:
</div>

<div class="grid grid-cols-2 gap-3">
<div class="bg-slate-50 p-2.5 rounded-lg border border-slate-200 shadow-sm flex items-center space-x-3">
<div class="w-7 h-7 rounded bg-blue-100 flex items-center justify-center text-blue-700 font-bold font-mono text-xs">PG</div>
<span class="text-sm font-semibold text-slate-700">PostgreSQL</span>
</div>
<div class="bg-slate-50 p-2.5 rounded-lg border border-slate-200 shadow-sm flex items-center space-x-3">
<div class="w-7 h-7 rounded bg-orange-100 flex items-center justify-center text-orange-700 font-bold font-mono text-xs">MY</div>
<span class="text-sm font-semibold text-slate-700">MySQL</span>
</div>
<div class="bg-slate-50 p-2.5 rounded-lg border border-slate-200 shadow-sm flex items-center space-x-3">
<div class="w-7 h-7 rounded bg-red-100 flex items-center justify-center text-red-700 font-bold font-mono text-xs">OR</div>
<span class="text-sm font-semibold text-slate-700">Oracle DB</span>
</div>
<div class="bg-slate-50 p-2.5 rounded-lg border border-slate-200 shadow-sm flex items-center space-x-3">
<div class="w-7 h-7 rounded bg-emerald-100 flex items-center justify-center text-emerald-700 font-bold font-mono text-xs">MG</div>
<span class="text-sm font-semibold text-slate-700">MongoDB</span>
</div>
</div>

<div class="mt-4 bg-blue-50/50 p-3 rounded-lg border border-blue-100 text-xs text-blue-900 leading-snug font-medium">
Pembaruan ini memastikan setiap koneksi klien menggunakan parameter dan penanganan data yang tepat secara instan tanpa perlu intervensi manual.
</div>
</div>

<div class="bg-white p-3 rounded-xl border border-slate-200 shadow-sm relative flex flex-col justify-center">
<div class="absolute -top-3 -right-2 bg-[#00285d] text-white text-[10px] font-bold px-2 py-1 rounded border border-blue-800 shadow-sm z-10">
KOLOM DETEKSI ENGINE
</div>
<div class="rounded-lg overflow-hidden border border-slate-200 bg-slate-50 flex items-center justify-center">
<img src="/db-engine-column.png" class="w-full object-contain max-h-[220px]" />
</div>
<p class="text-center text-[10px] text-slate-500 mt-2 font-mono">Tampilan kolom deteksi pada manajemen klien</p>
</div>

</div>

</div>
