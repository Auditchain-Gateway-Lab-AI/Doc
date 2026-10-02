---
layout: default
class: scenario-page
---

<div class="scenario-page-inner">
  <div class="scenario-header">
    <div>
      <div class="scenario-kicker"><span class="kicker-mark red"></span>REPEATABILITY</div>
      <h1>Setelah pulih, log yang sama masih bisa diuji lagi.</h1>
      <p class="scenario-lede">Recovery bukan penghapusan sejarah. Ia menutup incident, menyimpan bukti, dan menjaga snapshot terpercaya untuk siklus berikutnya.</p>
    </div>
    <div class="scenario-page-number">06 <span>/ 09</span></div>
  </div>

  <div class="repeat-timeline">
    <div class="repeat-cycle first-cycle">
      <div class="repeat-heading"><span>CYCLE 01</span><b>FIRST INCIDENT</b></div>
      <div class="repeat-steps"><div class="repeat-step rs-red"><b>TAMPER</b><small>incident OPEN</small></div><span>→</span><div class="repeat-step rs-amber"><b>RECOVERY</b><small>request SUCCEEDED</small></div><span>→</span><div class="repeat-step rs-green"><b>RESOLVED</b><small>bukti tetap ada</small></div></div>
    </div>
    <div class="repeat-down">↓</div>
    <div class="repeat-cycle second-cycle">
      <div class="repeat-heading"><span>CYCLE 02</span><b>SAME LOG, NEW INCIDENT</b></div>
      <div class="repeat-steps"><div class="repeat-step rs-red"><b>TAMPER LAGI</b><small>incident baru OPEN</small></div><span>→</span><div class="repeat-step rs-amber"><b>RECOVERY LAGI</b><small>trusted lineage</small></div><span>→</span><div class="repeat-step rs-green"><b>RESOLVED</b><small>dua recovery events</small></div></div>
    </div>
  </div>

  <div class="repeat-bottom"><div><span class="bottom-tag">THEN</span><b>UPDATE BARU</b><small>event client terbaru, bukan recovery event</small></div><div class="bottom-arrow">→</div><div><span class="bottom-tag tag-red">TEST AGAIN</span><b>TAMPER UPDATE</b><small>target recovery berpindah ke log baru</small></div></div>
</div>

<div class="scenario-footer"><span>AuditChain Gateway Protocol</span><span>REPEAT TAMPER / RECOVERY</span></div>
