---
layout: default
class: scenario-page
---

<div class="scenario-page-inner">
  <div class="scenario-header">
    <div>
      <div class="scenario-kicker"><span class="kicker-mark purple"></span>INTEGRITY LAYERS</div>
      <h1>Tidak semua status merah berarti masalah yang sama.</h1>
      <p class="scenario-lede">Satu klasifikasi yang tepat membuat hasil demo bisa ditindaklanjuti: pulihkan Gateway, periksa client, atau hentikan recovery.</p>
    </div>
    <div class="scenario-page-number">07 <span>/ 09</span></div>
  </div>

  <div class="layer-grid">
    <div class="layer-card layer-two">
      <div class="layer-number">02</div><div class="layer-title">LOCAL HASH</div><div class="layer-name">Gateway row berubah</div>
      <div class="layer-example"><code>metadata berubah<br />hash lama tertinggal</code></div>
      <div class="layer-result"><span class="result-dot red"></span><div><b>TAMPERED</b><small>Recovery utama</small></div></div>
    </div>
    <div class="layer-card layer-three">
      <div class="layer-number">03</div><div class="layer-title">AGENT SOURCE</div><div class="layer-name">Data live client drift</div>
      <div class="layer-example"><code>agent value ≠<br />latest client event</code></div>
      <div class="layer-result"><span class="result-dot amber"></span><div><b>MISMATCH</b><small>Periksa client</small></div></div>
    </div>
    <div class="layer-card layer-four">
      <div class="layer-number">04</div><div class="layer-title">FABRIC ANCHOR</div><div class="layer-name">Merkle / proof tidak cocok</div>
      <div class="layer-example"><code>merkle_root ≠<br />anchor Fabric</code></div>
      <div class="layer-result"><span class="result-dot purple"></span><div><b>FAIL-CLOSED</b><small>Negative recovery</small></div></div>
    </div>
  </div>

  <div class="layer-legend"><span class="legend-swatch red"></span><span>Recovery dapat memulihkan Layer 2 jika snapshot trusted tersedia.</span><span class="legend-swatch amber"></span><span>Recovery Gateway tidak menulis balik data operasional client.</span><span class="legend-swatch purple"></span><span>Anchor/proof rusak harus ditolak, bukan dipaksa pulih.</span></div>
</div>

<div class="scenario-footer"><span>AuditChain Gateway Protocol</span><span>LAYERED VERIFICATION</span></div>
