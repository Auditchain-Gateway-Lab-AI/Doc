---
layout: default
class: scenario-page
---

<div class="scenario-page-inner">
  <div class="scenario-header">
    <div>
      <div class="scenario-kicker"><span class="kicker-mark"></span>BASELINE</div>
      <h1>Mulai dari event normal: setiap action punya jejaknya sendiri.</h1>
      <p class="scenario-lede">Sebelum membuat tamper, pastikan pipeline CDC, hashing, snapshot, dan anchoring sudah menghasilkan baseline yang bisa dipercaya.</p>
    </div>
    <div class="scenario-page-number">02 <span>/ 09</span></div>
  </div>

  <div class="event-columns">
    <div class="event-column event-insert">
      <div class="event-top"><span class="event-index">01</span><span class="event-action">INSERT</span></div>
      <div class="event-title">Record dibuat</div>
      <div class="event-code">INSERT INTO<br /><b>public.orders</b></div>
      <div class="event-expect"><span></span><div><b>Audit log baru</b><small>snapshot + hash + actor</small></div></div>
    </div>
    <div class="event-column event-update">
      <div class="event-top"><span class="event-index">02</span><span class="event-action">UPDATE</span></div>
      <div class="event-title">Record berubah</div>
      <div class="event-code">UPDATE<br /><b>public.orders</b></div>
      <div class="event-expect"><span></span><div><b>Audit log baru</b><small>state berikutnya, bukan overwrite</small></div></div>
    </div>
    <div class="event-column event-delete">
      <div class="event-top"><span class="event-index">03</span><span class="event-action">DELETE</span></div>
      <div class="event-title">Record dihapus</div>
      <div class="event-code">DELETE FROM<br /><b>public.orders</b></div>
      <div class="event-expect"><span></span><div><b>Audit log baru</b><small>bukti DELETE tetap ada</small></div></div>
    </div>
  </div>

  <div class="baseline-strip">
    <div class="baseline-step"><span>01</span><b>CDC</b><small>event diterima</small></div>
    <div class="baseline-line"></div>
    <div class="baseline-step"><span>02</span><b>HASH</b><small>isi dikunci</small></div>
    <div class="baseline-line"></div>
    <div class="baseline-step"><span>03</span><b>SNAPSHOT</b><small>status VERIFIED</small></div>
    <div class="baseline-line"></div>
    <div class="baseline-step"><span>04</span><b>ANCHOR</b><small>status ANCHORED</small></div>
  </div>

  <div class="scenario-note-bar"><span class="note-icon">✓</span><span>Baseline lulus jika verify manual mengembalikan <code>HTTP 200</code>, <code>status=success</code>, dan <code>is_valid=true</code>.</span></div>
</div>

<div class="scenario-footer"><span>AuditChain Gateway Protocol</span><span>BASELINE EVENTS</span></div>
