# Doc

Folder ini dipakai untuk menyimpan source presentasi progress dan hasil laporan yang sudah dikunci.

## Workflow laporan progress

1. Edit materi terbaru di `presentation-demo`.
2. Export menjadi PDF:

   ```bash
   cd presentation-demo
   npm run export -- --output ../Progress_Agustus/Progress_Auditchain_Gateway-03-Agustus-2026.pdf
   ```

3. Commit/push PDF hasil export ke folder progress bulan berjalan, misalnya `Progress_Agustus`.

File di `presentation-demo` boleh terus berubah untuk progress berikutnya. PDF di folder progress menjadi arsip yang dikirim atau dilaporkan ke Gitea.
