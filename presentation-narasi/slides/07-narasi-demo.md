---
layout: default
transition: fade-out
class: "!py-5 !px-10 soft-grid"
---

<div class="deck-footer">
  <span>AuditChain Gateway Simulation</span>
  <span>07 / Future Flow</span>
</div>

<div class="grid grid-cols-12 gap-7 h-full items-center pb-5">
  <div class="col-span-5">
    <span class="kicker">Future Flow</span>
    <h1 class="text-[32px] leading-tight font-extrabold text-slate-950 mt-3">
      Gambaran flow ketika sistem sudah punya tracking user.
    </h1>
  </div>

  <div class="col-span-7 grid grid-cols-2 gap-4">
    <div class="flow-node">
      <div class="flow-icon">1</div>
      <div class="text-xl font-extrabold text-[#00285d] mt-4">Detect table user</div>
      <div class="text-[13px] font-bold text-slate-500 mt-2">ambil daftar user client</div>
    </div>
    <div class="flow-node">
      <div class="flow-icon">2</div>
      <div class="text-xl font-extrabold text-emerald-600 mt-4">Track DB event</div>
      <div class="text-[13px] font-bold text-slate-500 mt-2">insert / update / delete</div>
    </div>
    <div class="flow-node">
      <div class="flow-icon">3</div>
      <div class="text-xl font-extrabold text-indigo-600 mt-4">Compare actor</div>
      <div class="text-[13px] font-bold text-slate-500 mt-2">registered vs unknown</div>
    </div>
    <div class="flow-node border-l-4 border-l-red-500">
      <div class="flow-icon">!</div>
      <div class="text-xl font-extrabold text-red-600 mt-4">Show anomaly</div>
      <div class="text-[13px] font-bold text-slate-500 mt-2">tetap masuk dashboard</div>
    </div>
  </div>
</div>
