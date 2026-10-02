---
layout: default
class: scenario-page
---

<div class="scenario-page-inner">
  <div class="scenario-header">
    <div>
      <div class="scenario-kicker"><span class="kicker-mark green"></span>RECOVERY BOUNDARY</div>
      <h1>Recovery memulihkan bukti audit—bukan database client.</h1>
      <p class="scenario-lede">Batas ini harus terlihat jelas di presentasi agar recovery tidak disalahartikan sebagai rollback transaksi bisnis.</p>
    </div>
    <div class="scenario-page-number">05 <span>/ 09</span></div>
  </div>

  <div class="boundary-diagram">
    <div class="boundary-lane lane-gateway">
      <div class="boundary-label"><span class="boundary-dot blue"></span><b>GATEWAY / RECOVERY VAULT</b><small>yang disentuh recovery</small></div>
      <div class="boundary-track">
        <div class="boundary-box"><b>audit_logs</b><small>target log dikembalikan ke snapshot</small></div>
        <span class="boundary-arrow">→</span>
        <div class="boundary-box box-green"><b>VALID</b><small>hash + Merkle + anchor cocok</small></div>
        <span class="boundary-arrow">→</span>
        <div class="boundary-box box-amber"><b>recovery_events</b><small>bukti operasi recovery baru</small></div>
      </div>
    </div>
    <div class="boundary-lane lane-client">
      <div class="boundary-label"><span class="boundary-dot gray"></span><b>DATABASE OPERASIONAL CLIENT</b><small>tidak disentuh MVP</small></div>
      <div class="boundary-track">
        <div class="boundary-box"><b>public.orders</b><small>state bisnis tetap seperti kondisi terakhir</small></div>
        <span class="boundary-arrow muted">→</span>
        <div class="boundary-box box-gray"><b>DELETE tetap DELETE</b><small>row tidak otomatis dibuat kembali</small></div>
        <span class="boundary-arrow muted">→</span>
        <div class="boundary-box box-gray"><b>write-back terpisah</b><small>butuh adapter & izin eksplisit</small></div>
      </div>
    </div>
  </div>

  <div class="boundary-rule"><span class="rule-icon">!</span><span><b>Kalimat demo:</b> “Recovery mengembalikan integritas catatan AuditChain. Ia tidak meng-undo DELETE atau UPDATE pada database operasional client.”</span></div>
</div>

<div class="scenario-footer"><span>AuditChain Gateway Protocol</span><span>WHAT RECOVERY DOES / DOES NOT DO</span></div>
