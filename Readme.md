# MediQ — Sistem Antrian Klinik Berbasis Web

MediQ adalah aplikasi web antrian klinik yang membantu pasien mengambil nomor antrian dari mana saja dan memantau posisinya secara langsung. MediQ juga membantu petugas klinik mengelola dan memanggil antrian per poli.

---

## 1. Masalah

**Rumusan masalah**
Banyak orang datang ke klinik tanpa tahu berapa lama mereka harus menunggu dan berapa banyak orang yang sedang mengantre.

**Siapa yang terdampak dan seberapa sering**
Semua orang yang datang untuk pemeriksaan, pengecekan, dan konsultasi. Belum ada data resmi, tetapi berdasarkan pengamatan lapangan, masalah ini masih sering ditemui.

**Akibat jika dibiarkan**
Pasien harus menunggu di klinik tanpa kepastian berapa lama mereka akan menunggu.

**Dasar bahwa masalah ini nyata**
1. Waktu tunggu dan ketidakpastian antrean memang tinggi di banyak fasilitas kesehatan.
2. Ketidakpastian tersebut terukur menurunkan kepuasan pasien.
3. Sistem yang memberi informasi antrean dan waktu tunggu terbukti memperbaiki pengalaman pasien.

---

## 2. Aktor

| Aktor | Peran dalam sistem |
|---|---|
| **Pasien** | Mengambil nomor antrian online, memantau status antrian dari HP, dan melihat riwayat rekam medis kunjungan sebelumnya. |
| **Petugas / Admin Klinik** | Mendaftarkan pasien walk-in, serta memanggil, mengulang, atau melewati nomor antrian per poli. |
| **Dokter** | Mencatat diagnosis dan resep setelah memeriksa pasien, serta melihat riwayat kunjungan pasien sebelumnya. |
| **Layar TV Ruang Tunggu** *(aktor sistem)* | Menampilkan nomor yang sedang dipanggil dan ruang tujuannya secara otomatis. |

---

## 3. Proses Bisnis


### Langkah-langkah

1. **Ambil antrian.** Pasien memilih poli, tanggal, serta dokter dan jam praktik, lalu mengisi data diri. Sistem menolak pendaftaran jika kuota habis, dokter libur, atau pasien sudah memiliki antrian aktif di hari yang sama.
2. **Terima tiket.** Pasien mendapat nomor antrian (mis. `A-015`) beserta detail poli, dokter, dan jadwal.
3. **Pantau antrian.** Pasien melihat nomor yang sedang dipanggil, sisa antrian di depannya, dan estimasi waktu tunggu dari HP, sehingga bisa datang mendekati gilirannya.
4. **Pasien walk-in.** Pasien yang datang tanpa daftar online didaftarkan petugas ke antrian yang sama.
5. **Pemanggilan.** Petugas menekan *Panggil Berikutnya*. Nomor yang dipanggil tampil di layar TV ruang tunggu dan di HP pasien.
6. **Pasien tidak hadir.** Jika pasien tidak muncul, petugas menekan *Panggil Ulang*. Jika tetap tidak hadir, petugas menekan *Lewati* dan lanjut ke nomor berikutnya. Nomor yang dilewati masih dapat dipanggil kembali oleh petugas saat pasien datang.
7. **Pemeriksaan & rekam medis.** Dokter memeriksa pasien, sambil dapat melihat riwayat kunjungan sebelumnya, lalu mencatat diagnosis dan resep. Setelah itu antrian ditandai *Selesai*.
8. **Riwayat pasien.** Pasien dapat melihat riwayat resep, catatan diagnosis, dan rekam medis kunjungan sebelumnya. Karena data ini sensitif, akses hanya untuk pasien yang bersangkutan dan dokter, setelah login.

### Status antrian

| Status | Arti |
|---|---|
| Menunggu | Nomor sudah diambil dan belum dipanggil |
| Dipanggil | Nomor sedang dipanggil atau pasien sedang dilayani |
| Dilewati | Pasien tidak hadir saat dipanggil; dapat dipanggil kembali oleh petugas |
| Selesai | Pelayanan selesai |
| Batal | Dibatalkan oleh pasien |

---

## 4. Fitur Utama

| No | Fitur (pekerjaan pengguna) | Aktor & masalah yang dijawab | Prioritas |
|---|---|---|---|
| 1 | Mengambil nomor antrian dengan memilih poli, dokter, dan jadwal | Pasien; antre lama di klinik | Must-have |
| 2 | Memantau nomor yang sedang dipanggil dan sisa antrian dari HP | Pasien; tidak tahu kapan gilirannya | Must-have |
| 3 | Memanggil, mengulang, atau melewati nomor antrian per poli | Petugas; pemanggilan masih manual | Must-have |
| 4 | Mendaftarkan pasien yang datang langsung ke antrian yang sama | Petugas; pasien walk-in | Must-have |
| 5 | Melihat riwayat resep, catatan diagnosis, atau rekam medis kunjungan sebelumnya | Pasien & Dokter | Must-have |


## 5. Anggota Kelompok

| Student ID | Nama | Peran |
|---|---|---|
| 25523120 | Ahmad Azzuri Pakalessy | Project Management |
| 25523115 | Muchmamad Aril Kurniawan | Frontend |
| 25523___ | Muhammad Zulfahmi Radityo | System Architect |
| 25523135 | Alfian Nur Saputro | QA Engineer / Tester |
| 21523080 | Satrio Damar Ramadhan | Back End |

---

## 6. Desain

Wireframe dan prototype UI (alur pasien, layar TV ruang tunggu, dan dashboard petugas) tersedia di Figma: [Wireframe Antrian Klinik](https://www.figma.com/design/zgm6pVJ6OAjkPHayVS4XMs)
