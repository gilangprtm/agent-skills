---
name: adaptive-form-ux
description: Use in Native Pi to inspect, design, implement, or review adaptive forms and data-entry layouts based on content, grouping, available space, and responsive behavior.
---
# Adaptive Form UX

> **Runtime status: PUBLISHED — Owner approved publication on 2026-10-21.** Skill ini adalah panduan UX internal, bukan authority, approval, atau izin mengubah project.

## Tujuan
Membantu Native Pi menghasilkan form yang jelas, efisien, responsif, dan berorientasi pada kebutuhan data—bukan memakai grid dua kolom seragam sebagai default.

## Use When
- Form memiliki field dengan kebutuhan lebar yang berbeda.
- Foto/avatar, preview, upload, atau panel pendamping perlu ditata bersama data utama.
- Screenshot atau review menunjukkan ruang kosong, alignment buruk, field terlalu sempit/lebar, atau grouping yang tidak jelas.
- Form perlu beradaptasi terhadap ukuran viewport/container, label/value panjang, error, atau helper text.

## Do Not Use When
- Task tidak menyentuh form atau data-entry layout.
- Perbaikan memerlukan keputusan product/domain yang belum ditetapkan, misalnya mengubah field wajib, urutan proses bisnis, atau makna data.
- Target repository, scope, atau authorization tidak jelas.

## Input
Gunakan form atau screenshot yang ditinjau, struktur/container yang tersedia, masalah UX yang diminta, dan batasan visual atau perilaku yang diketahui. Perlakukan screenshot sebagai bukti tampilan pada kondisi tertentu; jangan menyimpulkan behavior source yang tidak terlihat.

## Prinsip Desain

### 1. Audit layout yang ada dahulu
- Periksa struktur form, parent/container constraints, komponen field, styling/token, urutan DOM/focus, validasi, helper text, upload/preview, serta screenshot/viewport yang tersedia.
- Bedakan masalah komposisi dari masalah data/model atau behavior.
- Jangan mengubah business logic, field, aturan validasi, atau urutan proses demi merapikan layout kecuali memang termasuk scope.

### 2. Layout mengikuti konten
- Jangan memakai `grid-cols-2` atau kolom sama lebar sebagai default untuk semua form.
- Tentukan lebar dan span berdasarkan panjang label/nilai, tipe kontrol, pesan helper/error, dan relasi field.
- Field yang secara makna terkait boleh berbagi baris bila ruang cukup; misalnya tempat lahir dan tanggal lahir.
- Field panjang seperti nama lengkap/alamat dapat mengambil ruang lebih besar; field pendek seperti kode/tahun/pilihan dapat lebih ringkas bila mudah dibaca dan digunakan.
- Gunakan komposisi seimbang, bukan memaksa semua baris terisi atau menghilangkan seluruh whitespace.
- Jangan memperlebar field singkat tanpa manfaat hanya untuk memenuhi viewport.

### 3. Foto atau media pendamping
- Bila foto penting untuk mengidentifikasi record, pertimbangkan preview yang cukup besar dan jelas di sisi data utama pada viewport lebar.
- Kelompokkan preview, pilih/ganti file, hapus, batas format/ukuran, dan feedback validasi sebagai satu unit yang mudah dipahami.
- Pilih proporsi area media dan data berdasarkan tugas, bukan angka tetap; pastikan konten data tetap memperoleh lebar yang cukup.
- Pada container sempit, susun media dan data vertikal dengan urutan baca dan fokus yang wajar.
- Jangan mengubah upload, crop, preview, deletion, atau persistence behavior untuk perubahan layout saja.

### 4. Adaptif terhadap ruang nyata
- Breakpoint dipilih dari lebar container dan kebutuhan isi, bukan hanya nama device atau kebiasaan memakai dua kolom.
- Pada ruang sempit, turunkan jumlah kolom dan biarkan field mengisi baris secara teratur; hindari horizontal overflow.
- Pertimbangkan sidebar/modal, zoom/scaling, label panjang, angka/tanggal lokal, pesan error, dan helper text.
- Pertahankan whitespace yang membantu grouping dan keterbacaan; rapikan ruang kosong yang timbul tanpa fungsi karena alignment/row sizing yang buruk.

### 5. Reuse dan konsistensi
- Gunakan komponen form, grid/layout primitive, spacing, typography, border, dan design token yang sudah dipakai repository.
- Hindari CSS/layout abstraction baru atau dependency kecuali dibutuhkan dan dibenarkan oleh consumer nyata dalam scope.
- Jangan menggandakan label, validation, helper/error mapping, atau business rule.
- Ikuti pola responsive dan style yang berlaku; jangan mengganti seluruh visual language saat task hanya meminta komposisi form.

### 6. Aksesibilitas dan behavior
- Pertahankan label yang terhubung ke kontrol, helper/error association, required/optional semantics, keyboard navigation, visible focus, dan urutan tab yang logis.
- Visual order harus konsisten dengan reading/focus order; hindari grid placement yang membingungkan pengguna keyboard atau screen reader.
- Beri target interaksi yang memadai dan jangan mengandalkan hover saja.
- Pastikan layout tidak menutupi error, status upload, tombol hapus, atau primary action.

## Cara Menilai dan Merancang
1. Audit komposisi yang tampak dan struktur form yang relevan: container, urutan field, komponen, helper/error, serta preview/upload bila ada. Bedakan fakta dari screenshot dengan fakta yang dibaca dari source.
2. Kelompokkan field menurut relasi tugas/data, bukan urutan untuk mengisi grid. Tentukan mana yang layak berbagi baris tanpa mengorbankan keterbacaan.
3. Pilih proporsi relatif berdasarkan panjang nilai/label, tipe kontrol, helper/error, dan kepentingan field. Hindari kolom sama lebar sebagai asumsi.
4. Tentukan peran foto/media: apakah perlu menjadi panel identifikasi yang jelas di samping data utama pada ruang lebar, atau lebih baik ditumpuk pada container sempit. Jaga agar kontrol upload dan statusnya tetap mudah ditemukan.
5. Uji keputusan terhadap lebar container, label/nilai panjang, helper/error, dan urutan baca/fokus. Reflow berdasarkan ruang yang benar-benar tersedia; jangan memaksakan breakpoint atau grid tertentu.
6. Pertahankan ruang kosong yang membantu grouping. Hilangkan ruang tak berguna akibat alignment/row sizing, tetapi jangan memadatkan form atau memperlebar field singkat tanpa manfaat.

## Acceptance Checklist
- Layout tidak mengasumsikan semua field membutuhkan lebar sama atau dua kolom.
- Field yang terkait dikelompokkan dan hanya berbagi baris saat ruang memadai.
- Proporsi foto/media dan area data mendukung tugas utama pada viewport lebar dan tetap terbaca pada viewport sempit.
- Tidak ada horizontal overflow atau field/error terpotong pada kondisi yang diuji.
- Field panjang/pendek mendapat ruang yang masuk akal; whitespace tetap disengaja.
- Komponen dan token existing digunakan bila sesuai; tidak ada abstraction/dependency tanpa kebutuhan.
- Label, validation, helper/error, upload/media actions, tab order, dan business logic tetap berfungsi.
- Criteria ditandai `PASS`, `PARTIAL`, `FAIL`, atau `UNKNOWN` berdasarkan evidence nyata.

## Integrasi dan Batas
- Skill ini memberi panduan UX, bukan workflow, authorization, atau lifecycle baru. Scope dan pelaporan mengikuti `native-workflow`.
- Untuk implementasi gunakan `native-programmer` beserta reuse-first procedure; untuk review gunakan `native-quality-review`. Bila Native Pi melakukan keduanya, review dilabeli `self_review`.
- Pertahankan komponen/token existing, behavior, validasi, dan business logic. Jangan mengubah makna field atau contract data sebagai efek samping perapian layout.
- Jika layout yang diinginkan memerlukan perubahan behavior atau domain contract yang tidak termasuk permintaan, jelaskan dampaknya dan minta keputusan sebelum memperluas scope.

## Output UX
Ringkas baseline yang diamati; masalah komposisi; grouping dan proporsi layout yang direkomendasikan beserta alasannya; behavior/aksesibilitas yang perlu dipertahankan; viewport dan state yang benar-benar diperiksa; temuan visual yang terkonfirmasi; serta unknown visual bila browser/viewport tidak tersedia. Format laporan dan status task mengikuti `native-workflow`.
