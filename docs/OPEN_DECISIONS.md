# Open Decisions

Keputusan berikut sengaja belum diambil pada bootstrap. Pemilik proyek perlu menetapkannya sebelum pipeline produksi penuh.

| ID | Keputusan | Mengapa diperlukan | Default sementara | Status |
|---|---|---|---|---|
| OD-001 | Provider/model image generation | Menentukan syntax prompt, seed, kualitas, dan biaya | Tidak ada panggilan | open |
| OD-002 | Resolusi dan rasio panel kerja | Memengaruhi framing, detail, dan assembly | Aspect intent per panel | open |
| OD-003 | Lebar final webtoon dan batas panjang file | Memengaruhi lettering serta slice export | Belum ditentukan | open |
| OD-004 | Font dan lisensi lettering | Harus aman untuk distribusi | Belum dipilih | open |
| OD-005 | Kebijakan bahasa/terjemahan | Menentukan apakah ada versi teks terpisah | Pertahankan bahasa sumber | open |
| OD-006 | Versioning aset final/Git LFS | Output gambar kini diabaikan Git | Simpan lokal, source Markdown di Git | open |
| OD-007 | Format gambar dan color profile | Memengaruhi kualitas/ukuran file | Belum ditentukan | open |
| OD-008 | Strategi seed/reference/identity | Memengaruhi konsistensi karakter | Manual dan provider-agnostic | open |
| OD-009 | Budget per panel/chapter | Diperlukan sebelum API berbayar | Nol pada bootstrap | open |
| OD-010 | Runtime validator/assembler | Menentukan tooling versi berikutnya | Tidak ada dependency | open |
| OD-011 | Siapa yang berwenang memberi approval | Menentukan audit trail status | Pemilik proyek | open |

## Format keputusan baru

Tambahkan baris dengan ID stabil. Ketika diputuskan, ubah status menjadi `decided`, tulis tanggal/otoritas, dan tautkan dokumen konfigurasi yang diperbarui. Jangan menghapus riwayat keputusan.

