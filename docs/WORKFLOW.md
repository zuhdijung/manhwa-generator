# Workflow Produksi v0.1

## Alur utama

```text
Naskah asli
  → analisis faktual
  → character/world bible
  → storyboard
  → spesifikasi panel
  → prompt preflight
  → generasi kandidat (manual, di luar v0.1)
  → QA dan approval artwork
  → lettering
  → assembly vertikal
  → final QA
```

## 1. Ingest naskah — Checkpoint A

Salin naskah ke `chapters/<chapter>/script.md` tanpa penyuntingan. Isi metadata sumber dan versi. Analisis dengan `prompts/analyze-script.md`, lalu manusia memverifikasi fakta serta inventaris dialog/narasi. Perubahan adaptasi dicatat sebagai proposal terpisah.

**Keluar ketika:** naskah dan analisis telah diterima; dialog/narasi memiliki locator.

## 2. Kunci canon visual — Checkpoint B

Buat character sheet dari template dan lengkapi world/location bible hanya dari sumber. Pertanyaan visual yang belum dijawab masuk ke `OPEN_DECISIONS.md`; alternatif kreatif bertanda `PROPOSAL`.

**Keluar ketika:** desain yang akan tampak pada chapter dan lokasi relevan berstatus approved.

## 3. Storyboard — Checkpoint C

Gunakan `prompts/generate-storyboard.md`. Pecah scene menjadi beat visual, berikan ID panel stabil, petakan semua teks persis ke panel, rancang kamera, blocking, continuity, ruang lettering, dan ritme vertikal. Review perubahan urutan atau staging sebelum lanjut.

**Keluar ketika:** urutan panel, teks, continuity, dan pacing disetujui.

## 4. Spesifikasi panel — Checkpoint D

Buat `panels/panel-NNN.md` per baris storyboard mengikuti kontrak di `config/panel-rules.md`. Susun prompt visual Inggris dari data approved, tanpa memasukkan dialog ke gambar. Review panel murah lebih dulu: komposisi, continuity, dan acceptance criteria sebelum memilih model atau resolusi.

**Keluar ketika:** panel spec/prompt approved dan budget/provider disetujui secara eksplisit.

## 5. Generasi dan seleksi — Checkpoint E

Tahap ini manual dan **tidak diimplementasikan pada v0.1**. Jika kelak dijalankan, mulai dengan kandidat berbiaya rendah untuk validasi komposisi, lalu gunakan kualitas tinggi hanya untuk kandidat terpilih. Simpan versi baru; jangan menimpa artwork approved. Review memakai `prompts/review-panel.md`.

**Keluar ketika:** satu clean artwork per panel dipilih manusia dan versinya dicatat.

## 6. Lettering — Checkpoint F

Kerjakan pada salinan clean artwork. Ambil teks persis dari script melalui mapping storyboard. Terapkan `config/lettering-rules.md`, lalu periksa speaker, urutan baca, placement, dan keterbacaan ponsel.

**Keluar ketika:** seluruh panel lettered approved dan clean source tetap tersimpan.

## 7. Assembly dan final QA

Buat manifest memakai `prompts/assemble-chapter.md`; susun hanya versi panel approved. Periksa order, spacing, crop, transisi, duplikasi, file hilang, konsistensi warna, dan teks. Assembly memakai nama versi baru.

## Strategi Git

- Satu perubahan logis per commit; commit tetap dilakukan manusia.
- Tinjau diff Markdown sebelum approval.
- Jangan commit `.env`, token, output sementara, atau kandidat gambar yang tidak diperlukan.
- Jika aset final kelak masuk Git, putuskan Git LFS dan ubah `.gitignore` secara eksplisit.

## Definition of done untuk satu panel

- ID unik dan tertaut dari storyboard.
- Semua field minimum lengkap dan dapat dilacak ke sumber.
- Dialog/narasi cocok persis atau `none`.
- Continuity in/out konsisten.
- Clean artwork dan lettered artwork terpisah.
- QA selesai dan approval manusia tercatat.

