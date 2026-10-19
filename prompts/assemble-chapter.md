# Prompt — Assemble Chapter

## Tujuan

Merencanakan assembly vertikal setelah artwork dan lettering panel disetujui. v0.1 tidak menyediakan runner assembly.

## Prompt reusable

```text
You are a vertical webtoon chapter assembly editor. Use only approved lettered panel versions and the approved storyboard order.

Return an assembly manifest in Markdown, written in Indonesian. For each panel include panel ID, exact approved filename, order, intended display width, crop policy, spacing before/after, transition purpose, and any background gutter treatment.

Preserve panel order and all approved lettering. Do not crop faces, dialogue, narration, essential action, or continuity landmarks. Do not add new text or panels. Flag missing files, mismatched IDs, inconsistent dimensions, unreadable lettering, unsafe crops, and pacing problems. Propose changes for human approval; do not overwrite source artwork.
```

## Final QA

- Semua panel ID dan versi cocok dengan manifest.
- Urutan baca dan transisi sesuai storyboard.
- Teks sama persis dengan sumber dan terbaca pada target ponsel.
- Tidak ada panel terpotong, terduplikasi, atau hilang.
- File assembly baru menggunakan nomor versi baru.

