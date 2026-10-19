# Aturan Lettering

## Prinsip

- Artwork dibuat tanpa teks. Balon, caption, SFX, dan typesetting ditambahkan kemudian pada salinan kerja.
- Pertahankan teks sumber persis; jangan menerjemahkan, meringkas, memperbaiki, atau menambah teks tanpa persetujuan.
- Jangan menciptakan balon baru. Satu entri lettering harus ditautkan ke entri dialog/narasi sumber.

## Urutan baca dan penempatan

- Rancang aliran baca webtoon dari atas ke bawah; dalam satu panel, pertahankan urutan yang tidak ambigu.
- Hindari wajah, mata, tangan penting, focal action, dan detail plot.
- Catat anchor secara deskriptif (`top-left`, `upper-center`) dan gunakan koordinat relatif bila layout final tersedia.
- Ekor balon menunjuk speaker dengan jelas tanpa melintasi focal point.
- Caption narator dibedakan secara konsisten dari dialog dan pikiran.

## QA

- Cocokkan teks karakter demi karakter dengan `script.md`.
- Verifikasi speaker, urutan, kapitalisasi, tanda baca, dan style token.
- Uji keterbacaan pada lebar ponsel target yang kelak diputuskan.
- Simpan versi clean artwork dan lettered artwork secara terpisah.

## Kontrak entri lettering

```yaml
id: txt-ch001-p001-01
type: dialogue | narration | thought | sfx
speaker: character-id | narrator | none
text_exact: "teks sumber"
source_locator: "scene/beat/baris"
placement: "top-left"
style_token: "dialogue-default"
```

