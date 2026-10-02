---
layout: default
transition: slide-left
---

<div class="px-8 pt-2">
  <div class="flex items-end justify-between">
    <div><div class="text-[10px] font-bold uppercase tracking-[0.2em] text-rose-700">Major Plan · Ketahanan CDC</div><h1 class="m-0 mt-1 text-2xl font-extrabold leading-tight tracking-tight text-slate-900">Deteksi Kafka mati dan log terhapus</h1></div>
    <div class="rounded-full border border-rose-200 bg-rose-50 px-3 py-1.5 text-[9px] font-bold uppercase tracking-wide text-rose-800">Rencana teknis</div>
  </div>

  <div class="mt-2 rounded-2xl bg-[#071629] px-4 py-2.5 text-white">
    <div class="flex items-center justify-between gap-2 text-[11px] font-semibold">
      <span class="rounded-lg border border-white/10 bg-white/5 px-3 py-2">Perubahan di DB client</span><span class="text-emerald-300">→ CDC</span>
      <span class="rounded-lg border border-white/10 bg-white/5 px-3 py-2">Durable spool</span><span class="text-emerald-300">→ Kafka</span>
      <span class="rounded-lg border border-rose-300/30 bg-rose-500/15 px-3 py-2 text-rose-100">Broker mati / log hilang</span><span class="text-emerald-300">→ replay</span>
      <span class="rounded-lg border border-white/10 bg-white/5 px-3 py-2">Gateway</span><span class="text-emerald-300">→ anchor</span>
      <span class="rounded-lg border border-emerald-300/20 bg-emerald-300/10 px-3 py-2 text-emerald-100">On-chain</span>
    </div>
  </div>

  <div class="mt-3 grid grid-cols-3 gap-3">
    <section class="rounded-2xl border border-blue-100 bg-white p-3 shadow-sm">
      <div class="text-[9px] font-bold uppercase tracking-[0.16em] text-blue-800">01 · Tahan saat Kafka down</div>
      <div class="mt-2 text-[16px] font-bold leading-tight text-slate-900">Simpan salinan di sisi client</div>
      <p class="mt-2 text-[10px] leading-relaxed text-slate-600">Agent menulis event ke durable spool/outbox sebelum publish. Beri setiap event ID + urutan per client; simpan sampai Gateway mengonfirmasi checkpoint on-chain.</p>
    </section>
    <section class="rounded-2xl border border-emerald-100 bg-white p-3 shadow-sm">
      <div class="text-[9px] font-bold uppercase tracking-[0.16em] text-emerald-800">02 · Lindungi Kafka</div>
      <div class="mt-2 text-[16px] font-bold leading-tight text-slate-900">Replikasi dan batasi penghapusan</div>
      <p class="mt-2 text-[10px] leading-relaxed text-slate-600">Untuk cluster produksi: replication factor 3, min ISR 2, producer acks=all + idempotence. Batasi ACL Delete/DeleteRecords dan audit perubahan topic.</p>
    </section>
    <section class="rounded-2xl border border-amber-100 bg-white p-3 shadow-sm">
      <div class="text-[9px] font-bold uppercase tracking-[0.16em] text-amber-800">03 · Deteksi lalu pulihkan</div>
      <div class="mt-2 text-[16px] font-bold leading-tight text-slate-900">Bandingkan urutan dan replay gap</div>
      <p class="mt-2 text-[10px] leading-relaxed text-slate-600">Gateway membandingkan sequence/source offset dengan checkpoint on-chain. Gap memicu alarm; replay dari spool atau WAL/binlog yang masih tersedia, lalu deduplikasi berdasarkan event ID.</p>
    </section>
  </div>

  <div class="mt-2 grid grid-cols-[1.2fr_1fr] gap-3">
    <div class="rounded-xl border border-rose-200 bg-rose-50 px-3 py-2 text-[8px] leading-relaxed text-rose-950"><strong>Batas pemulihan:</strong> jika log Kafka, spool client, dan log sumber database semuanya sudah hilang/expired, urutan historis tidak bisa direkonstruksi tepat dari snapshot saat ini.</div>
    <div class="rounded-xl bg-slate-50 px-3 py-2 text-[7px] leading-relaxed text-slate-600">
      Referensi:
      <a class="text-blue-700 underline" href="https://kafka.apache.org/31/configuration/producer-configs/">Kafka acks/idempotence</a> ·
      <a class="text-blue-700 underline" href="https://kafka.apache.org/43/configuration/topic-configs/">min ISR</a> ·
      <a class="text-blue-700 underline" href="https://kafka.apache.org/43/security/authorization-and-acls/">ACL delete</a> ·
      <a class="text-blue-700 underline" href="https://debezium.io/documentation/reference/stable/transformations/outbox-event-router.html">Debezium outbox</a>
      <div class="mt-1 text-[7px] text-slate-600"><strong>Skenario uji:</strong> broker down → DML → hapus topic (test) → restart → cek gap/replay.</div>
    </div>
  </div>
</div>
<div class="absolute bottom-3 left-10 text-[9px] font-semibold uppercase tracking-[0.16em] text-slate-400">AUDITCHAIN · MAJOR PLAN</div>
<div class="absolute bottom-3 right-10 text-[9px] font-mono text-slate-400">07 / 09</div>
