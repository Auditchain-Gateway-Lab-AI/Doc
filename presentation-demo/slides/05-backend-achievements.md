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

<!-- SLIDE 4: Combined Backend, Infrastructure & Problem Solving -->
<div class="pt-2 pb-10">

<div class="mb-4">
<span class="text-xs font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-3 py-1 rounded-md border border-blue-100">Backend, Infrastruktur & Reliability</span>
<h1 class="text-2xl font-black text-slate-900 mt-1.5">
Pencapaian Utama Backend & Solusi Arsitektur CDC
</h1>
</div>

<div class="grid grid-cols-3 gap-4 mb-4">

<!-- Card 1: Oracle CDC & Pipeline -->
<div class="bg-white p-4 rounded-xl border border-slate-200 shadow-sm space-y-3 flex flex-col justify-between">
  <div>
    <div class="flex items-center justify-between border-b border-slate-100 pb-2 mb-2">
      <span class="text-sm font-extrabold text-slate-800 flex items-center gap-1.5">
        <span class="w-2.5 h-2.5 rounded-full bg-blue-600"></span> 1. Real-Time Oracle CDC
      </span>
      <span class="text-[10px] font-mono font-bold text-blue-700 bg-blue-50 px-2 py-0.5 rounded border border-blue-200">REAL-TIME</span>
    </div>
    <p class="text-xs text-slate-600 leading-relaxed">
      Integrasi <strong>Oracle Enterprise DB</strong> via <strong>Debezium & Kafka</strong> ke Go Gateway dan PostgreSQL Sentral.
    </p>
  </div>
  <div class="bg-slate-50 p-2.5 rounded-lg border border-slate-200 text-xs text-slate-700 space-y-1.5">
    <div class="flex justify-between font-mono">
      <span>Multitenant:</span> <strong class="text-slate-900">CDB & PDB Ready</strong>
    </div>
    <div class="flex justify-between font-mono">
      <span>Topic Routing:</span> <strong class="text-blue-600">Dynamic Prefix</strong>
    </div>
  </div>
</div>

<!-- Card 2: Installer Automation -->
<div class="bg-white p-4 rounded-xl border border-slate-200 shadow-sm space-y-3 flex flex-col justify-between">
  <div>
    <div class="flex items-center justify-between border-b border-slate-100 pb-2 mb-2">
      <span class="text-sm font-extrabold text-slate-800 flex items-center gap-1.5">
        <span class="w-2.5 h-2.5 rounded-full bg-emerald-600"></span> 2. Skrip Installer Bulletproof
      </span>
      <span class="text-[10px] font-mono font-bold text-emerald-700 bg-emerald-50 px-2 py-0.5 rounded border border-emerald-200">INSTALL.SH</span>
    </div>
    <p class="text-xs text-slate-600 leading-relaxed">
      Refaktor skrip instalasi agen klien dengan dialog interaktif & otomatisasi susunan JSON rules Debezium.
    </p>
  </div>
  <div class="bg-emerald-50/60 p-2.5 rounded-lg border border-emerald-200 text-xs text-emerald-950 font-medium leading-snug">
    ⚡ Onboarding rumit Oracle tuntas hanya dengan <strong>3 pertanyaan terminal</strong>.
  </div>
</div>

<!-- Card 3: Resolved Blocker -->
<div class="bg-white p-4 rounded-xl border border-slate-200 shadow-sm space-y-3 flex flex-col justify-between">
  <div>
    <div class="flex items-center justify-between border-b border-slate-100 pb-2 mb-2">
      <span class="text-sm font-extrabold text-slate-800 flex items-center gap-1.5">
        <span class="w-2.5 h-2.5 rounded-full bg-amber-500"></span> 3. Bypass LogMiner Blocker
      </span>
      <span class="text-[10px] font-mono font-bold text-emerald-700 bg-emerald-50 px-2 py-0.5 rounded border border-emerald-200">100% RESOLVED</span>
    </div>
    <p class="text-xs text-slate-600 leading-relaxed">
      Penanganan pemblokiran skema <code class="bg-slate-100 px-1 py-0.5 rounded font-mono text-slate-800">SYSTEM</code> oleh Oracle LogMiner internal.
    </p>
  </div>
  <div class="bg-amber-50/70 p-2.5 rounded-lg border border-amber-200 text-xs text-amber-950 leading-snug">
    🛠️ Solusi Taktis: <strong>Koneksi Hybrid</strong> (Host CDB, Target PDB) + Bypass <code class="bg-amber-100/80 px-1 rounded font-mono">schema.include.list</code>.
  </div>
</div>

</div>

<!-- End-to-End Pipeline Banner -->
<div class="bg-gradient-to-r from-[#00285d] to-slate-900 p-4 rounded-xl text-white shadow-md flex items-center justify-between">
  <div class="space-y-1.5">
    <span class="text-xs font-bold uppercase tracking-wider text-blue-200 bg-white/10 px-2.5 py-0.5 rounded font-mono">End-to-End Pipeline Data Flow</span>
    <div class="flex items-center space-x-2 font-mono font-bold text-white text-xs pt-0.5">
      <span class="bg-amber-500/20 text-amber-300 px-2.5 py-1 rounded border border-amber-500/30">Oracle DB</span>
      <span class="text-slate-400">➔</span>
      <span class="bg-blue-500/20 text-blue-300 px-2.5 py-1 rounded border border-blue-500/30">Debezium CDC</span>
      <span class="text-slate-400">➔</span>
      <span class="bg-slate-700 text-slate-200 px-2.5 py-1 rounded border border-slate-600">Apache Kafka</span>
      <span class="text-slate-400">➔</span>
      <span class="bg-indigo-500/20 text-indigo-300 px-2.5 py-1 rounded border border-indigo-500/30">Go Gateway</span>
      <span class="text-slate-400">➔</span>
      <span class="bg-emerald-500/20 text-emerald-300 px-2.5 py-1 rounded border border-emerald-500/30">PostgreSQL Sentral</span>
    </div>
  </div>
  <div class="bg-emerald-500/20 text-emerald-300 px-3.5 py-2 rounded-lg border border-emerald-500/40 text-center flex-shrink-0 ml-4">
    <div class="text-sm font-extrabold font-mono">STABLE & VERIFIED</div>
    <div class="text-[10px] text-slate-300 font-mono">Zero Data Loss Pipeline</div>
  </div>
</div>

</div>

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

<!-- SLIDE 4b: Multi Table Audit -->
<div class="pt-2 pb-10">
<div class="mb-4">
<span class="text-xs font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-3 py-1 rounded-md border border-blue-100">Fitur Baru Client</span>
<h1 class="text-2xl font-black text-slate-900 mt-1.5">
Dukungan Multi-Table Audit
</h1>
</div>

<div class="grid grid-cols-5 gap-6">
<div class="col-span-2 space-y-4 pt-4">
<div class="bg-white p-5 rounded-xl border border-slate-200 shadow-sm border-l-4 border-l-blue-500">
<p class="text-sm text-slate-700 leading-relaxed">
Client sudah bisa menambahkan <strong>beberapa table</strong> sekaligus untuk diaudit oleh sistem kita.
</p>
</div>
<div class="bg-slate-50 p-5 rounded-xl border border-slate-200 shadow-sm border-l-4 border-l-emerald-500">
<p class="text-sm text-slate-700 leading-relaxed">
Jadi client tidak harus memilih 1 saja yang ingin diaudit, melainkan bisa <strong>banyak table</strong> dengan cara memilih table mana saja yang akan dipilih secara fleksibel.
</p>
</div>
</div>

<div class="col-span-3 flex items-center">
<div class="bg-slate-100 p-2 rounded-xl border border-slate-200 shadow-inner w-full">
<img src="/Double adudit.png" alt="Multi Table Audit" class="w-full rounded-lg shadow-sm border border-slate-300" />
</div>
</div>
</div>
</div>
