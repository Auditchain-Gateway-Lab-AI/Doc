---
layout: default
transition: slide-left
---

<!-- Footer -->
<div class="absolute bottom-6 left-10 flex items-center space-x-2 text-xs text-slate-500 font-semibold">
<span class="w-2 h-2 rounded-full bg-[#00285d]"></span>
<span>AuditChain Gateway Protocol</span>
</div>
<div class="absolute bottom-6 right-10 text-xs text-slate-400 font-mono">
Sprint 2026
</div>

<!-- SLIDE: Peningkatan Tampilan Log History -->
<div class="pt-2 pb-10">

<div class="mb-4">
<span class="text-xs font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-3 py-1 rounded-md border border-blue-100">Progress Report: UI/UX</span>
<h1 class="text-2xl font-black text-slate-900 mt-1.5">
Peningkatan Tampilan Log History Dashboard
</h1>
</div>

<p class="text-sm text-slate-600 mb-4 max-w-3xl leading-relaxed">
  Pembaruan signifikan pada struktur dan keterbacaan riwayat log aktivitas. Transformasi ini dirancang untuk mempermudah pelacakan (<i>tracking</i>) dan analisis data secara visual bagi pengguna.
</p>

<div class="grid grid-cols-2 gap-6">

  <!-- BEFORE -->
  <div class="bg-white p-4 rounded-xl border border-slate-200 shadow-sm flex flex-col space-y-3">
    <div class="flex items-center justify-between border-b border-slate-100 pb-2">
      <span class="text-sm font-extrabold text-slate-800 flex items-center gap-1.5">
        <span class="w-2.5 h-2.5 rounded-full bg-red-500"></span> Sebelum (Before)
      </span>
    </div>
    <div class="flex-grow bg-slate-50 rounded border border-slate-100 overflow-hidden flex items-center justify-center p-2 h-[220px]">
      <img src="/loghistory-before.png" class="max-h-full object-contain rounded shadow-sm border border-slate-200/50" />
    </div>
    <div class="bg-red-50 p-2.5 rounded-lg border border-red-100 text-xs text-red-900 leading-snug">
      Desain awal menyajikan data mentah yang kurang terstruktur, sehingga menyulitkan pembacaan aktivitas sistem dengan cepat.
    </div>
  </div>

  <!-- AFTER -->
  <div class="bg-white p-4 rounded-xl border border-slate-200 shadow-sm flex flex-col space-y-3">
    <div class="flex items-center justify-between border-b border-slate-100 pb-2">
      <span class="text-sm font-extrabold text-slate-800 flex items-center gap-1.5">
        <span class="w-2.5 h-2.5 rounded-full bg-emerald-500"></span> Sesudah (After)
      </span>
      <span class="text-[10px] font-mono font-bold text-emerald-700 bg-emerald-50 px-2 py-0.5 rounded border border-emerald-200">NEW UI</span>
    </div>
    <div class="flex-grow bg-slate-50 rounded border border-slate-100 overflow-hidden flex items-center justify-center p-2 h-[220px]">
      <img src="/loghistory-after.png" class="max-h-full object-contain rounded shadow-sm border border-slate-200/50" />
    </div>
    <div class="bg-emerald-50 p-2.5 rounded-lg border border-emerald-200 text-xs text-emerald-950 font-medium leading-snug">
      ✨ <strong>Tampilan Modern & Rapi:</strong> Hirarki informasi yang jelas, penambahan detail terstruktur, serta estetika visual yang lebih intuitif.
    </div>
  </div>

</div>

</div>
