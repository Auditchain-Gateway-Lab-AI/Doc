---
layout: default
transition: slide-left
---

<div class="px-8 pt-2">
  <div class="flex items-end justify-between">
    <div>
      <div class="text-[10px] font-bold uppercase tracking-[0.2em] text-amber-700">Langkah berikutnya</div>
      <h1 class="m-0 mt-1 text-2xl font-extrabold tracking-tight text-slate-900">Rencana lanjutan</h1>
    </div>
    <div class="text-[10px] text-slate-500">Frontend · Ketahanan log · Operasional</div>
  </div>

  <section class="mt-3 rounded-2xl border border-amber-200 bg-amber-50/70 px-4 py-3">
    <div class="text-[9px] font-bold uppercase tracking-[0.18em] text-amber-800">Fokus utama · Ketahanan Kafka</div>
    <div class="mt-1 text-[15px] font-bold text-slate-900">Perubahan client tetap tercatat saat Kafka terputus</div>
    <p class="mt-1 text-[10px] leading-relaxed text-slate-700">Cari cara agar perubahan tetap bisa dikirim ke AuditChain setelah Kafka pulih, termasuk jika log Kafka sempat terhapus.</p>
  </section>

  <div class="mt-3 grid grid-cols-12 items-start gap-3">
    <div class="col-span-7 space-y-2">
      <div class="text-[9px] font-bold uppercase tracking-[0.18em] text-blue-800">Rencana frontend</div>
      <div class="grid grid-cols-2 gap-2">
        <section class="rounded-xl border border-blue-100 bg-white p-3">
          <div class="text-xs font-bold text-slate-900">Menu Recovery</div>
          <p class="mt-1 text-[9px] leading-relaxed text-slate-600">Tambahkan menu Recovery di dashboard Client Portal yang baru.</p>
        </section>
        <section class="rounded-xl border border-blue-100 bg-white p-3">
          <div class="text-xs font-bold text-slate-900">Multi Recovery Logs</div>
          <p class="mt-1 text-[9px] leading-relaxed text-slate-600">Dukung tampilan beberapa catatan recovery dalam satu portal.</p>
        </section>
      </div>
    </div>
    <div class="col-span-5">
      <div class="overflow-hidden rounded-xl border border-slate-200 bg-white p-1 shadow-sm">
        <ZoomImage src="/client-registration-redacted.png" alt="Contoh tampilan registrasi client dengan installer dan API key disamarkan" preview-class="mx-auto block max-h-[105px] w-full rounded-lg object-contain" />
      </div>
      <div class="mt-1 text-center text-[8px] text-slate-500">Contoh registrasi client · klik gambar untuk perbesar · data disamarkan</div>
    </div>
  </div>

  <div class="mt-3">
    <div class="mb-2 text-[9px] font-bold uppercase tracking-[0.18em] text-slate-600">Rencana minor · delivery dan pengujian</div>
    <div class="grid grid-cols-5 gap-2">
      <div class="rounded-xl border border-slate-200 bg-white p-2.5"><div class="text-[9px] font-bold leading-tight text-slate-900">Deploy Client Portal</div></div>
      <div class="rounded-xl border border-slate-200 bg-white p-2.5"><div class="text-[9px] font-bold leading-tight text-slate-900">CI/CD repo dashboard client</div></div>
      <div class="rounded-xl border border-slate-200 bg-white p-2.5"><div class="text-[9px] font-bold leading-tight text-slate-900">Domain publik untuk registry client</div></div>
      <div class="rounded-xl border border-slate-200 bg-white p-2.5"><div class="text-[9px] font-bold leading-tight text-slate-900">Aktifkan cronjob</div></div>
      <div class="rounded-xl border border-slate-200 bg-white p-2.5"><div class="text-[9px] font-bold leading-tight text-slate-900">Uji INSERT, UPDATE, DELETE Morbis dengan data besar</div></div>
    </div>
  </div>
</div>
<div class="absolute bottom-3 left-10 text-[9px] font-semibold uppercase tracking-[0.16em] text-slate-400">AUDITCHAIN · NEXT STEPS</div>
<div class="absolute bottom-3 right-10 text-[9px] font-mono text-slate-400">06 / 07</div>
