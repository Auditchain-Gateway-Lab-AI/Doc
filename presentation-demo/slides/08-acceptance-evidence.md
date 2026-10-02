---
layout: default
class: scenario-page
---

<div class="scenario-page-inner">
  <div class="scenario-header">
    <div>
      <div class="scenario-kicker"><span class="kicker-mark green"></span>ACCEPTANCE EVIDENCE</div>
      <h1>Bukti lulus bukan hanya screenshot status hijau.</h1>
      <p class="scenario-lede">Setiap skenario harus menyimpan identitas log, hash sebelum/sesudah, incident, request, dan recovery event.</p>
    </div>
    <div class="scenario-page-number">08 <span>/ 09</span></div>
  </div>

  <div class="evidence-grid">
    <div class="evidence-checklist">
      <div class="evidence-heading">PASS GATE</div>
      <div class="evidence-item"><span>01</span><b>Event normal terbukti</b><small>INSERT, UPDATE, DELETE muncul sebagai log terpisah.</small></div>
      <div class="evidence-item"><span>02</span><b>Tamper terdeteksi</b><small>Incident OPEN dan layer penyebab sesuai.</small></div>
      <div class="evidence-item"><span>03</span><b>Recovery tervalidasi</b><small>Preflight VALID, request SUCCEEDED.</small></div>
      <div class="evidence-item"><span>04</span><b>Histori tetap utuh</b><small>Incident RESOLVED; bukti tampered tidak dihapus.</small></div>
      <div class="evidence-item"><span>05</span><b>Repeat cycle lulus</b><small>Log yang sama bisa diuji kembali.</small></div>
    </div>
    <div class="evidence-record">
      <div class="evidence-heading">EVIDENCE RECORD</div>
      <div class="record-row"><span>scenario_id</span><b>S5</b></div>
      <div class="record-row"><span>target_log_id</span><b class="mono">&lt;LOG_ID&gt;</b></div>
      <div class="record-row"><span>original_hash</span><b class="mono">&lt;HASH_BEFORE&gt;</b></div>
      <div class="record-row"><span>current_hash</span><b class="mono danger-text">&lt;HASH_TAMPERED&gt;</b></div>
      <div class="record-row"><span>recovery_request</span><b class="mono">SUCCEEDED</b></div>
      <div class="record-row"><span>final_hash</span><b class="mono green-text">&lt;HASH_AFTER&gt;</b></div>
      <div class="record-row"><span>incident</span><b class="status-pair"><i>OPEN</i> → <em>RESOLVED</em></b></div>
    </div>
  </div>

  <div class="evidence-footer-callout"><span class="callout-line green-line"></span><span><b>Output yang disimpan:</b> screenshot Dashboard, response API, query baseline, incident ID, request ID, recovery event ID, dan hash sebelum/sesudah.</span></div>
</div>

<div class="scenario-footer"><span>AuditChain Gateway Protocol</span><span>PASS / FAIL EVIDENCE</span></div>
