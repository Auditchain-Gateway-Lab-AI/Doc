---
layout: default
transition: slide-left
class: "!py-5 !px-10"
---

<div class="deck-footer">
  <span>AuditChain Gateway Simulation</span>
  <span>06 / Feature Plan</span>
</div>

<span class="kicker">Next Plan</span>
<h1 class="text-[34px] leading-tight font-extrabold text-slate-950 mt-3">
  Plan fitur berikutnya: tracking kegiatan user + anomaly detection.
</h1>

<div class="mt-8 grid grid-cols-5 gap-3 items-stretch">
  <div class="narrative-card p-4">
    <div class="text-[10px] font-extrabold text-slate-400">PLAN 01</div>
    <div class="text-base font-extrabold text-[#00285d] mt-2">Scan users table</div>
    <p class="text-[11px] text-slate-600 mt-2">Baca daftar user dari DB client.</p>
  </div>
  <div class="flex items-center justify-center text-2xl font-extrabold text-emerald-500">></div>
  <div class="narrative-card p-4">
    <div class="text-[10px] font-extrabold text-slate-400">PLAN 02</div>
    <div class="text-base font-extrabold text-[#00285d] mt-2">Map actor</div>
    <p class="text-[11px] text-slate-600 mt-2">Cocokkan event DB dengan user terdaftar.</p>
  </div>
  <div class="flex items-center justify-center text-2xl font-extrabold text-emerald-500">></div>
  <div class="narrative-card p-4">
    <div class="text-[10px] font-extrabold text-slate-400">PLAN 03</div>
    <div class="text-base font-extrabold text-red-600 mt-2">Flag anomaly</div>
    <p class="text-[11px] text-slate-600 mt-2">Actor tidak dikenal tetap masuk log.</p>
  </div>
</div>

<div class="grid grid-cols-3 gap-4 mt-7">
  <div class="lane">
    <div class="text-lg font-extrabold text-slate-900">User Activity</div>
    <p class="text-[12px] text-slate-600 mt-1">insert, update, delete</p>
  </div>
  <div class="lane">
    <div class="text-lg font-extrabold text-slate-900">Actor Status</div>
    <p class="text-[12px] text-slate-600 mt-1">known / unknown</p>
  </div>
  <div class="lane">
    <div class="text-lg font-extrabold text-slate-900">Alert Layer</div>
    <p class="text-[12px] text-slate-600 mt-1">anomaly indicator</p>
  </div>
</div>
