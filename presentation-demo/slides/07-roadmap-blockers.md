---
layout: default
transition: slide-left
---

<div class="px-8 pt-3">
  <div>
    <div class="text-[10px] font-bold uppercase tracking-[0.2em] text-emerald-700">Progress 3 · Backend</div>
    <h1 class="m-0 mt-1 text-2xl font-extrabold tracking-tight text-slate-900">Recovery dari sumber data client</h1>
    <p class="mt-1 max-w-4xl text-[11px] leading-relaxed text-slate-600">Jalur recovery aktif mengambil data dari database client, lalu mencocokkannya dengan catatan AuditChain.</p>
  </div>

  <div class="mt-5 grid grid-cols-3 gap-3">
    <section class="rounded-2xl border border-emerald-100 bg-white p-4 shadow-sm">
      <div class="text-[9px] font-bold uppercase tracking-wide text-emerald-800">01 · Sumber pemulihan</div>
      <div class="mt-2 text-[16px] font-bold text-slate-900">Langsung dari database client</div>
      <p class="mt-2 text-[10px] leading-relaxed text-slate-600">Data recovery dibaca dari sumber off-chain milik client. MinIO tidak lagi dipakai pada jalur aktif ini.</p>
    </section>
    <section class="rounded-2xl border border-blue-100 bg-white p-4 shadow-sm">
      <div class="text-[9px] font-bold uppercase tracking-wide text-blue-800">02 · Sebelum pemulihan</div>
      <div class="mt-2 text-[16px] font-bold text-slate-900">Catatan AuditChain diperiksa</div>
      <p class="mt-2 text-[10px] leading-relaxed text-slate-600">Log perubahan menjadi acuan untuk memastikan data yang akan dipulihkan memang sesuai.</p>
    </section>
    <section class="rounded-2xl border border-slate-200 bg-white p-4 shadow-sm">
      <div class="text-[9px] font-bold uppercase tracking-wide text-slate-600">03 · Setelah pemulihan</div>
      <div class="mt-2 text-[16px] font-bold text-slate-900">Hasilnya dicek kembali</div>
      <p class="mt-2 text-[10px] leading-relaxed text-slate-600">Data pada client dibaca ulang agar hasil recovery bisa dipastikan sudah sesuai.</p>
    </section>
  </div>

  <div class="mt-5 rounded-2xl bg-[#071629] px-5 py-3 text-white">
    <span class="text-[10px] font-bold uppercase tracking-[0.2em] text-emerald-300">Analogi:</span>
    <span class="ml-2 text-xs">mengambil barang dari gudang yang sebenarnya, lalu mencocokkannya dengan buku catatan resmi.</span>
  </div>
</div>
<div class="absolute bottom-3 left-10 text-[9px] font-semibold uppercase tracking-[0.16em] text-slate-400">AUDITCHAIN · BACKEND</div>
<div class="absolute bottom-3 right-10 text-[9px] font-mono text-slate-400">07 / 10</div>
