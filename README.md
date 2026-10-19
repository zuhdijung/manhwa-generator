# Manhwa Production Studio v0.1

Repository Markdown-first untuk mengubah naskah menjadi storyboard, spesifikasi panel, artwork terpilih, lettering, lalu chapter webtoon vertikal. Versi 0.1 berfokus pada kontrak produksi yang dapat ditinjau dan dilacak melalui Git; belum ada generator gambar atau aplikasi.

## Mulai cepat

1. Baca [workflow produksi](docs/WORKFLOW.md) dan [keputusan terbuka](docs/OPEN_DECISIONS.md).
2. Tempel naskah tanpa mengubah isinya ke `chapters/<chapter>/script.md`.
3. Definisikan karakter memakai [template karakter](characters/templates/character-template.md), lalu minta persetujuan canon.
4. Lengkapi dunia dan lokasi di [world-building](world/world-building.md) serta [locations](world/locations.md).
5. Susun storyboard dengan [prompt analisis](prompts/analyze-script.md) dan [prompt storyboard](prompts/generate-storyboard.md).
6. Buat satu berkas per panel berdasarkan contoh `chapters/chapter-001/panels/panel-001.md`.
7. Jalankan review manusia sebelum generasi, seleksi artwork, lettering, dan assembly.

## Peta repository

| Path | Fungsi |
|---|---|
| `config/` | Identitas visual serta aturan storytelling, panel, dan lettering |
| `characters/` | Sumber kebenaran desain dan kontinuitas karakter |
| `world/` | Canon dunia dan kamus lokasi |
| `chapters/` | Naskah, storyboard, spesifikasi panel, dan output per chapter |
| `prompts/` | Prompt kerja reusable; prompt visual berbahasa Inggris |
| `tools/` | Kontrak alat yang boleh ditambahkan pada versi berikutnya |
| `docs/` | Workflow dan keputusan produksi lintas chapter |

## Prinsip data

- ID panel tidak berubah walau urutan produksi atau layout direvisi.
- Artwork tanpa teks dan lettering merupakan artefak terpisah.
- Semua detail baru yang belum disetujui harus bertanda `PROPOSAL`.
- Output gambar diabaikan Git secara default untuk menghindari file besar dan overwrite tidak disengaja.
- Tidak ada rahasia atau credential yang boleh masuk repository.

