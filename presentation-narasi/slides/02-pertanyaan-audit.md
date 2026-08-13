---
layout: default
transition: slide-up
class: "!py-5 !px-10"
---

<div class="deck-footer">
  <span>AuditChain Gateway Simulation</span>
  <span>02 / Gambaran Sistem</span>
</div>

<span class="kicker">System Overview</span>
<h1 class="text-[36px] leading-tight font-extrabold text-slate-950 mt-3">
  AuditChain berada di luar aplikasi client
</h1>

<div class="grid grid-cols-[1fr_52px_1fr_52px_1fr] gap-2 mt-10 items-center">
  <div class="flow-node">
    <div class="flow-icon">DB</div>
    <div class="text-2xl font-extrabold text-[#00285d] mt-4">Database Client</div>
    <div class="text-[13px] font-bold text-slate-500 mt-2">users, invoice, payment, transaction</div>
  </div>
  <div class="flow-arrow">></div>
  <div class="flow-node dark">
    <div class="flow-icon bg-white/15 text-white">AC</div>
    <div class="text-2xl font-extrabold mt-4">AuditChain</div>
    <div class="text-[13px] font-bold text-blue-100/80 mt-2">detect changes + actors</div>
  </div>
  <div class="flow-arrow">></div>
  <div class="flow-node">
    <div class="flow-icon">LOG</div>
    <div class="text-2xl font-extrabold text-emerald-600 mt-4">Audit Log</div>
    <div class="text-[13px] font-bold text-slate-500 mt-2">timeline + anomaly flag</div>
  </div>
</div>

<div class="grid grid-cols-4 gap-4 mt-8">
  <div class="metric-pill text-center">INSERT</div>
  <div class="metric-pill text-center">UPDATE</div>
  <div class="metric-pill text-center">DELETE</div>
  <div class="metric-pill text-center">UNKNOWN ACTOR</div>
</div>
