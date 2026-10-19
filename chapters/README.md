# Produksi Chapter

Setiap chapter memakai folder `chapter-NNN/` dengan kontrak berikut:

```text
chapter-NNN/
├── script.md       # naskah asli/canon, tidak diedit tanpa approval
├── storyboard.md   # breakdown scene, beat, dan urutan panel
├── panels/         # satu spesifikasi per panel
└── output/         # artwork lokal; diabaikan Git kecuali .gitkeep
```

## Siklus status

`draft` → `in-review` → `approved` → `locked`

`needs-revision` dapat digunakan dari tahap review. Hanya manusia yang memberi status `approved` atau `locked`. Storyboard tidak boleh masuk generasi sebelum script dan referensi canon relevan disetujui.

## Penamaan output

- Clean artwork: `chNNN-pNNN_art_vNN.ext`
- Lettered panel: `chNNN-pNNN_lettered_vNN.ext`
- Chapter assembly: `chNNN_assembled_vNN.ext`

Catat file terpilih pada spesifikasi panel; jangan mengandalkan nama `final-final`.

