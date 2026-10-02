---
layout: default
class: scenario-page
---

<div class="scenario-page-inner">
  <div class="scenario-header">
    <div>
      <div class="scenario-kicker"><span class="kicker-mark"></span>THE TESTING QUESTION</div>
      <h1>Yang diuji bukan hanya log masuk.</h1>
      <p class="scenario-lede">Kita ingin melihat apakah AuditChain tetap bisa menjelaskan <strong>apa yang berubah, kapan terdeteksi, dan apa yang dipulihkan</strong> setelah data audit dirusak.</p>
    </div>
    <div class="scenario-page-number">01 <span>/ 09</span></div>
  </div>

  <div class="question-grid">
    <div class="question-statement">
      <div class="statement-label">CLAIM</div>
      <div class="statement-title">Setiap perubahan harus punya status yang jelas.</div>
      <div class="statement-copy">Event normal, tamper Gateway, mismatch data client, dan recovery tidak boleh terbaca sebagai satu jenis kejadian.</div>
    </div>
    <div class="question-lanes">
      <div class="question-lane lane-normal">
        <div class="lane-dot"></div>
        <div><span class="lane-label">NORMAL EVENT</span><strong>INSERT / UPDATE / DELETE</strong><small>Ditangkap CDC dan dibuatkan audit log baru.</small></div>
      </div>
      <div class="question-lane lane-tamper">
        <div class="lane-dot"></div>
        <div><span class="lane-label">INTEGRITY FAILURE</span><strong>HASH / MERKLE MISMATCH</strong><small>Isi log atau bukti kriptografi tidak lagi cocok.</small></div>
      </div>
      <div class="question-lane lane-recovery">
        <div class="lane-dot"></div>
        <div><span class="lane-label">RECOVERY EVIDENCE</span><strong>RESTORE + FORENSICS</strong><small>Log dipulihkan, incident diselesaikan, bukti tetap disimpan.</small></div>
      </div>
    </div>
  </div>

  <div class="scenario-note-bar"><span class="note-icon">i</span><span>Aturan dasar: perubahan normal di database client adalah event baru; tamper utama dibuat dengan mengubah <code>audit_logs</code> Gateway setelah log berstatus <code>ANCHORED</code>.</span></div>
</div>

<div class="scenario-footer"><span>AuditChain Gateway Protocol</span><span>SCENARIO TESTING 1</span></div>
