---
layout: default
transition: slide-left
---

<div class="px-8 pt-3">
  <div><div class="text-[10px] font-bold uppercase tracking-[0.2em] text-blue-700">Frontend · Rencana Lanjutan</div><h1 class="m-0 mt-1 text-2xl font-extrabold tracking-tight text-slate-900">Perluasan fitur Client Portal</h1><p class="mt-1 text-[11px] text-slate-600">Dua pekerjaan FE untuk melengkapi alur pemulihan dan penelusuran log.</p></div>
  <div class="mt-3 grid grid-cols-2 gap-4">
    <section class="rounded-2xl border border-blue-100 bg-white p-4 shadow-sm">
      <div class="flex items-center justify-between"><span class="flex h-11 w-11 items-center justify-center rounded-xl bg-blue-50 text-lg font-bold text-blue-800">01</span><span class="rounded-full bg-blue-50 px-3 py-1 text-[9px] font-bold uppercase tracking-wide text-blue-800">Navigation</span></div>
      <div class="mt-3 text-[18px] font-bold leading-tight text-slate-900">Menu Recovery di dashboard baru</div>
      <p class="mt-2 text-[12px] leading-relaxed text-slate-600">Tuntaskan menu Recovery di dashboard Client Portal baru. Route dan tab dasar sudah ada di repo; pekerjaan berikutnya adalah memastikan entry point dari Monitor/temuan integritas dan menyambungkan data live ke backend.</p>
      <div class="mt-3 rounded-xl bg-slate-50 px-3 py-2 text-[10px] leading-relaxed text-slate-700"><strong>Selesai bila:</strong> pengguna bisa membuka incident dari temuan integritas, melihat preflight, dan memahami hasil recovery lewat data API.</div>
    </section>
    <section class="rounded-2xl border border-indigo-100 bg-white p-4 shadow-sm">
      <div class="flex items-center justify-between"><span class="flex h-11 w-11 items-center justify-center rounded-xl bg-indigo-50 text-lg font-bold text-indigo-800">02</span><span class="rounded-full bg-indigo-50 px-3 py-1 text-[9px] font-bold uppercase tracking-wide text-indigo-800">Recovery Logs</span></div>
      <div class="mt-3 text-[18px] font-bold leading-tight text-slate-900">Multi Recovery Logs</div>
      <p class="mt-2 text-[12px] leading-relaxed text-slate-600">Tampilkan banyak recovery request/log sekaligus dengan filter status, incident, resource, dan waktu. Sediakan detail per request untuk melihat actor, operasi, hasil read-back, dan status CDC.</p>
      <div class="mt-3 rounded-xl bg-slate-50 px-3 py-2 text-[10px] leading-relaxed text-slate-700"><strong>Catatan backend:</strong> request aktif pada resource yang sama ditolak sebagai conflict; UI perlu menjelaskan status itu dan tetap menampilkan request dari resource lain.</div>
    </section>
  </div>
  <div class="mt-2 rounded-xl bg-blue-950 px-4 py-2 text-[10px] leading-relaxed text-white"><span class="font-bold text-blue-200">Urutan:</span> lengkapi menu dan integrasi sumber data Recovery → susun Multi Recovery Logs → validasi hasil backend.</div>
</div>
<div class="absolute bottom-3 left-10 text-[9px] font-semibold uppercase tracking-[0.16em] text-slate-400">AUDITCHAIN · FRONTEND PLAN</div>
<div class="absolute bottom-3 right-10 text-[9px] font-mono text-slate-400">06 / 09</div>
