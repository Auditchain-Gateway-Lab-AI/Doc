---
layout: default
class: scenario-page
---

<div class="scenario-page-inner">
  <div class="scenario-header">
    <div>
      <div class="scenario-kicker"><span class="kicker-mark amber"></span>SCENARIO MAP</div>
      <h1>Dari satu event sampai rangkaian yang saling berulang.</h1>
      <p class="scenario-lede">Matriks ini menjadi daftar kerja demo: mulai dari action tunggal, lanjut ke histori berantai, lalu uji recovery ulang.</p>
    </div>
    <div class="scenario-page-number">04 <span>/ 09</span></div>
  </div>

  <div class="matrix-wrap">
    <table class="scenario-matrix">
      <thead><tr><th>ID</th><th>Urutan</th><th>Target tamper</th><th>Recovery</th><th>Yang harus terlihat</th></tr></thead>
      <tbody>
        <tr><td><b>S1</b></td><td><span class="mini-pill blue">INSERT</span></td><td>metadata</td><td>1×</td><td>log INSERT kembali valid</td></tr>
        <tr><td><b>S2</b></td><td><span class="mini-pill purple">UPDATE</span></td><td>actor / metadata</td><td>1×</td><td>state update dipulihkan</td></tr>
        <tr><td><b>S3</b></td><td><span class="mini-pill red">DELETE</span></td><td>metadata</td><td>1×</td><td>bukti DELETE pulih; row client tetap hilang</td></tr>
        <tr class="row-highlight"><td><b>S4</b></td><td><span class="mini-pill blue">INSERT</span> → <span class="mini-pill purple">UPDATE</span> → <span class="mini-pill red">DELETE</span></td><td>log DELETE terakhir</td><td>1×</td><td>hanya target terakhir yang berubah</td></tr>
        <tr class="row-highlight"><td><b>S5</b></td><td>tamper → recovery → tamper lagi</td><td>log yang sama</td><td>2×</td><td>incident kedua OPEN setelah pertama RESOLVED</td></tr>
        <tr><td><b>S6</b></td><td>recovery → UPDATE baru</td><td>UPDATE baru</td><td>1×</td><td>latest client event tetap UPDATE baru</td></tr>
        <tr><td><b>S8</b></td><td>event apa pun</td><td>merkle_root</td><td>fail expected</td><td>fail-closed, bukan recovery sukses</td></tr>
      </tbody>
    </table>
  </div>

  <div class="matrix-callout"><span class="callout-line"></span><span><b>Urutan demo yang paling kuat:</b> S1 → S2 → S3 → S4 → S5 → S6. S8 dipakai terakhir sebagai negative test.</span></div>
</div>

<div class="scenario-footer"><span>AuditChain Gateway Protocol</span><span>SCENARIO MATRIX</span></div>
