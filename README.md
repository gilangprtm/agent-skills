# Agent Skills

Koleksi skill AI berbasis `SKILL.md` untuk digunakan oleh agent yang kompatibel.

## Skills

- [Asset Batch](skills/asset-batch/SKILL.md) — membuat banyak aset gambar dengan satu file independen per aset, bukan sprite sheet atau kolase.

- [Adaptive Form UX](skills/adaptive-form-ux/SKILL.md) — merancang layout form adaptif berdasarkan konten, grouping, media, ruang tersedia, dan perilaku responsif.
- [UI Asset Generator](skills/ui-asset-generator/SKILL.md) — membuat aset gambar raster dari screenshot UI melalui image generation dan iterasi visual.
- [Hero Precision UI](skills/hero-precision-ui/SKILL.md) — rekonstruksi UI dari screenshot menjadi satu `index.html` menggunakan Tailwind CSS v4.
- [Precision UI Slicing](skills/precision-ui-slicing/SKILL.md) — panduan Native Pi untuk audit dan rekonstruksi UI screenshot secara responsif dan evidence-driven.
- [Vintage Paper Pack](skills/vintage-paper-pack/SKILL.md) — satu canvas landscape dengan lima ikon vintage monoline berjajar horizontal di atas satu background kertas bertekstur.
- [Vintage Illustration Card](skills/vintage-illustration-card/SKILL.md) — satu ilustrasi vintage berwarna pada canvas 1:1, objek terpusat dengan margin lega dan tanpa ornamen mengambang.

## Penggunaan

Buka `SKILL.md` skill yang diperlukan dan jalankan instruksinya dengan agent yang memiliki tool sesuai. Vintage Paper Pack dan UI Asset Generator membutuhkan image generation; skill slicing UI lainnya tidak menyediakan tool pembuat gambar raster.

Adaptive Form UX dan Precision UI Slicing merujuk pada workflow internal Native Pi yang tidak disertakan dalam repo ini. Hero Precision UI mempertahankan skill sumber dengan perubahan nama frontmatter saja. Kedua skill slicing memiliki cakupan yang beririsan; pilih salah satunya sesuai prosedur yang diinginkan. Akurasi visual perlu diperiksa pada hasil render, bukan diasumsikan dari keberadaan skill.

Contoh: **"Bikinkan Vintage Paper Pack Halloween"**.
