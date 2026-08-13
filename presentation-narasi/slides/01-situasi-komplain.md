---
layout: default
transition: fade-out
class: "!py-5 !px-10 soft-grid"
---

<div class="deck-footer">
  <span>AuditChain Gateway Simulation</span>
  <span>01 / Problem</span>
</div>

<div class="h-full pb-5">
  <span class="kicker">Problem</span>
  <h1 class="text-[36px] leading-tight font-extrabold text-slate-950 mt-4">
    Masalah yang sering muncul di sistem client
  </h1>

  <div class="grid grid-cols-3 gap-5 mt-10">
    <div class="quote-card min-h-[190px]">
      <div class="speaker">Case 01</div>
      <div class="quote">"Data saya hilang"</div>
      <div class="mt-5 text-[13px] font-bold text-slate-500">INSERT -> DELETE</div>
    </div>
    <div class="quote-card min-h-[190px]">
      <div class="speaker">Case 02</div>
      <div class="quote">"Sudah update kok masih sama"</div>
      <div class="mt-5 text-[13px] font-bold text-slate-500">UPDATE -> UPDATE BALIK</div>
    </div>
    <div class="quote-card min-h-[190px] border-l-4 border-l-red-500">
      <div class="speaker">Case 03</div>
      <div class="quote">"Siapa yang ubah?"</div>
      <div class="mt-5 text-[13px] font-bold text-red-600">ACTOR TIDAK JELAS</div>
    </div>
  </div>

  <div class="ink-panel p-5 mt-8">
    <div class="text-[12px] text-blue-100/80 uppercase font-extrabold">Goal</div>
    <div class="text-2xl font-extrabold mt-1">Setiap perubahan data punya jejak: siapa, kapan, dan aksi apa.</div>
  </div>
</div>
