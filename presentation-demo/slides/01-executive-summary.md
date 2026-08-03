---
layout: default
transition: fade-out
class: "!py-2 !px-8"
---

<!-- Footer -->
<div class="absolute bottom-2 left-10 flex items-center space-x-2 text-[10px] text-slate-500 font-semibold z-10">
<span class="w-1.5 h-1.5 rounded-full bg-[#00285d]"></span>
<span>AuditChain Gateway Protocol</span>
</div>
<div class="absolute bottom-2 right-10 text-[10px] text-slate-400 font-mono z-10">
Sprint 2026
</div>

<!-- SLIDE 1: Executive Summary / Ringkasan Progress -->
<div class="grid grid-cols-12 gap-6 h-full items-center pb-2 pt-2">

<!-- Left Overview Column -->
<div class="col-span-4 pr-1">
<span class="text-[9px] font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-2 py-0.5 rounded-md border border-blue-100">Executive Summary</span>
<h1 class="text-2xl font-extrabold text-slate-900 leading-tight mt-3">
Ringkasan Progress <br/>
<span class="text-[#00285d]">Sprint Terbaru</span>
</h1>
<p class="text-[10px] text-slate-500 mt-2.5 leading-relaxed">
Rangkuman pembaruan fitur utama yang telah dikembangkan dan dipush oleh tim pada sistem Gateway Audit.
</p>

<div class="mt-4 p-3 rounded-xl bg-blue-50/80 border border-blue-100 text-[9.5px] text-slate-700">
<div class="font-bold text-[#00285d] mb-0.5">Status Fitur:</div>
Modul Auto-Discovery DB dan Optimasi UI Audit Log siap digunakan.
</div>
</div>

<!-- Right Cards Grid (4 Key Highlights) -->
<div class="col-span-8 grid grid-cols-2 gap-3">

<!-- Card 1: Auto-Discovery (Team) -->
<div class="ref-card p-3.5 flex flex-col justify-between relative border-t-2 border-t-[#00285d] bg-white rounded-xl shadow-sm border border-slate-200">
<div class="flex justify-between items-center mb-2">
<span class="text-[8px] font-mono font-bold uppercase text-slate-400">Database Engine</span>
<span class="px-1.5 py-0.5 bg-blue-50 text-blue-700 text-[8px] font-bold rounded border border-blue-100">CDC Ready</span>
</div>
<div>
<div class="text-xs font-bold text-slate-800 flex items-center gap-1">
  <span class="w-1.5 h-1.5 rounded-full bg-[#00285d]"></span> Auto-Discovery DB
</div>
<p class="text-[9.5px] text-slate-500 mt-1 leading-normal">
Mendeteksi database & tabel klien secara otomatis untuk persiapan proses <em>Change Data Capture</em> (CDC).
</p>
</div>
</div>

<!-- Card 2: Simplifikasi Kredensial (Team) -->
<div class="ref-card p-3.5 flex flex-col justify-between relative border-t-2 border-t-emerald-500 bg-white rounded-xl shadow-sm border border-slate-200">
<div class="flex justify-between items-center mb-2">
<span class="text-[8px] font-mono font-bold uppercase text-slate-400">Konektivitas Klien</span>
<span class="px-1.5 py-0.5 bg-emerald-50 text-emerald-700 text-[8px] font-bold rounded border border-emerald-100">Auto Connect</span>
</div>
<div>
<div class="text-xs font-bold text-slate-800 flex items-center gap-1">
  <span class="w-1.5 h-1.5 rounded-full bg-emerald-500"></span> Simplifikasi Kredensial
</div>
<p class="text-[9.5px] text-slate-500 mt-1 leading-normal">
Menghubungkan DB klien hanya dengan Username & Password, serta indikator status koneksi real-time.
</p>
</div>
</div>

<!-- Card 3: Unifikasi Select Table (User) -->
<div class="ref-card p-3.5 flex flex-col justify-between relative border-t-2 border-t-indigo-500 bg-white rounded-xl shadow-sm border border-slate-200">
<div class="flex justify-between items-center mb-2">
<span class="text-[8px] font-mono font-bold uppercase text-slate-400">UI / UX Log Query</span>
<span class="px-1.5 py-0.5 bg-indigo-50 text-indigo-700 text-[8px] font-bold rounded border border-indigo-100">Optimasi View</span>
</div>
<div>
<div class="text-xs font-bold text-slate-800 flex items-center gap-1">
  <span class="w-1.5 h-1.5 rounded-full bg-indigo-500"></span> Unifikasi Select Table
</div>
<p class="text-[9.5px] text-slate-500 mt-1 leading-normal">
Menyatukan filter tabel (<code class="text-[8px] bg-slate-100 px-1 rounded text-indigo-700">All Tables</code>) ke <em>All Transaction History</em> untuk menghilangkan redundansi Data Inventory.
</p>
</div>
</div>

<!-- Card 4: Sorting Kronologis (User) -->
<div class="ref-card p-3.5 flex flex-col justify-between relative border-t-2 border-t-amber-500 bg-white rounded-xl shadow-sm border border-slate-200">
<div class="flex justify-between items-center mb-2">
<span class="text-[8px] font-mono font-bold uppercase text-slate-400">Data Exploration</span>
<span class="text-[8px] font-bold text-amber-600 bg-amber-50 px-1.5 py-0.5 rounded border border-amber-100">DESC / ASC</span>
</div>
<div>
<div class="text-xs font-bold text-slate-800 flex items-center gap-1">
  <span class="w-1.5 h-1.5 rounded-full bg-amber-500"></span> Sorting Kronologis
</div>
<p class="text-[9.5px] text-slate-500 mt-1 leading-normal">
Pengurutan transaksi (Newest / Oldest First) yang tersinkronisasi penuh dengan Date Range Window (<strong class="text-slate-600">FROM - TO</strong>).
</p>
</div>
</div>

</div>

</div>
