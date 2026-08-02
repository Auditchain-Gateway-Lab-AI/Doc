---
theme: default
highlighter: shiki
lineNumbers: false
colorSchema: light
transition: slide-left
aspectRatio: 16/10
title: AuditChain Gateway Progress Report
layout: center
class: cover-slide
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap');

* {
  font-family: 'Plus Jakarta Sans', -apple-system, BlinkMacSystemFont, sans-serif;
}

:root { --slidev-body-bg: #f8fafc !important; }
html, body, #app { background-color: #f8fafc !important; }

/* Background Cover Slide: Navy Blue dengan efek cahaya profesional */
.cover-slide {
  background: linear-gradient(135deg, #00285d 0%, #00193c 60%, #00102b 100%) !important;
  color: #FFFFFF !important;
  position: relative;
  overflow: hidden;
  padding: 0 !important;
}

/* Subtle Glass Reflection */
.cover-slide::before {
  content: '';
  position: absolute;
  top: -50%; left: -50%; width: 200%; height: 200%;
  background: linear-gradient(
    -45deg, 
    transparent 40%, 
    rgba(255,255,255,0.04) 46%, 
    rgba(255,255,255,0.12) 49%, 
    rgba(255,255,255,0.02) 52%, 
    transparent 58%
  );
  pointer-events: none;
  z-index: 1;
  animation: subtlePan 8s ease-in-out infinite alternate;
}

@keyframes subtlePan {
  0% { transform: translate(-20px, -10px) rotate(0deg); }
  100% { transform: translate(20px, 10px) rotate(2deg); }
}

.ref-card {
  background-color: #ffffff;
  border-radius: 1rem;
  border: 1px solid #e2e8f0;
  box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.02), 0 1px 2px -1px rgba(0, 0, 0, 0.02);
  transition: all 0.25s ease;
}
.ref-card:hover {
  transform: translateY(-2px);
  border-color: #cbd5e1;
  box-shadow: 0 10px 15px -3px rgba(0, 40, 93, 0.05);
}
</style>

<!-- Cover Header -->
<div class="absolute top-8 left-12 text-[11px] text-white/70 tracking-widest uppercase font-semibold flex items-center space-x-2">
<span class="w-1.5 h-1.5 rounded-full bg-emerald-400"></span>
<span>AuditChain Core Development</span>
</div>
<div class="absolute top-8 right-12 text-xs text-white/80 font-mono tracking-wider px-3 py-1 bg-white/10 rounded-lg border border-white/10 backdrop-blur-md">
Q3 - 2026
</div>

<!-- Cover Center Logo -->
<div class="flex flex-col items-center justify-center w-full h-full relative z-10">
<div class="p-1 rounded-3xl bg-white/10 backdrop-blur-md shadow-2xl mb-4 border border-white/15">
<img src="/logo.png" class="h-40 object-contain bg-white p-6 rounded-2xl shadow-inner" />
</div>

<div class="text-white font-extrabold tracking-widest text-2xl text-center uppercase">
Laporan Progres <span class="text-emerald-400">AuditChain Gateway</span>
</div>
<p class="text-xs text-blue-200/70 mt-2 font-medium tracking-wide">
Sistem Verifikasi & Ledger Audit Terdistribusi
</p>
</div>

---
layout: default
---

<!-- Footer -->
<div class="absolute bottom-6 left-10 flex items-center space-x-2 text-xs text-slate-500 font-semibold">
<span class="w-2 h-2 rounded-full bg-[#00285d]"></span>
<span>AuditChain Gateway Protocol</span>
</div>
<div class="absolute bottom-6 right-10 text-xs text-slate-400 font-mono">
Sprint 2026
</div>

<!-- SLIDE 1 (TEKS / METRIK): Key Performance & Technical Metrics -->
<div class="grid grid-cols-12 gap-8 h-full items-center pt-2 pb-10">

<div class="col-span-4 pr-2">
<span class="text-[10px] font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-2.5 py-1 rounded-md border border-blue-100">Executive Summary</span>
<h1 class="text-3xl font-extrabold text-slate-900 leading-tight mt-3">
Ringkasan Performa <br/>
<span class="text-[#00285d]">Sprint Agustus</span>
</h1>
<p class="text-xs text-slate-500 mt-3 leading-relaxed">
Evaluasi metrik teknis dan tingkat kestabilan gateway dalam menangani lalu lintas verifikasi transaksi audit.
</p>

<div class="mt-5 p-3.5 rounded-xl bg-slate-100 border border-slate-200/80 text-[11px] text-slate-600">
<div class="font-bold text-slate-800 mb-1">Status Milestone:</div>
Semua target arsitektur backend utama telah berhasil diverifikasi tanpa adanya insiden kritis.
</div>
</div>

<div class="col-span-8 grid grid-cols-2 gap-4">

<div class="ref-card p-5 flex flex-col justify-between h-44 relative border-t-2 border-t-[#00285d]">
<div class="flex justify-between items-center">
<span class="text-[10px] font-mono font-bold uppercase text-slate-400">System Availability</span>
<span class="w-2 h-2 rounded-full bg-emerald-500"></span>
</div>
<div class="my-auto">
<div class="text-3xl font-extrabold text-slate-900 tracking-tight">99.9%</div>
<div class="text-xs font-bold text-slate-700 mt-1">Uptime Verifier Node</div>
<p class="text-[11px] text-slate-400 mt-0.5">Operasional tanpa downtime</p>
</div>
</div>

<div class="ref-card p-5 flex flex-col justify-between h-44 relative border-t-2 border-t-emerald-500">
<div class="flex justify-between items-center">
<span class="text-[10px] font-mono font-bold uppercase text-slate-400">Latency Benchmark</span>
<span class="w-2 h-2 rounded-full bg-emerald-500"></span>
</div>
<div class="my-auto">
<div class="text-3xl font-extrabold text-emerald-600 tracking-tight">&lt; 45ms</div>
<div class="text-xs font-bold text-slate-700 mt-1">Waktu Respon API</div>
<p class="text-[11px] text-slate-400 mt-0.5">Optimasi query database</p>
</div>
</div>

<div class="ref-card p-5 flex flex-col justify-between h-44 relative border-t-2 border-t-blue-500">
<div class="flex justify-between items-center">
<span class="text-[10px] font-mono font-bold uppercase text-slate-400">Data Integrity</span>
<span class="w-2 h-2 rounded-full bg-blue-500"></span>
</div>
<div class="my-auto">
<div class="text-3xl font-extrabold text-[#00285d] tracking-tight">100%</div>
<div class="text-xs font-bold text-slate-700 mt-1">Validasi Hash Kriptografi</div>
<p class="text-[11px] text-slate-400 mt-0.5">Nir-kesalahan data log</p>
</div>
</div>

<div class="ref-card p-5 flex flex-col justify-between h-44 relative border-t-2 border-t-teal-500">
<div class="flex justify-between items-center">
<span class="text-[10px] font-mono font-bold uppercase text-slate-400">Security Audit</span>
<span class="w-2 h-2 rounded-full bg-teal-500"></span>
</div>
<div class="my-auto">
<div class="text-3xl font-extrabold text-teal-600 tracking-tight">0 Vulnerability</div>
<div class="text-xs font-bold text-slate-700 mt-1">Keamanan Kode</div>
<p class="text-[11px] text-slate-400 mt-0.5">Lolos pemeriksaan penetrasi</p>
</div>
</div>

</div>

</div>

---
layout: default
---

<!-- Footer -->
<div class="absolute bottom-6 left-10 flex items-center space-x-2 text-xs text-slate-500 font-semibold">
<span class="w-2 h-2 rounded-full bg-[#00285d]"></span>
<span>AuditChain Gateway Protocol</span>
</div>
<div class="absolute bottom-6 right-10 text-xs text-slate-400 font-mono">
Sprint 2026
</div>

<!-- SLIDE 2 (VISUAL 1): Arsitektur Sistem & Flow Diagram -->
<div class="pt-2 pb-10">

<div class="flex justify-between items-end mb-4">
<div>
<span class="text-[10px] font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-2.5 py-1 rounded-md border border-blue-100">System Architecture</span>
<h1 class="text-2xl font-extrabold text-slate-900 mt-1">
Arsitektur Gateway & Alur Data
</h1>
</div>
<div class="text-xs text-slate-400 font-mono">Diagram Interaksi Komponen</div>
</div>

<!-- Frame Diagram Arsitektur -->
<div class="bg-white rounded-xl shadow-sm border border-slate-200 overflow-hidden">
<div class="bg-slate-100/80 px-4 py-2 border-b border-slate-200 flex items-center justify-between">
<div class="flex items-center space-x-2">
<span class="w-2.5 h-2.5 rounded-full bg-slate-300"></span>
<span class="w-2.5 h-2.5 rounded-full bg-slate-300"></span>
<span class="w-2.5 h-2.5 rounded-full bg-slate-300"></span>
<span class="text-xs text-slate-500 font-mono ml-2">architecture_overview.png</span>
</div>
<span class="text-[10px] text-slate-400 font-mono">High-Availability Topology</span>
</div>

<div class="p-6 bg-slate-50/50 flex items-center justify-center min-h-[300px]">

<!-- TEMPAT GAMBAR ARSITEKTUR -->
<!-- <img src="/architecture-diagram.png" class="w-full h-auto object-contain max-h-[310px] rounded-lg border border-slate-200 shadow-sm" /> -->

<div class="border-2 border-dashed border-slate-300 bg-white rounded-xl p-8 text-center w-full max-w-lg shadow-sm hover:border-[#00285d] transition-colors cursor-pointer">
<div class="w-12 h-12 bg-slate-100 text-[#00285d] rounded-xl flex items-center justify-center text-xl mx-auto mb-3 font-bold">
SVG
</div>
<h3 class="font-bold text-slate-800 text-sm">Diagram Arsitektur Sistem Gateway</h3>
<p class="text-xs text-slate-400 mt-1">
Letakkan gambar diagram di <code class="bg-slate-100 text-blue-600 px-1 py-0.5 rounded font-mono">public/architecture.png</code>.
</p>
</div>

</div>
</div>

</div>

---
layout: default
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

---
layout: default
---

<!-- Footer -->
<div class="absolute bottom-6 left-10 flex items-center space-x-2 text-xs text-slate-500 font-semibold">
<span class="w-2 h-2 rounded-full bg-[#00285d]"></span>
<span>AuditChain Gateway Protocol</span>
</div>
<div class="absolute bottom-6 right-10 text-xs text-slate-400 font-mono">
Sprint 2026
</div>

<!-- SLIDE 4 (VISUAL 3): Audit Monitoring Dashboard UI -->
<div class="grid grid-cols-12 gap-8 h-full items-center pt-2 pb-10">

<div class="col-span-5 space-y-4">

<div>
<span class="text-[10px] font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-2.5 py-1 rounded-md border border-blue-100">User Interface</span>
<h1 class="text-2xl font-extrabold text-slate-900 mt-2 leading-tight">
Antarmuka Monitoring <br/> Dashboard Gateway
</h1>
</div>

<div class="space-y-3 text-xs text-slate-600">
<div class="p-3 bg-white rounded-lg border border-slate-200">
<div class="font-bold text-slate-800 mb-0.5">Realtime Telemetry</div>
Visualisasi status kesehatan verifier node dan beban lalu lintas log audit.
</div>

<div class="p-3 bg-white rounded-lg border border-slate-200">
<div class="font-bold text-slate-800 mb-0.5">Audit Log Search & Filter</div>
Pencarian instan bukti audit berdasarkan ID transaksi dan tanda tangan digital.
</div>
</div>

</div>

<!-- Screenshot Container (Visual 3) -->
<div class="col-span-7 pl-2">
<div class="bg-white rounded-xl shadow-sm p-4 border border-slate-300 space-y-3">

<div class="flex items-center justify-between border-b border-slate-100 pb-2">
<span class="text-xs font-bold text-slate-700 font-mono">auditchain_dashboard_ui.png</span>
<span class="px-2 py-0.5 bg-emerald-50 text-emerald-700 text-[10px] font-bold rounded border border-emerald-200">VERIFIED</span>
</div>

<!-- TEMPAT GAMBAR UI DASHBOARD -->
<!-- <img src="/dashboard-ui.png" class="w-full h-48 object-cover rounded-lg border border-slate-200 shadow-sm" /> -->

<div class="border-2 border-dashed border-slate-200 bg-slate-50/80 rounded-lg p-8 text-center hover:border-[#00285d] transition-colors cursor-pointer">
<div class="text-xl font-bold text-slate-400 mb-1">UI MOCKUP</div>
<h4 class="font-bold text-slate-700 text-xs">Tangkapan Layar Dashboard Monitoring</h4>
<p class="text-[10px] text-slate-400 mt-1">Simpan gambar di <code class="bg-white px-1 rounded font-mono">public/dashboard-ui.png</code></p>
</div>

<div class="flex items-center justify-between bg-slate-100 p-2 rounded-lg text-xs font-mono text-slate-600">
<span>Status Engine: <strong class="text-emerald-600">HEALTHY</strong></span>
<span>Cluster: <strong class="text-[#00285d]">prod-gateway-01</strong></span>
</div>

</div>
</div>

</div>

---
layout: default
---

<!-- Footer -->
<div class="absolute bottom-6 left-10 flex items-center space-x-2 text-xs text-slate-500 font-semibold">
<span class="w-2 h-2 rounded-full bg-[#00285d]"></span>
<span>AuditChain Gateway Protocol</span>
</div>
<div class="absolute bottom-6 right-10 text-xs text-slate-400 font-mono">
Sprint 2026
</div>

<!-- SLIDE 5 (TEKS / FEATURE): Platform Capabilities & Specifications Bento Grid -->
<div class="pt-2 pb-10">

<div class="text-center max-w-2xl mx-auto mb-5">
<span class="text-[10px] font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-2.5 py-1 rounded-md border border-blue-100">Platform Specifications</span>
<h1 class="text-2xl font-extrabold text-slate-900 mt-2">
Kapabilitas Utama AuditChain Gateway
</h1>
</div>

<div class="grid grid-cols-3 gap-3.5 max-w-4xl mx-auto">

<div class="bg-[#00285d] text-white p-5 rounded-xl flex flex-col justify-between shadow-md">
<div>
<span class="text-[10px] font-mono text-blue-200 uppercase font-bold tracking-wider">Core Feature</span>
<h3 class="font-extrabold text-sm mt-1">High Throughput Engine</h3>
<p class="text-[11px] text-white/70 mt-1 leading-relaxed">
Dirancang khusus untuk menangani verifikasi berkecepatan tinggi tanpa kompromi performa.
</p>
</div>
<div class="text-[10px] text-emerald-400 font-mono font-bold mt-3">PROD READY</div>
</div>

<div class="ref-card p-5 flex flex-col justify-between">
<div>
<span class="text-[10px] font-mono text-slate-400 uppercase font-bold">Security</span>
<h3 class="font-bold text-slate-800 text-sm mt-1">Proteksi Enkripsi End-to-End</h3>
<p class="text-[11px] text-slate-500 mt-1 leading-relaxed">
Enkripsi SHA-256 dan token JWT pada setiap payload transaksi.
</p>
</div>
<div class="text-[10px] text-slate-400 font-mono">ISO 27001 Compliant</div>
</div>

<div class="ref-card p-5 flex flex-col justify-between">
<div>
<span class="text-[10px] font-mono text-slate-400 uppercase font-bold">Reliability</span>
<h3 class="font-bold text-slate-800 text-sm mt-1">High Availability & Failover</h3>
<p class="text-[11px] text-slate-500 mt-1 leading-relaxed">
Dukungan auto-recovery jika terjadi gangguan pada simpul jaringan.
</p>
</div>
<div class="text-[10px] text-slate-400 font-mono">SLA 99.9%</div>
</div>

<div class="ref-card p-5 flex flex-col justify-between">
<div>
<span class="text-[10px] font-mono text-slate-400 uppercase font-bold">Integration</span>
<h3 class="font-bold text-slate-800 text-sm mt-1">Realtime Audit Ledger</h3>
<p class="text-[11px] text-slate-500 mt-1 leading-relaxed">
Pencatatan langsung ke dalam immutable blockchain ledger.
</p>
</div>
<div class="text-[10px] text-slate-400 font-mono">Direct Consensus</div>
</div>

<div class="ref-card p-5 flex flex-col justify-between">
<div>
<span class="text-[10px] font-mono text-slate-400 uppercase font-bold">Architecture</span>
<h3 class="font-bold text-slate-800 text-sm mt-1">Scalable Microservices</h3>
<p class="text-[11px] text-slate-500 mt-1 leading-relaxed">
Modul terpisah yang memudahkan penskalaan kapasitas server.
</p>
</div>
<div class="text-[10px] text-slate-400 font-mono">Docker & K8s Ready</div>
</div>

<div class="ref-card p-5 flex flex-col justify-between">
<div>
<span class="text-[10px] font-mono text-slate-400 uppercase font-bold">Analytics</span>
<h3 class="font-bold text-slate-800 text-sm mt-1">Laporan Eksekutif Metrik</h3>
<p class="text-[11px] text-slate-500 mt-1 leading-relaxed">
Penyajian data agregasi untuk kemudahan analisis manajemen.
</p>
</div>
<div class="text-[10px] text-slate-400 font-mono">Automated Export</div>
</div>

</div>

</div>

---
layout: center
class: text-center
---

<!-- SLIDE 6: Next Steps & Challenges -->
<div class="max-w-3xl mx-auto mb-6 text-center">
<span class="text-[10px] font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-2.5 py-1 rounded-md border border-blue-100">Roadmap & Challenges</span>
<h1 class="text-2xl font-extrabold text-slate-900 mt-2">Rencana Depan & Kendala Technical</h1>
</div>

<div class="grid grid-cols-2 gap-5 max-w-4xl mx-auto text-left">

<div class="bg-white p-5 rounded-xl border border-rose-200 shadow-sm border-t-2 border-t-rose-500">
<div class="flex items-center justify-between mb-3 pb-2 border-b border-slate-100">
<h3 class="font-extrabold text-slate-800 text-sm">Kendala Utama (Blockers)</h3>
<span class="text-[10px] font-mono font-bold text-rose-600 bg-rose-50 px-2 py-0.5 rounded">ACTION NEEDED</span>
</div>

<ul class="space-y-2.5 text-xs text-slate-600">
<li class="flex items-start space-x-2">
<span class="text-rose-500 font-bold">•</span>
<span>Persetujuan akses kredensial ke server staging blockchain utama dari Infrastructure team.</span>
</li>
<li class="flex items-start space-x-2">
<span class="text-rose-500 font-bold">•</span>
<span>Alokasi tambahan kuota RAM untuk node Kafka consumer di environment pengujian.</span>
</li>
</ul>
</div>

<div class="bg-white p-5 rounded-xl border border-emerald-200 shadow-sm border-t-2 border-t-emerald-500">
<div class="flex items-center justify-between mb-3 pb-2 border-b border-slate-100">
<h3 class="font-extrabold text-slate-800 text-sm">Target Sprint Berikutnya</h3>
<p class="text-[10px] font-mono font-bold text-emerald-600 bg-emerald-50 px-2 py-0.5 rounded">MILESTONE Q3</p>
</div>

<ul class="space-y-2.5 text-xs text-slate-600">
<li class="flex items-start space-x-2">
<span class="text-emerald-500 font-bold">•</span>
<span>Integrasi penuh dengan modul frontend dashboard audit utama.</span>
</li>
<li class="flex items-start space-x-2">
<span class="text-emerald-500 font-bold">•</span>
<span>Pelaksanaan Load Testing batas beban 10,000 transaksi per menit.</span>
</li>
</ul>
</div>

</div>

---
layout: center
class: text-center
---

<!-- SLIDE 7: Closing -->
<div class="flex flex-col items-center justify-center space-y-4">

<img src="/logo.png" class="h-24 object-contain bg-white p-4 rounded-2xl shadow-md border border-slate-200 mb-2" />

<h1 class="text-3xl font-extrabold text-slate-900 tracking-tight">Terima Kasih</h1>

<p class="text-slate-500 max-w-md text-xs leading-relaxed">
Laporan Progres AuditChain Gateway Protocol <br/> Silakan menyampaikan pertanyaan atau arahan lebih lanjut dari Manajemen.
</p>

<div class="pt-2 flex items-center space-x-3">
<span class="px-3.5 py-1.5 rounded-lg bg-white text-slate-700 text-xs font-semibold border border-slate-200 shadow-sm">
Sesi Tanya Jawab (Q&A)
</span>
<span class="px-3.5 py-1.5 rounded-lg bg-blue-50 text-[#00285d] text-xs font-semibold border border-blue-100 shadow-sm">
AuditChain Core Team
</span>
</div>

</div>
