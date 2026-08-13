---
layout: default
transition: slide-up
class: "!py-5 !px-10 soft-grid"
---

<div class="deck-footer">
  <span>AuditChain Gateway Simulation</span>
  <span>05 / Log Result</span>
</div>

<span class="kicker">Audit Log</span>
<h1 class="text-[34px] leading-tight font-extrabold text-slate-950 mt-3">
  Semua event tetap muncul, termasuk actor yang tidak dikenal.
</h1>

<div class="mt-8 narrative-card p-5">
  <table class="mini-log">
    <thead>
      <tr>
        <th>Time</th>
        <th>Actor</th>
        <th>Table</th>
        <th>Action</th>
        <th>Status</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>09:14</td>
        <td>rina</td>
        <td>invoice</td>
        <td>INSERT</td>
        <td><span class="tag-ok">normal</span></td>
      </tr>
      <tr>
        <td>10:03</td>
        <td>budi</td>
        <td>payment</td>
        <td>UPDATE</td>
        <td><span class="tag-ok">normal</span></td>
      </tr>
      <tr>
        <td>02:18</td>
        <td>unknown_session</td>
        <td>customer</td>
        <td>DELETE</td>
        <td><span class="tag-danger">anomaly</span></td>
      </tr>
      <tr>
        <td>02:19</td>
        <td>root_db</td>
        <td>invoice</td>
        <td>UPDATE</td>
        <td><span class="tag-danger">anomaly</span></td>
      </tr>
    </tbody>
  </table>
</div>

<div class="grid grid-cols-3 gap-4 mt-5">
  <div class="tag-ok justify-center">registered user</div>
  <div class="tag-warn justify-center">service actor</div>
  <div class="tag-danger justify-center">unknown actor</div>
</div>
