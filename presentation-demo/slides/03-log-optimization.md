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

<!-- SLIDE: Optimasi Performa Log History -->
<div class="pt-2 pb-10">

<div class="mb-4">
<span class="text-xs font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-3 py-1 rounded-md border border-blue-100">Progress Report: Performa & Optimasi</span>
<h1 class="text-2xl font-black text-slate-900 mt-1.5">
Optimasi Beban Data & <i>Loading State</i>
</h1>
</div>

<p class="text-sm text-slate-600 leading-relaxed mb-4">
Untuk mencegah penurunan performa web (<i>lag/freeze</i>) akibat volume data log yang masif, kami mengimplementasikan <strong>strategi optimasi pengambilan data</strong>:
</p>

<div class="grid grid-cols-2 gap-6">

<div>
<ul class="space-y-4">
<li class="flex items-start gap-3">
<span class="w-6 h-6 rounded-full bg-blue-100 text-blue-700 flex items-center justify-center flex-shrink-0 mt-0.5 text-xs font-bold">1</span>
<div class="text-sm">
<span class="font-bold text-slate-800">Limitasi 10 Data Terbaru</span><br/>
<span class="text-slate-600 text-xs leading-relaxed">Meskipun berjalan terus-menerus, UI dibatasi hanya memuat 10 log paling aktual untuk efisiensi memori.</span>
</div>
</li>
<li class="flex items-start gap-3">
<span class="w-6 h-6 rounded-full bg-emerald-100 text-emerald-700 flex items-center justify-center flex-shrink-0 mt-0.5 text-xs font-bold">2</span>
<div class="text-sm">
<span class="font-bold text-slate-800">Indikator Loading Realistis</span><br/>
<span class="text-slate-600 text-xs leading-relaxed">Penambahan efek <i>loading state</i> saat memproses antrian data guna menginformasikan bahwa sistem sedang bekerja.</span>
</div>
</li>
<li class="flex items-start gap-3">
<span class="w-6 h-6 rounded-full bg-purple-100 text-purple-700 flex items-center justify-center flex-shrink-0 mt-0.5 text-xs font-bold">3</span>
<div class="text-sm">
<span class="font-bold text-slate-800">Menghindari Render Blocking</span><br/>
<span class="text-slate-600 text-xs leading-relaxed">Web aplikasi kini berjalan jauh lebih ringan dan mulus dalam me-<i>render</i> antarmuka dashboard.</span>
</div>
</li>
</ul>
</div>

<div class="bg-slate-50 p-3 rounded-xl border border-slate-200 shadow-sm relative flex flex-col justify-center">
<div class="absolute -top-3 -right-2 bg-emerald-600 text-white text-[10px] font-bold px-2 py-1 rounded border border-emerald-500 shadow-sm z-10">
UI PREVIEW
</div>
<div class="rounded-lg overflow-hidden border border-slate-200 bg-white">
<img src="/loading-logs.png" class="w-full object-contain max-h-[220px]" />
</div>
<p class="text-center text-[10px] text-slate-500 mt-2 font-mono">Simulasi loading data log pada Dashboard UI</p>
</div>

</div>

</div>
