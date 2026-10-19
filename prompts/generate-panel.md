# Prompt — Generate Panel

## Tujuan

Template instruksi untuk menghasilkan satu clean artwork setelah spesifikasi panel disetujui. v0.1 tidak menjalankan prompt ini secara otomatis.

## Prompt compiler contract

Gabungkan hanya data approved dengan urutan berikut:

```text
[SUBJECT AND ACTION]
[APPROVED CHARACTER APPEARANCE AND CURRENT CONTINUITY]
[LOCATION AND ENVIRONMENT]
[CAMERA, POV, COMPOSITION, AND DEPTH]
[EMOTION AND ATMOSPHERE]
[LIGHTING, PALETTE, AND MATERIAL DETAIL]
Premium original Korean webtoon illustration, semi-realistic anime proportions, cinematic visual storytelling, vertical panel composition.
[LETTERING SAFE SPACE]
No text, no speech bubbles, no captions, no watermark, no logo.
```

Tulisan di dalam prompt artwork harus bahasa Inggris. Dialog tidak dimasukkan ke artwork prompt; ia tetap berada di kontrak lettering dalam bahasa sumber.

## Preflight wajib

- Panel ID valid dan unik.
- Script, karakter, lokasi, storyboard, dan panel spec terkait berstatus approved.
- Semua detail visual dapat dilacak atau diberi label proposal yang telah disetujui.
- Continuity cocok dengan panel sebelumnya.
- Prompt dan negative prompt telah ditinjau.
- Provider/model, ukuran, seed strategy, dan budget telah dipilih manusia.
- Persetujuan eksplisit untuk biaya API telah tercatat.

Jika salah satu syarat gagal, hentikan generasi dan laporkan kekurangannya.

