# Panduan Berkontribusi ke Kamus Aceh

Terima kasih sudah tertarik berkontribusi! Kamu **tidak perlu jago coding** untuk membantu. Cukup ikuti panduan ini langkah demi langkah.

---

## Apa itu GitHub?

GitHub adalah tempat menyimpan file secara online yang bisa diedit bersama-sama. Bayangkan seperti Google Docs, tapi untuk kode dan teks terstruktur. Setiap perubahan dicatat, jadi tidak ada yang bisa hilang.

---

## Cara Berkontribusi (Untuk Pemula)

### Yang kamu butuhkan

- Akun GitHub gratis → daftar di [github.com](https://github.com)
- Browser (Chrome, Firefox, Safari — tidak perlu install apapun lagi)

---

### Langkah 1 — Fork repositori ini

"Fork" artinya membuat salinan repositori ini ke akun GitHub kamu sendiri, supaya kamu bisa bebas mengeditnya.

1. Buka halaman repositori ini: `https://github.com/kbpro8/kamus-aceh`
2. Klik tombol **Fork** di pojok kanan atas
3. Pilih akun GitHub kamu → klik **Create fork**
4. Sekarang kamu punya salinan sendiri di `https://github.com/<username-kamu>/kamus-aceh`

---

### Langkah 2 — Buat file entri baru (langsung di browser)

1. Di repositori fork kamu, masuk ke folder `src/entries/`
2. Klik tombol **Add file** → **Create new file**
3. Beri nama file dengan format: `nama-kata.yaml`
   - Gunakan huruf kecil semua
   - Ganti spasi dengan tanda hubung `-`
   - Contoh: `ie-paya.yaml`, `meugah.yaml`, `boh-kayee.yaml`

---

### Langkah 3 — Isi isi file entri

Salin template berikut ke dalam file baru kamu, lalu isi bagian yang kamu tahu:

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
  - aceh: "Kalimat contoh dalam Bahasa Aceh."
    id: "Terjemahan Indonesia."
    en: "English translation."
etymology: "Asal usul kata (opsional)"
related_words:
  - "slug-kata-lain"
dialect_notes: "Catatan dialek jika ada (opsional)"
source: "Nama buku atau sumber"
date_added: "2025-01-01"
contributor: "Nama Kamu"
```

**Keterangan kode `part_of_speech`:**

| Kode | Artinya |
|------|---------|
| `kb` | kata benda (noun) |
| `kk` | kata kerja (verb) |
| `ks` | kata sifat (adjective) |
| `keterangan` | kata keterangan (adverb) |
| `partikel` | partikel |
| `kata ganti` | kata ganti (pronoun) |
| `seruan` | kata seru / interjection |
| `bilangan` | kata bilangan (numeral) |

**Isian wajib:** `headword`, `part_of_speech`, `definitions`, `source`, `date_added`, `contributor`

**Isian opsional (tapi sangat dihargai):** `jawi`, `ipa`, `examples`, `etymology`, `related_words`, `dialect_notes`

---

### Langkah 4 — Simpan file

1. Setelah selesai mengisi, scroll ke bawah
2. Di bagian **Commit new file**, tulis pesan singkat, contoh:
   `Tambah entri: ie-paya`
3. Pastikan pilihan **Commit directly to the main branch** dipilih
4. Klik **Commit new file**

---

### Langkah 5 — Kirim Pull Request

"Pull Request" (PR) adalah cara kamu mengajukan perubahan ke repositori utama. Pengelola akan mengecek dan menyetujuinya.

1. Kembali ke halaman fork kamu (`https://github.com/<username-kamu>/kamus-aceh`)
2. GitHub akan menampilkan banner: **"This branch is 1 commit ahead of kbpro8:main"**
3. Klik **Contribute** → **Open pull request**
4. Tulis judul PR yang jelas, contoh: `Tambah 3 entri baru: ie-paya, meugah, boh-kayee`
5. Di kotak deskripsi, ceritakan singkat entri apa yang kamu tambah dan dari sumber mana
6. Klik **Create pull request**

Selesai! Pengelola akan mengecek dan menggabungkan kontribusimu.

---

## Mengedit Entri yang Sudah Ada

Kalau kamu menemukan entri yang salah atau kurang lengkap:

1. Di fork kamu, buka file yang mau diedit di `src/entries/`
2. Klik ikon pensil ✏️ (Edit this file)
3. Lakukan perubahan
4. Commit dengan pesan seperti: `Perbaiki entri: ie-paya (tambah contoh kalimat)`
5. Buat Pull Request seperti Langkah 5 di atas

---

## Pedoman Kualitas

- **Ejaan**: Ikuti ejaan yang ada di sumber terpercaya (kamus cetak, publikasi akademik, dll)
- **Sumber**: Selalu sebutkan dari mana kamu mendapat informasi ini
- **Contoh kalimat**: Minimal satu contoh lengkap sangat membantu
- **Jawi**: Kalau kamu bisa tulisan Jawi, tambahkan — sangat berharga!
- **Jangan mengarang**: Kalau tidak yakin, biarkan field kosong daripada mengisi informasi yang tidak akurat

---

## Pertanyaan atau Masalah?

Buka [GitHub Issue](https://github.com/kbpro8/kamus-aceh/issues) dan jelaskan pertanyaanmu. Kami akan bantu!

---

*Terima kasih sudah membantu melestarikan Bahasa Aceh!*
