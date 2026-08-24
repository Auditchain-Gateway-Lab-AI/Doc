---
layout: default
transition: slide-left
---

<!-- Footer -->
<div class="absolute bottom-6 left-10 flex items-center space-x-2 text-xs text-slate-500 font-semibold z-50">
<span class="w-2 h-2 rounded-full bg-[#00285d]"></span>
<span>AuditChain Gateway Protocol</span>
</div>
<div class="absolute bottom-6 right-10 text-xs text-slate-400 font-mono z-50">
Sprint 2026
</div>

<!-- SLIDE: Backend Installer Update -->
<div class="pt-2 pb-10 max-w-5xl mx-auto">

<div class="mb-6">
  <span class="text-xs font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-3 py-1 rounded-md border border-blue-100">Progress Report: Backend</span>
  <h1 class="text-2xl font-black text-slate-900 mt-2">
    Automasi Installer Backend & CDC Setup
  </h1>
  <p class="text-sm text-slate-600 mt-2 leading-relaxed">
    Pembaruan signifikan pada <i>shell script</i> <code>install.sh</code> untuk meningkatkan ketahanan (<i>resilience</i>) saat instalasi <i>agent</i> dan sinkronisasi Debezium.
  </p>
</div>

<div class="grid grid-cols-3 gap-6 mt-8">
  
  <div class="bg-slate-50 p-5 rounded-xl border border-slate-200 shadow-sm relative overflow-hidden flex flex-col">
    <div class="absolute top-0 left-0 w-full h-1.5 bg-blue-500"></div>
    <div class="text-3xl mb-4 mt-1">🐳</div>
    <h3 class="text-sm font-bold text-slate-800 mb-2">Smart Docker Networking</h3>
    <p class="text-xs text-slate-600 leading-relaxed">Resolusi dinamis port PostgreSQL & penggunaan <code class="bg-slate-200/60 px-1 rounded text-slate-600">host.docker.internal</code> untuk koneksi <i>cross-container</i> yang mulus.</p>
  </div>
  
  <div class="bg-slate-50 p-5 rounded-xl border border-slate-200 shadow-sm relative overflow-hidden flex flex-col">
    <div class="absolute top-0 left-0 w-full h-1.5 bg-emerald-500"></div>
    <div class="text-3xl mb-4 mt-1">⚙️</div>
    <h3 class="text-sm font-bold text-slate-800 mb-2">Automated CDC Setup</h3>
    <p class="text-xs text-slate-600 leading-relaxed">Verifikasi dan pembuatan <i>Publication</i> (<code class="bg-slate-200/60 px-1 rounded text-slate-600">dbz_publication</code>) dilakukan secara eksplisit sebelum konektor Debezium diaktifkan.</p>
  </div>

  <div class="bg-slate-50 p-5 rounded-xl border border-slate-200 shadow-sm relative overflow-hidden flex flex-col">
    <div class="absolute top-0 left-0 w-full h-1.5 bg-amber-500"></div>
    <div class="text-3xl mb-4 mt-1">🔄</div>
    <h3 class="text-sm font-bold text-slate-800 mb-2">Resilient Restart</h3>
    <p class="text-xs text-slate-600 leading-relaxed">Implementasi <i>smart wait</i> dan pengecekan koneksi saat database me-<i>recreate container</i> untuk konfigurasi <code class="bg-slate-200/60 px-1 rounded text-slate-600">wal_level=logical</code>.</p>
  </div>

</div>

</div>
