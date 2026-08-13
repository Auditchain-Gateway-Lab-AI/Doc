---
layout: default
transition: fade-out
class: "!py-5 !px-10"
---

<div class="deck-footer">
  <span>AuditChain Gateway Simulation</span>
  <span>04 / Direct DB Change</span>
</div>

<span class="kicker">Anomaly Case</span>
<h1 class="text-[34px] leading-tight font-extrabold text-slate-950 mt-3">
  Kalau ada update langsung ke DB, AuditChain tetap menangkap event.
</h1>

<div class="grid grid-cols-[1fr_52px_1fr_52px_1fr] gap-2 mt-10 items-center">
  <div class="flow-node">
    <div class="flow-icon">?</div>
    <div class="text-2xl font-extrabold text-red-600 mt-4">Hacker / DB Admin</div>
    <div class="text-[13px] font-bold text-slate-500 mt-2">akses langsung database</div>
  </div>
  <div class="flow-arrow">></div>
  <div class="flow-node dark">
    <div class="flow-icon bg-white/15 text-white">SQL</div>
    <div class="text-2xl font-extrabold mt-4">UPDATE / DELETE</div>
    <div class="text-[13px] font-bold text-blue-100/80 mt-2">tanpa lewat aplikasi</div>
  </div>
  <div class="flow-arrow">></div>
  <div class="flow-node border-l-4 border-l-red-500">
    <div class="flow-icon">!</div>
    <div class="text-2xl font-extrabold text-red-600 mt-4">Anomaly Actor</div>
    <div class="text-[13px] font-bold text-slate-500 mt-2">tetap tampil di audit log</div>
  </div>
</div>

<div class="grid grid-cols-3 gap-4 mt-8">
  <div class="metric-pill text-center">event detected</div>
  <div class="metric-pill text-center">actor not registered</div>
  <div class="metric-pill text-center">marked as anomaly</div>
</div>
