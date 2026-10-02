---
layout: default
class: scenario-page
---

<div class="scenario-page-inner">
  <div class="scenario-header">
    <div>
      <div class="scenario-kicker"><span class="kicker-mark red"></span>CORE LOOP</div>
      <h1>Satu siklus tamper–recovery yang bisa diulang.</h1>
      <p class="scenario-lede">Target utama adalah tamper Layer 2: field canonical diubah, tetapi hash dan snapshot lama tetap menjadi referensi.</p>
    </div>
    <div class="scenario-page-number">03 <span>/ 09</span></div>
  </div>

  <div class="cycle-flow">
    <div class="cycle-node node-event"><div class="cycle-index">01</div><div class="cycle-label">EVENT</div><b>INSERT / UPDATE / DELETE</b><small>Log sudah ANCHORED</small></div>
    <div class="cycle-connector"><span>→</span></div>
    <div class="cycle-node node-tamper"><div class="cycle-index">02</div><div class="cycle-label">TAMPER</div><b>metadata berubah</b><small>hash lama dibiarkan</small></div>
    <div class="cycle-connector"><span>→</span></div>
    <div class="cycle-node node-detect"><div class="cycle-index">03</div><div class="cycle-label">DETECT</div><b>verify / scanner</b><small>incident OPEN</small></div>
    <div class="cycle-connector"><span>→</span></div>
    <div class="cycle-node node-recover"><div class="cycle-index">04</div><div class="cycle-label">RECOVER</div><b>snapshot tervalidasi</b><small>preflight → execute</small></div>
    <div class="cycle-connector"><span>→</span></div>
    <div class="cycle-node node-valid"><div class="cycle-index">05</div><div class="cycle-label">VERIFY</div><b>isi kembali valid</b><small>incident RESOLVED</small></div>
  </div>

  <div class="cycle-proof-grid">
    <div class="proof-box proof-danger"><span class="proof-caption">INJEKSI TAMPER</span><code>UPDATE audit_logs<br />SET metadata = '{...}'</code><small>Jangan membuat hash baru.</small></div>
    <div class="proof-box proof-amber"><span class="proof-caption">PRECONDITION RECOVERY</span><code>snapshot_status = VERIFIED<br />status = ANCHORED</code><small>MinIO, Merkle, dan Fabric harus reachable.</small></div>
    <div class="proof-box proof-green"><span class="proof-caption">HASIL YANG DICARI</span><code>current_hash ≠ snapshot_hash<br />after_hash = snapshot_hash</code><small>Yang dipulihkan adalah audit log Gateway.</small></div>
  </div>
</div>

<div class="scenario-footer"><span>AuditChain Gateway Protocol</span><span>TAMPER → RECOVERY → VERIFY</span></div>
