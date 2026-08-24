---
layout: two-cols
transition: slide-left
class: pt-2 pb-10
---

<!-- Footer -->
<div class="absolute bottom-6 left-10 flex items-center space-x-2 text-xs text-slate-500 font-semibold z-50">
<span class="w-2 h-2 rounded-full bg-[#00285d]"></span>
<span>AuditChain Gateway Protocol</span>
</div>
<div class="absolute bottom-6 right-10 text-xs text-slate-400 font-mono z-50">
Sprint 2026
</div>

<!-- Header (spans both columns visually if we adjust, but in two-cols it's in left by default. Let's keep it compact) -->
<div class="mb-6 pr-4">
  <span class="text-xs font-bold uppercase tracking-wider text-[#00285d] bg-blue-50 px-3 py-1 rounded-md border border-blue-100">Progress Report: DevOps</span>
  <h1 class="text-2xl font-black text-slate-900 mt-2">
    Automasi Deployment Dev Server
  </h1>
  <p class="text-xs text-slate-600 mt-2 leading-relaxed">
    Pipeline CI/CD menggunakan GitHub Actions untuk deployment otomatis ke server dev Besu.
  </p>
</div>

<!-- Left Column: Key Features -->
<div class="space-y-3 pr-4">
  <div class="bg-slate-50 p-3 rounded-xl border border-slate-200 shadow-sm flex items-start gap-3">
    <div class="text-2xl">🚀</div>
    <div>
      <h3 class="text-sm font-bold text-slate-800">Automasi via Actions</h3>
      <p class="text-[10px] text-slate-600 mt-1">Merge ke branch <code class="text-indigo-600 font-bold bg-indigo-50 px-1 rounded">dev</code> otomatis memicu workflow deployment.</p>
    </div>
  </div>
  
  <div class="bg-slate-50 p-3 rounded-xl border border-slate-200 shadow-sm flex items-start gap-3">
    <div class="text-2xl">🐳</div>
    <div>
      <h3 class="text-sm font-bold text-slate-800">Docker Fleksibel</h3>
      <p class="text-[10px] text-slate-600 mt-1">Fallback otomatis antara <code class="text-emerald-600 font-bold bg-emerald-50 px-1 rounded">docker compose</code> dan versi lama.</p>
    </div>
  </div>

  <div class="bg-slate-50 p-3 rounded-xl border border-slate-200 shadow-sm flex items-start gap-3">
    <div class="text-2xl">🔐</div>
    <div>
      <h3 class="text-sm font-bold text-slate-800">Keamanan Credentials</h3>
      <p class="text-[10px] text-slate-600 mt-1">Menggunakan GitHub Repository Secrets untuk menyimpan SSH Key.</p>
    </div>
  </div>
</div>

::right::

<div class="mt-4 ml-4">
  <span class="text-[10px] font-bold uppercase tracking-wider text-slate-500 mb-2 bg-slate-100 px-3 py-1 rounded-md block text-center w-max mx-auto">Alur Deployment (CI/CD Flow)</span>
</div>

```mermaid {class: 'overflow-auto max-h-[360px] ml-4 mt-2 bg-white p-4 rounded-xl border border-slate-200 shadow-sm custom-scrollbar'}
flowchart TD
    A[Feature Branch] -->|Merge PR| B(Branch dev)
    B -->|Trigger Workflow| C{GitHub Actions}
    C -->|SSH Login| D[Server Dev]
    D -->|git pull| E[Update Code]
    E -->|docker up| F((Updated))
    
    style A fill:#f1f5f9,stroke:#94a3b8
    style B fill:#e0e7ff,stroke:#6366f1,stroke-width:2px
    style C fill:#dcfce7,stroke:#22c55e
    style D fill:#fef3c7,stroke:#f59e0b
    style E fill:#f1f5f9,stroke:#94a3b8
    style F fill:#cffafe,stroke:#06b6d4,stroke-width:2px
```

<style>
.custom-scrollbar::-webkit-scrollbar {
  width: 6px;
  height: 6px;
}
.custom-scrollbar::-webkit-scrollbar-track {
  background: #f1f5f9;
  border-radius: 4px;
}
.custom-scrollbar::-webkit-scrollbar-thumb {
  background: #cbd5e1;
  border-radius: 4px;
}
.custom-scrollbar::-webkit-scrollbar-thumb:hover {
  background: #94a3b8;
}
</style>
