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

<!-- SLIDE 3 (VISUAL 2): Engineering Implementation & Code Base -->
<div class="pt-2 pb-10">

<div class="mb-4">
<span class="text-[10px] font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-2.5 py-1 rounded-md border border-blue-100">Engineering Implementation</span>
<h1 class="text-2xl font-extrabold text-slate-900 mt-1">
Modul Utama Engine Backend
</h1>
</div>

<div class="grid grid-cols-12 gap-6 items-center">

<div class="col-span-5 space-y-3">

<div class="ref-card p-3.5 border-l-4 border-l-[#00285d]">
<div class="font-bold text-slate-800 text-xs">Agent Verifier Service</div>
<p class="text-[11px] text-slate-500 mt-0.5">Modul Go-lang murni untuk validasi kriptografi dan verifikasi hash transaksi.</p>
</div>

<div class="ref-card p-3.5 border-l-4 border-l-emerald-500">
<div class="font-bold text-slate-800 text-xs">Kafka Event Pipeline</div>
<p class="text-[11px] text-slate-500 mt-0.5">Penanganan antrean log berskala tinggi secara asinkronus tanpa bottleneck.</p>
</div>

<div class="ref-card p-3.5 border-l-4 border-l-blue-500">
<div class="font-bold text-slate-800 text-xs">REST & gRPC Endpoints</div>
<p class="text-[11px] text-slate-500 mt-0.5">Antarmuka komunikasi internal berkecepatan tinggi antar mikroservis.</p>
</div>

</div>

<!-- Real Code Window (Visual Kode 2) -->
<div class="col-span-7">
<div class="bg-slate-900 rounded-xl shadow-xl overflow-hidden border border-slate-800">
<div class="bg-slate-950 px-4 py-2.5 flex items-center justify-between border-b border-slate-800">
<div class="flex items-center space-x-1.5">
<span class="w-2.5 h-2.5 rounded-full bg-rose-500"></span>
<span class="w-2.5 h-2.5 rounded-full bg-amber-500"></span>
<span class="w-2.5 h-2.5 rounded-full bg-emerald-500"></span>
<span class="text-xs text-slate-400 font-mono ml-2">internal/blockchain/agentverifier/service.go</span>
</div>
<span class="text-[10px] text-emerald-400 font-mono font-bold bg-emerald-950 px-2 py-0.5 rounded">Go 1.22</span>
</div>
<div class="p-3.5 text-[11px] font-mono leading-relaxed">

```go {1-3|4-6|all}
func (s *Service) VerifyAuditTransaction(ctx context.Context, req *VerifyRequest) (*VerifyResult, error) {
    // 1. Dekripsi Payload & Cek Signature
    if err := s.verifier.ValidatePayload(req.Payload); err != nil {
        return nil, fmt.Errorf("audit integrity failed: %w", err)
    }
    // 2. Commit Record ke Blockchain Ledger
    return s.repo.CommitAuditRecord(ctx, req.Payload.Hash)
}
```

</div>
</div>
</div>

</div>

</div>
