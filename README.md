# Agent Skills

Koleksi skill AI berbasis `SKILL.md` untuk digunakan oleh agent yang kompatibel.

## Skills

- [Adaptive Form UX](skills/adaptive-form-ux/SKILL.md) — merancang layout form adaptif berdasarkan konten, grouping, media, ruang tersedia, dan perilaku responsif.
- [Hero Precision UI](skills/hero-precision-ui/SKILL.md) — rekonstruksi UI dari screenshot menjadi satu `index.html` menggunakan Tailwind CSS v4.
- [Precision UI Slicing](skills/precision-ui-slicing/SKILL.md) — panduan Native Pi untuk audit dan rekonstruksi UI screenshot secara responsif dan evidence-driven.
- [Vintage Paper Pack](skills/vintage-paper-pack/SKILL.md) — satu canvas landscape dengan lima ikon vintage monoline berjajar horizontal di atas satu background kertas bertekstur.

## Penggunaan

Buka `SKILL.md` skill yang diperlukan dan jalankan instruksinya dengan agent yang memiliki tool sesuai. Vintage Paper Pack membutuhkan image generation; skill UI tidak menyediakan tool pembuat gambar raster.

Adaptive Form UX dan Precision UI Slicing merujuk pada workflow internal Native Pi yang tidak disertakan dalam repo ini. Hero Precision UI mempertahankan skill sumber dengan perubahan nama frontmatter saja. Kedua skill slicing memiliki cakupan yang beririsan; pilih salah satunya sesuai prosedur yang diinginkan. Akurasi visual perlu diperiksa pada hasil render, bukan diasumsikan dari keberadaan skill.

Contoh: **"Bikinkan Vintage Paper Pack Halloween"**.
