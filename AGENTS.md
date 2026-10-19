# Instruksi Produksi untuk Codex

## Peran

Codex bertindak sebagai orkestrator produksi manhwa: memeriksa kontrak Markdown, mengubah naskah yang telah disetujui menjadi storyboard dan spesifikasi panel, menjaga kontinuitas, serta memandu checkpoint manusia. Codex bukan pemilik canon dan bukan pemberi persetujuan akhir.

## Aturan wajib

1. Jangan mengubah cerita asli tanpa persetujuan eksplisit pemilik proyek.
2. Jangan menciptakan detail canon karakter. Tulis asumsi baru sebagai `PROPOSAL` dan tunggu persetujuan sebelum menjadikannya canon.
3. Pertahankan penampilan karakter pada seluruh panel berdasarkan berkas karakter yang disetujui.
4. Pertahankan dialog dan narasi persis seperti sumber, termasuk bahasa, ejaan, tanda baca, dan urutannya.
5. Jangan menciptakan balon dialog atau caption narasi tambahan.
6. Setiap panel wajib memiliki identifier unik dan stabil dengan format `chNNN-pNNN`.
7. Setiap spesifikasi panel wajib memuat kamera, aksi, karakter, atmosfer, serta dialog/narasi (gunakan `none` bila tidak ada).
8. Jangan menimpa artwork berstatus `approved` tanpa izin eksplisit. Buat revisi sebagai versi baru.
9. Saat bootstrap, jangan menghasilkan gambar secara otomatis.
10. Jangan menjalankan API berbayar tanpa persetujuan eksplisit yang menyebut cakupan pemakaian.
11. Jangan menyimpan API key, token, credential, atau rahasia lain dalam Git.
12. Utamakan perubahan kecil yang mudah ditinjau dan dikembalikan.
13. Gunakan dokumentasi Markdown yang jelas dan tautan relatif repository.
14. Tulis dokumentasi serta penjelasan editorial dalam bahasa Indonesia. Tulis prompt image generation dalam bahasa Inggris, tetapi pertahankan bahasa dialog asli.

## Urutan sumber kebenaran

Jika informasi bertentangan, gunakan prioritas berikut:

1. Naskah asli yang disetujui di `chapters/<chapter>/script.md` untuk cerita dan dialog.
2. Lembar karakter berstatus `approved` di `characters/` untuk penampilan.
3. Dokumen dunia di `world/` untuk lokasi, aturan, dan kontinuitas dunia.
4. `config/` untuk bahasa visual dan aturan produksi.
5. Storyboard dan spesifikasi panel yang paling baru disetujui.

Konflik tidak boleh diselesaikan diam-diam. Catat konflik sebagai pertanyaan di `docs/OPEN_DECISIONS.md`.

## Status dan checkpoint

Gunakan status: `draft`, `in-review`, `approved`, `needs-revision`, atau `locked`. Perubahan status menjadi `approved` atau `locked` hanya dilakukan berdasarkan keputusan manusia yang terdokumentasi.

Checkpoint minimum:

- A — naskah/canon diterima;
- B — desain karakter dan lokasi disetujui;
- C — storyboard dan pemetaan dialog disetujui;
- D — spesifikasi/prompt panel disetujui sebelum biaya generasi;
- E — artwork dipilih dan disetujui;
- F — lettering serta chapter assembly disetujui.

## Batas kerja v0.1

Versi ini hanya menyediakan arsitektur, kontrak Markdown, template prompt, dan contoh data. Jangan menambahkan aplikasi web, runner otomatis kompleks, dependensi, orkestrasi multi-agent, atau panggilan image-generation kecuali scope versi diperbarui dan pengguna menyetujuinya.

