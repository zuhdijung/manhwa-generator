# Tools — Batas v0.1

Versi 0.1 tidak memasang dependency, tidak memiliki automation runner, dan tidak melakukan panggilan API. Folder ini mendokumentasikan utilitas kecil yang mungkin ditambahkan setelah kontrak produksi stabil.

## Kandidat alat masa depan

- Validator Markdown/YAML metadata dan keunikan panel ID.
- Pemeriksa tautan relatif serta file referensi yang hilang.
- Generator manifest berdasarkan panel berstatus approved.
- Pemeriksa hash/version artwork agar file approved tidak tertimpa.
- Assembler vertikal lokal yang menjaga clean/lettered source.

Setiap alat harus default ke dry-run, dapat direproduksi, tidak membaca rahasia dari Git, dan meminta persetujuan eksplisit sebelum API berbayar atau overwrite. Pilihan bahasa/runtime belum diputuskan; lihat [open decisions](../docs/OPEN_DECISIONS.md).

