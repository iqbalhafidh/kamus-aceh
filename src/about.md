---
layout: base.njk
title: Tentang
description: Tentang Kamus Aceh — cara berkontribusi dan lisensi.
permalink: /about/
---

<div class="prose">

## Tentang Kamus Aceh

**Kamus Aceh** adalah kamus digital gratis untuk Bahasa Aceh, dirancang untuk memudahkan dokumentasi dan pelestarian bahasa daerah Aceh. Setiap entri tersedia dalam tiga bahasa: Aceh, Indonesia, dan Inggris.

Proyek ini sepenuhnya berbasis teks biasa (YAML) yang disimpan di GitHub, sehingga siapa pun dapat berkontribusi melalui pull request.

## Cara berkontribusi

Kamu **tidak perlu jago coding** untuk berkontribusi — cukup akun GitHub gratis dan browser.

### Langkah 1 — Fork repositori

1. Buka [github.com/kbpro8/kamus-aceh](https://github.com/kbpro8/kamus-aceh)
2. Klik tombol **Fork** di pojok kanan atas
3. Pilih akun GitHub kamu → klik **Create fork**

### Langkah 2 — Buat file entri baru

1. Di fork kamu, buka folder `src/entries/`
2. Klik **Add file** → **Create new file**
3. Beri nama file: `nama-kata.yaml` (huruf kecil, pakai `-` untuk spasi)

### Langkah 3 — Isi entri

Salin template berikut dan isi bagian yang kamu tahu:

```yaml
headword: "kata-aceh"
jawi: "کات اچيه"
alt_spelling:
  - "ejaan-alternatif"
ipa: "/transkripsi-ipa/"
part_of_speech: "kb"
definitions:
  - meaning_id: "Arti dalam Bahasa Indonesia"
    meaning_en: "Meaning in English"
examples:
  - aceh: "Kalimat dalam Bahasa Aceh."
    id: "Terjemahan Indonesia."
    en: "English translation."
etymology: "Asal usul kata"
related_words:
  - "slug-kata-lain"
dialect_notes: "Catatan dialek jika ada"
source: "Nama buku atau sumber"
date_added: "2025-01-01"
contributor: "Nama Kamu"
```

**Wajib diisi:** `headword`, `part_of_speech`, `definitions`, `source`, `date_added`, `contributor`

**Opsional (sangat dihargai):** `jawi`, `ipa`, `examples`, `etymology`, `related_words`, `dialect_notes`

Kode `part_of_speech`: `kb` (kata benda) · `kk` (kata kerja) · `ks` (kata sifat) · `keterangan` · `partikel` · `kata ganti` · `seruan` · `bilangan`

### Langkah 4 — Commit dan kirim Pull Request

1. Scroll ke bawah, tulis pesan commit: `Tambah entri: nama-kata`
2. Klik **Commit new file**
3. Kembali ke fork kamu → klik **Contribute** → **Open pull request**
4. Tulis judul yang jelas, klik **Create pull request**

Selesai! Pengelola akan mengecek dan menggabungkan kontribusimu.

Panduan lengkap dengan penjelasan lebih detail tersedia di [CONTRIBUTING.md](https://github.com/kbpro8/kamus-aceh/blob/main/CONTRIBUTING.md).

## Lisensi

- **Konten** (entri kamus): [Creative Commons BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
- **Kode sumber** (template, CSS, konfigurasi): [MIT License](https://opensource.org/licenses/MIT)

## Teknologi

Situs ini dibangun dengan [Eleventy](https://www.11ty.dev/) (generator situs statis) dan pencarian ditenagai oleh [Pagefind](https://pagefind.app/), tanpa server atau basis data. Di-_host_ gratis di [GitHub Pages](https://pages.github.com/).

## Proyek terkait

- [Aceh Wiki History](https://kbpro8.github.io/acehwiki) — ensiklopedia sejarah Aceh berbasis Quartz.

</div>
