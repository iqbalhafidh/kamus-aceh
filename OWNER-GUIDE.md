# Panduan Pengelola — Kamus Aceh

Panduan ini khusus untuk kamu sebagai pemilik repositori. Berisi cara mengelola kontribusi, menjaga kualitas, dan memastikan proyek tetap hidup jangka panjang.

---

## Rutinitas Harian / Mingguan

### Mengecek Pull Request masuk

1. Buka `https://github.com/kbpro8/kamus-aceh/pulls`
2. Untuk setiap PR, cek:
   - Apakah format YAML valid? (GitHub akan menampilkan preview file)
   - Apakah `headword`, `part_of_speech`, `source`, `contributor`, dan `date_added` sudah diisi?
   - Apakah nama file sesuai (huruf kecil, pakai `-`, berekstensi `.yaml`)?
   - Apakah kontennya masuk akal dan bukan spam?
3. Kalau bagus → klik **Merge pull request**
4. Kalau perlu perbaikan → klik **Files changed** → **Review changes** → pilih **Request changes** dan tulis komentar yang ramah

### Template balasan PR yang baik

**Untuk PR yang diterima:**
> Terima kasih atas kontribusinya! Entri sudah digabungkan ke repositori. Semoga makin banyak kata Aceh yang bisa didokumentasikan bersama.

**Untuk PR yang perlu perbaikan:**
> Terima kasih sudah berkontribusi! Ada beberapa hal yang perlu diperbaiki sebelum bisa digabungkan:
> - [sebutkan masalahnya secara spesifik]
> Kalau ada pertanyaan, jangan ragu untuk tanya di sini.

---

## Mengecek Issues

1. Buka `https://github.com/kbpro8/kamus-aceh/issues`
2. Balas setiap issue dalam 3–7 hari — komunitas menghargai respons yang cepat
3. Gunakan label untuk mengorganisir: `bug`, `enhancement`, `question`, `good first issue`
4. Tandai issue yang sudah selesai dengan **Close issue**

### Cara menambahkan label

1. Di halaman Issues, klik **Labels** di sidebar kanan
2. Buat label baru: `tambah-entri`, `perbaikan`, `pertanyaan`, `prioritas-tinggi`, dll

---

## Menjaga Kualitas Entri

### Tanda entri yang bermasalah

- `headword` mengandung karakter aneh atau huruf kapital
- `source` kosong atau hanya ditulis "internet"
- Definisi dalam bahasa yang salah atau tidak masuk akal
- File bernama dengan huruf kapital atau spasi

### Cara memperbaiki langsung

Kamu bisa edit file YAML langsung di GitHub:
1. Masuk ke `src/entries/`
2. Klik file yang mau diperbaiki
3. Klik ikon pensil ✏️
4. Edit → Commit

Atau clone repositori ke laptop dan edit di sana:
```bash
git clone https://github.com/kbpro8/kamus-aceh.git
cd kamus-aceh
# edit file
git add .
git commit -m "Perbaiki entri: nama-kata"
git push
```

---

## Deployment & Situs Web

Situs otomatis di-deploy ke GitHub Pages setiap kali ada push ke `main`.

### Mengecek status deploy

1. Buka `https://github.com/kbpro8/kamus-aceh/actions`
2. Cari workflow **Deploy to GitHub Pages**
3. Tanda ✅ hijau = berhasil, ❌ merah = gagal
4. Kalau gagal, klik workflow-nya untuk melihat log error

### Waktu deploy

Biasanya 2–5 menit setelah merge PR atau push ke main. Kalau lebih dari 10 menit, cek Actions.

---

## Backup Rutin

Data kamus kamu ada di GitHub — tapi tetap bijak untuk backup lokal:

```bash
# Clone/update backup lokal
git clone https://github.com/kbpro8/kamus-aceh.git ~/backup-kamus-aceh
# atau jika sudah ada:
cd ~/backup-kamus-aceh && git pull
```

Pertimbangkan backup ke Google Drive atau hard drive eksternal setiap bulan, terutama folder `src/entries/`.

---

## Menambah Kontributor Terpercaya

Kalau ada kontributor yang aktif dan terpercaya, kamu bisa beri akses langsung (tanpa PR):

1. Buka `https://github.com/kbpro8/kamus-aceh/settings/access`
2. Klik **Add people**
3. Masukkan username GitHub mereka
4. Pilih role:
   - **Write** — bisa push langsung dan merge PR
   - **Triage** — bisa kelola Issues dan PR tapi tidak bisa merge
   - **Read** — hanya bisa lihat (default untuk semua orang)

Mulai dengan **Triage** untuk kontributor baru, tingkatkan ke **Write** setelah terbukti.

---

## Promosi & Membangun Komunitas

### Langkah awal untuk menarik kontributor

1. **Bagikan ke komunitas Aceh** — grup Facebook, Telegram, atau WhatsApp tentang bahasa/budaya Aceh
2. **Mention di sosmed** — Twitter/X, Instagram dengan tagar #BahasaAceh #KamusAceh
3. **Hubungi universitas** — Fakultas Bahasa di Universitas Syiah Kuala, UIN Ar-Raniry bisa jadi mitra
4. **Ajukan ke BPBA** — Badan Pengembangan Bahasa dan Perbukuan Aceh

### Hal yang perlu disiapkan untuk komunitas

- **README yang menarik**: Tambahkan badge jumlah entri, screenshot situs, dan tombol "Berkontribusi"
- **Good First Issue**: Tandai beberapa issue sederhana dengan label `good first issue` supaya pemula tahu dari mana mulai
- **Changelog**: Catat setiap milestone (1.000 entri, 5.000 entri, dst.) di Releases

---

## Milestone yang Perlu Dirayakan

Buat **GitHub Release** untuk setiap pencapaian besar:

1. Buka `https://github.com/kbpro8/kamus-aceh/releases`
2. Klik **Create a new release**
3. Beri tag versi (contoh: `v1.0`, `v2.0`)
4. Tulis deskripsi pencapaian

Contoh milestone:
- 1.000 entri → v0.1
- 5.000 entri → v0.5
- 10.000 entri → v1.0
- 25.000 entri → v2.0

---

## Lisensi dan Kredit

Pastikan file `LICENSE` ada di root repositori. Proyek ini menggunakan:
- Konten: Creative Commons BY-SA 4.0
- Kode: MIT

Jangan ubah lisensi tanpa memberitahu kontributor yang sudah ada.

---

## Tanda-Tanda Repositori Sehat

- Pull Requests ditinjau dalam < 1 minggu
- Issues dibalas dalam < 3 hari
- Tidak ada entri duplikat atau kosong
- Deploy selalu berhasil (Actions hijau semua)
- Ada aktivitas commit minimal 1x sebulan

---

*Kamu melakukan pekerjaan penting. Pelestarian bahasa daerah dimulai dari langkah kecil seperti ini.*
