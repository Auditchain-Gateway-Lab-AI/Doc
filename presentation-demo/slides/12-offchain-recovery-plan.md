---
layout: default
transition: slide-left
---

<div class="px-8 pt-3">
  <div class="text-[10px] font-bold uppercase tracking-[0.2em] text-emerald-700">Pendukung Recovery Off-chain</div>
  <h1 class="m-0 mt-1 text-2xl font-extrabold tracking-tight text-slate-900">Jaga data tetap utuh saat dipulihkan</h1>
  <p class="mt-1 text-[11px] text-slate-600">Data off-chain harus bisa ditulis kembali ke database client tanpa perubahan nilai.</p>

  <div class="mt-3 grid grid-cols-2 gap-3">
    <section class="rounded-2xl border border-emerald-100 bg-white p-3 shadow-sm">
      <div class="flex h-10 w-10 items-center justify-center rounded-xl bg-emerald-50 text-sm font-bold text-emerald-800">01</div>
      <h2 class="mt-2 text-[12px] font-bold text-slate-900">Normalisasi lossless</h2>
      <p class="mt-1 text-[9px] leading-relaxed text-slate-600">Ikuti schema Debezium agar ID besar, decimal, dan tanggal tetap presisi; pastikan after-state utuh (Oracle ALL COLUMNS).</p>
    </section>
    <section class="rounded-2xl border border-emerald-100 bg-white p-3 shadow-sm">
      <div class="flex h-10 w-10 items-center justify-center rounded-xl bg-emerald-50 text-sm font-bold text-emerald-800">02</div>
      <h2 class="mt-2 text-[12px] font-bold text-slate-900">Kolom sensitif aman</h2>
      <p class="mt-1 text-[9px] leading-relaxed text-slate-600">Jangan simpan [REDACTED]. Kecualikan dari audit/recovery atau simpan terenkripsi.</p>
    </section>
  </div>

  <div class="mt-3 rounded-2xl bg-[#071629] px-5 py-3 text-white">
    <div class="text-[9px] font-bold uppercase tracking-[0.18em] text-emerald-300">Uji end-to-end</div>
    <div class="mt-1 flex items-center justify-between gap-3 text-[12px] font-semibold">
      <span class="rounded-lg border border-white/10 bg-white/5 px-3 py-1.5">Tamper</span><span class="text-emerald-300">→</span>
      <span class="rounded-lg border border-white/10 bg-white/5 px-3 py-1.5">Verify</span><span class="text-emerald-300">→</span>
      <span class="rounded-lg border border-white/10 bg-white/5 px-3 py-1.5">Recovery</span><span class="text-emerald-300">→</span>
      <span class="rounded-lg border border-emerald-300/20 bg-emerald-300/10 px-3 py-1.5 text-emerald-100">Read-back hash cocok</span>
    </div>
  </div>
</div>
<div class="absolute bottom-3 left-10 text-[9px] font-semibold uppercase tracking-[0.16em] text-slate-400">AUDITCHAIN · OFF-CHAIN RECOVERY</div>
<div class="absolute bottom-3 right-10 text-[9px] font-mono text-slate-400">06 / 08</div>
