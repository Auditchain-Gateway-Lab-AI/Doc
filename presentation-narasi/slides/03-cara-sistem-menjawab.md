---
layout: default
transition: slide-left
class: "!py-5 !px-10 soft-grid"
---

<div class="deck-footer">
  <span>AuditChain Gateway Simulation</span>
  <span>03 / Tracking User</span>
</div>

<div class="grid grid-cols-12 gap-7 h-full items-center pb-5">
  <div class="col-span-4">
    <span class="kicker">User Mapping</span>
    <h1 class="text-[32px] leading-tight font-extrabold text-slate-950 mt-3">
      Rencana: AuditChain membaca table user milik client.
    </h1>
  </div>

  <div class="col-span-8">
    <div class="grid grid-cols-[1fr_50px_1fr] gap-3 items-center">
      <div class="flow-node">
        <div class="text-[11px] uppercase font-extrabold text-slate-400">Client DB</div>
        <div class="text-3xl font-extrabold text-[#00285d] mt-3">table users</div>
        <div class="mt-5 space-y-2 text-[13px] font-bold text-slate-600">
          <div>user_id</div>
          <div>username</div>
          <div>role</div>
        </div>
      </div>
      <div class="flow-arrow">></div>
      <div class="flow-node dark">
        <div class="text-[11px] uppercase font-extrabold text-blue-100/70">AuditChain</div>
        <div class="text-3xl font-extrabold mt-3">actor map</div>
        <div class="mt-5 flex flex-wrap gap-2">
          <span class="tag-ok">registered user</span>
          <span class="tag-warn">service actor</span>
          <span class="tag-danger">unknown actor</span>
        </div>
      </div>
    </div>
    <div class="narrative-card p-5 mt-5">
      <div class="grid grid-cols-3 gap-4 text-center">
        <div>
          <div class="text-2xl font-extrabold text-[#00285d]">1</div>
          <div class="text-[12px] font-bold text-slate-500 mt-1">detect user table</div>
        </div>
        <div>
          <div class="text-2xl font-extrabold text-emerald-600">2</div>
          <div class="text-[12px] font-bold text-slate-500 mt-1">match actor</div>
        </div>
        <div>
          <div class="text-2xl font-extrabold text-red-600">3</div>
          <div class="text-[12px] font-bold text-slate-500 mt-1">flag anomaly</div>
        </div>
      </div>
    </div>
  </div>
</div>
