# MIDNIGHT LAB..

Game horor 3D berbasis browser bertema edukasi. Kamu terjebak semalaman di lab komputer sekolah, harus menjawab soal-soal mata pelajaran pilihanmu (RPL, B. Indonesia, B. Inggris, Sejarah, Matematika, atau Campuran), dan menghindari dua hantu bernama **El Kalla** dan **Oni**.

> Seluruh karakter, cerita, dan kejadian adalah fiksi. Game ini dibuat untuk hiburan dan pembelajaran, dan tidak menggambarkan institusi atau tempat tertentu.

Dibuat oleh Iqdham, Kevin, Arif.

## Daftar isi
[Cerita](#cerita) · [Cara bermain](#cara-bermain) · [Mode](#mode) · [Fitur](#fitur) · [Ending dan cutscene](#ending-dan-cutscene) · [Menjalankan](#menjalankan) · [Struktur file](#struktur-file) · [Panduan pengembang](#panduan-pengembang) · [Saran dan peringatan](#saran-dan-peringatan)

---

## Cerita
Wandih adalah siswa SMK yang malas dan tiga kali tidak naik kelas. Seluruh cerita (Single Player) tampil sebagai **cutscene 3D** beranimasi.

1. **Pembuka di kelas (sore):** Wandih tertidur di kelas, namanya selalu di urutan paling bawah rapor, rapor merah, teman-temannya lulus lebih dulu, lalu ia menolak mengerjakan remedial. Guru menggiringnya ke lab komputer.
2. **Hukuman di lab:** Guru memarahi Wandih, menyuruhnya mengerjakan semua soal di lembar kertas, lalu keluar dan mengunci pintu.
3. **Cerita dari teman (flashback):** tiga teman Wandih pernah menginap di lab untuk mengedit poster dan membuat proyek event sekolah, lalu diganggu El Kalla dan Oni dan kapok.
4. **Tengah malam:** lampu berkedip, El Kalla dan Oni muncul bergantian secara samar. Permainan dimulai.
5. **Telepon guru:** setelah soal terakhir benar, Wandih menelpon Guru (yang duduk di kantor memegang HP) dan diminta mengambil kunci cadangan.
6. **Monolog di jalan:** Wandih pulang naik Vespa merah melewati jalan hutan malam hari, sambil bermonolog (dan melihat sosok samar di pinggir jalan).
7. **Ending:** sampai di rumah, membuka pintu, masuk, lalu tidur. Ada tiga ending (lihat [Ending dan cutscene](#ending-dan-cutscene)).

## Cara bermain

### Tujuan
1. Temukan dan jawab semua lembar soal di meja komputer (muncul 5 lembar per gelombang). Pilihan jawaban diacak tiap kertas dibuka.
2. Telepon guru, lalu ambil kunci di meja guru (ruang biru).
3. Buka pintu di ruangan itu dan keluar.

### Kontrol
| | PC / Laptop | HP |
|---|---|---|
| Jalan | W A S D atau tombol panah | geser layar kiri (joystick) |
| Lari | Shift (tahan) | tombol LARI (ketuk, aktif/nonaktif) |
| Melihat | Mouse | geser layar kanan (atau gyro, lihat Pengaturan) |
| Interaksi | E | ketuk tulisan interaksi |
| Senter | F | tombol senter kanan bawah |

Lari memakai **stamina** yang habis lalu terisi kembali.

### Shortcut keyboard (PC / Laptop)
| Tombol | Fungsi |
|---|---|
| 1 - 4 | Memilih jawaban saat membaca kertas soal |
| Q | Menutup kertas soal tanpa menjawab |
| P | Jeda dan lanjut (Single Player) |
| M | Bisukan / hidupkan semua suara |
| Esc | Melepas kursor mouse (Single Player otomatis menjeda) |
| Enter / Space | Melanjutkan teks cerita |
| Enter (Multi Player) | Membuka chat, Enter lagi untuk kirim, Esc untuk tutup |
| V (Multi Player) | Chat cepat emoji, lalu tekan `1`-`8` (HP: tombol 😁) |
| Z / X / C (Multi Player) | Tanda cepat: soal di sini / kunci di sini / hantu! |
| Panah kiri / kanan (Multi Player) | Berganti pemain yang ditonton saat menjadi penonton |

### Aturan
- Jawaban benar menjadi hijau, salah menjadi merah. Lembar yang salah bisa dicoba lagi.
- **Gagal** jika salah menjawab melebihi batas salah level (lihat tabel), atau jika disentuh El Kalla atau Oni.
- Saat El Kalla atau Oni muncul, sembunyi di lemari (E). Jika ia berdiri di depan lemari, ia pergi setelah 5 detik.
- Saat hantu mendekat, **detak jantung dan getar** (HP) makin cepat sebagai petunjuk. Keduanya bisa dimatikan di Pengaturan.

### Hantu: El Kalla dan Oni
Dua hantu muncul **bersamaan** di setiap putaran. Masing-masing menjaga **satu ruang** dan hanya berkeliling di ruangnya sendiri (memeriksa 2 lemari di ruang itu). Tiap putaran mereka **bertukar ruang**:

| Putaran | Ruang pertama (kuning) | Ruang kedua (biru) |
|---|---|---|
| 1 (setelah pemain spawn) | El Kalla | Oni |
| 2 | Oni | El Kalla |
| 3 | El Kalla | Oni |
| dst. | bergantian terus | bergantian terus |

Kedua hantu muncul di batas dua ruang (sisi kiri/kanan diacak), lalu masuk ke ruangnya. Hantu hanya mengejar pemain yang ada di ruangnya. Jeda setelah hantu menghilang sama dengan jeda kemunculan pertama (lihat tabel level), dihitung setelah **kedua** hantu pergi. Yang berbeda antara keduanya hanya wajah dan suara langkah/keliling.

### Tingkat kesulitan
| Level | Single Player | Batas salah | Multi Player (soal) | Hantu muncul / jeda | Hadir | Kecepatan |
|---|---|---|---|---|---|---|
| Mudah | 10 soal | 6 (60%) | 10 + 3 per pemain tambahan | 55 dtk | 20 dtk | +10% |
| Sedang | 15 soal | 8 (50%) | 15 + 3 per pemain tambahan | 40 dtk | 25 dtk | +20% |
| Sulit | 20 soal | 8 (40%) | 20 + 3 per pemain tambahan | 30 dtk (SP) / 25 dtk (MP) | 30 dtk | +30% |
| Latihan (SP) | 10 soal | tanpa batas | - | tanpa hantu | - | - |

Level **Latihan** tidak ada hantu dan tidak tercatat di rekor. Di Multi Player, batas salah berlaku **per pemain** dan tidak bertambah mengikuti jumlah pemain.

### Mata pelajaran
- **Single Player:** setelah menekan MULAI di layar Cara Bermain, pilih mata pelajaran (atau **Campuran**). Soal dalam game diambil dari mapel itu.
- **Multi Player:** pembuat room memilih mapel di lobi (di bawah tombol level). Pemain lain hanya melihat mapel yang dipilih.
- Soal disimpan di `soal.js` per mapel (`BANK.rpl`, `BANK.indonesia`, `BANK.inggris`, `BANK.sejarah`, `BANK.matematika`).

## Mode
- **Single Player:** cerita Wandih melawan El Kalla dan Oni sendirian, lengkap dengan semua cutscene di atas.
- **Multi Player:** **2 sampai 6 pemain** lewat PeerJS. Satu pemain membuat room dan membagikan kode, yang lain masuk dengan kode itu. Ada chat lobi/dalam game, chat cepat emoji, penanda lokasi (soal, kunci, hantu), dan mode penonton bagi pemain yang gagal atau tertangkap. Multi Player tidak memakai cutscene cerita.

## Fitur

### Skor, rekor, dan peringkat
- **Rekap hasil** (`fitur.js`): di akhir game (menang, diculik, atau gagal) tampil skor, waktu, benar/salah, dan daftar soal yang salah beserta jawaban benar. Di Multi Player, daftar soal yang salah ditambahkan ke papan skor akhir.
- **Skor:** `(benar x 100 - salah x 30)`, ditambah bila menang `500 + bonus waktu (maks 600)`, ditambah 300 untuk ending rahasia, lalu dikali level (Mudah 1, Sedang 1,25, Sulit 1,5).
- **Rekor dan statistik:** disimpan di `localStorage` (`mlab_stats`), jadi ikut offline. Tombol REKOR di menu utama.
- **Peringkat online:** skor bisa dikirim lewat tombol KIRIM SKOR ke Google Apps Script (`Code.gs`, sheet `Skor`, filter mapel, level, kelas). Skor yang gagal terkirim disimpan dan dikirim ulang saat online. Skor dihitung di sisi pemain. Kalau `Code.gs` diubah, deploy ulang (Deploy > Manage deployments > New version).
- **Ulasan:** halaman TENTANG berisi latar belakang game dan kolom ulasan bintang (`tentang.js`, juga lewat Apps Script). `xsx.html` adalah halaman admin ulasan (tidak diindeks mesin pencari).

### Pengaturan (ikon gigi)
Volume musik, volume efek suara, sensitivitas mouse/layar, jumpscare (suara dan efek kilat), kualitas grafis (Rendah/Sedang/Tinggi), latar menu 3D, detak jantung dan getar, ukuran dan tinggi tombol, mode kidal, joystick tetap, gyro (dengan opsi balik arah), teks soal besar, kontras tinggi, dan tampilan minimalis (HP).

Catatan: gyro belum diuji di perangkat asli (iPhone butuh izin sensor).

### Layar besar (desktop)
Di monitor lebar (>= 1500 px, mouse) panel menu, teks cerita, dan HUD otomatis diperbesar 1,2-1,25x, dan 1,5-1,6x di layar >= 2200 px (4K). Aturannya ada di akhir `style.css`.

### Tampilan minimalis HP
`mobile.css` dan `mobile.js`. Aktif otomatis di layar sentuh, bisa dimatikan lewat Pengaturan > "Tampilan minimalis (HP)" (`localStorage` `mlab_mn`). Isi: menu utama dengan satu tombol MULAI besar, kartu pilihan 2 kolom dengan teks ringkas, Cara Bermain jadi 3 kartu pendek, HUD dan tombol kontrol lebih transparan. Rincian lengkap level tetap ada di Panduan.

### Pasang sebagai aplikasi (PWA)
Game ini bisa dipasang seperti aplikasi dan dimainkan offline setelah dibuka sekali dengan internet.
- **Android (Chrome):** buka alamat game, tekan **PASANG APLIKASI** di menu (atau menu titik tiga > *Instal aplikasi*).
- **iPhone (Safari):** tombol Bagikan > *Tambah ke Layar Utama*.
- Aplikasi terpasang berjalan layar penuh dan terkunci landscape. Single Player otomatis jeda saat aplikasi ke latar belakang (`pwa.js`).
- Multiplayer, peringkat online, dan ulasan tetap butuh internet.

### Durasi jumpscare dan glitch
Jumpscare 3 detik, lalu glitch 5 detik (total 8 detik, Single Player dan Multi Player), disesuaikan dengan `jumpscare.mp3` (3,1 dtk) dan `glitch.mp3` (5,2 dtk). Angkanya ada di `game.js` (`scT<3` dan `scT<8`) dan `mp2.js` (`scT=8.01` saat jumpscare dimatikan).

## Ending dan cutscene
Semua adegan di bawah memakai panggung 3D. Kalau 3D gagal dimuat, adegan otomatis kembali ke gambar cadangan (`sv`/`img`).

| Situasi | Naskah | Isi |
|---|---|---|
| Menang normal | `END` (`cerita.js`) | Sampai di rumah, buka pintu, masuk, tidur |
| Lolos tapi salah >= 60% batas salah | `END_JELEK` (`cerita2.js`) | "Bayangan di Spion": hantu menumpang di Vespa, mata di jendela kamar |
| Semua benar dan tidak pernah bersembunyi | `END_RAHASIA` (`cerita2.js`) | "Penjaga Lab": El Kalla dan Oni memberi kertas nilai 100 di ambang pintu lab |
| Diculik El Kalla | `CAUGHT_KALLA` | Diseret ke pintu lab, pintu dikunci |
| Diculik Oni | `CAUGHT_ONI` | Layar komputer menyala, Wandih memudar |
| Gagal karena terlalu banyak salah | `CAUGHT_SALAH` | Kedua hantu muncul bersama dan "menghitung" kesalahan |

---

## Menjalankan
Buka `index.html` di browser modern (Chrome, Edge, Firefox, Safari) dengan koneksi internet, atau jalankan lewat server lokal, misalnya `python3 -m http.server`, lalu buka `http://localhost:8000`.

Three.js r128 dan PeerJS 1.5.4 dimuat dari cdnjs, jadi pertama kali butuh internet. Setelah itu service worker menyimpannya di cache untuk mode offline.

## Struktur file
| File | Fungsi |
|---|---|
| `index.html`, `style.css`, `mobile.css` | Struktur halaman, menu, dan tampilan |
| `game.js` | Mesin game, cerita, kontrol, hantu |
| `mp.js`, `mp2.js` | Multiplayer (PeerJS) |
| `soal.js` | Bank soal |
| `cerita.js` | Cerita pembuka (`OPEN`), telepon (`CALL`), monolog (`MONO`), ending (`END`), dan `CUT_SND` (sound cutscene) |
| `cerita2.js` | Cutscene tertangkap (`CAUGHT_*`), ending jelek dan rahasia |
| `cutscene3d.js` | Mesin cutscene 3D: tokoh, ekspresi wajah, kamera, panggung `hukuman`, `lab`, `telepon`, `kantor` |
| `cutscene_awal.js` | Panggung `kelas` dan `teman` (cerita pembuka) |
| `cutscene_akhir.js` | Panggung `jalan`, `rumah`, `tidur`, `ambang`, `tangkap` |
| `fitur.js` | Rekap, skor, rekor, peringkat online, pengaturan, stamina, latihan, gyro, chat emoji |
| `tentang.js` | Halaman Tentang dan ulasan |
| `mobile.js` | Tampilan minimalis HP |
| `pwa.js`, `sw.js`, `manifest.webmanifest` | Aplikasi terpasang dan mode offline |
| `aset.js` | Daftar gambar dan suara (skin tokoh, poster, `BLANKET_URL`, dll.) |
| `xsx.html` | Halaman admin ulasan |
| `hantu.png`, `hantu.mp3` | Wajah dan suara El Kalla |
| `oni.png`, `oni.mp3` | Wajah dan suara Oni (ganti dengan file buatanmu, nama file tetap) |

---

## Panduan pengembang

### Format adegan cerita
Adegan ada di `cerita.js` dan `cerita2.js`. Tiap adegan punya `e` (ikon), `t` (judul), `x` (teks), `bg` (dua warna latar), `snd` (suara adegan), `ok:true` (tombol OK) dan field di bawah.

| Field | Fungsi |
|---|---|
| `img` | File gambar 16:9 (jpg/png) di folder yang sama dengan `index.html`. Kalau belum ada, otomatis memakai `sv` |
| `sv` | Nama scene gambar-lewat-kode di `SCN` (SVG) sebagai cadangan |
| `who` | `'WANDIH'` atau `'GURU'`: pembicara disorot, kepalanya mengangguk saat teks diketik |
| `fx` | `'shake'` (layar bergetar) atau `'flash'` (kilat) saat adegan muncul |
| `amb` | Daftar suara latar berulang, mis. `['night.mp3',CUT_SND.motor]` |

Gambar cadangan opsional: `scene-hukuman.jpg`, `scene-teman.jpg`, `scene-tengahmalam.jpg`.

### Cutscene 3D
Adegan dengan field `stage` tampil sebagai adegan 3D: tokoh balok bergerak dan berdialog, kamera berpindah sudut seperti film. Panggung `hukuman`, `lab`, `telepon`, `teman` memakai **ruang pertama (dinding kuning) lab yang sama dengan yang dimainkan** (scene game dirender dengan kamera cutscene). Panggung lain punya ruang sendiri.

| Panggung | Isi |
|---|---|
| `kelas` | Ruang kelas sore hari (`cutscene_awal.js`) |
| `hukuman` | Guru dan Wandih di ruang pertama lab, pintu belakang |
| `teman` | Flashback tiga teman di lab (`cutscene_awal.js`) |
| `lab` | Tengah malam, lampu berkedip, hantu samar |
| `telepon` | Wandih menelpon, berdiri di tempat pemain menyelesaikan soal |
| `kantor` | Guru duduk di meja kerja memegang HP |
| `jalan` | Jalan hutan malam, Vespa merah, tiang lampu tiap 10 m (`cutscene_akhir.js`) |
| `rumah` | Halaman, rumah batu, rumah tetangga, pintu rumah |
| `tidur` | Kamar tidur, selimut dinamis, efek Zzz |
| `ambang` | Ambang pintu lab (ending rahasia) |
| `tangkap` | Adegan diculik / gagal |

Field umum:

| Field | Fungsi |
|---|---|
| `stage` | Nama panggung (tabel di atas) |
| `cam` | Sudut kamera. hukuman: `tegang`, `guru`, `wandih`, `pintu`. lab: `belakang`, `lorong`. telepon: `wdepan`, `wsamping` (otomatis menghindari meja/dinding). kantor: `meja`, `dekat`. kelas: `lebar`, `wandih`, `papan`, `dua`, `lulus`, `keluar`. teman: `lebar`, `dekat`, `pintu`. jalan: `kiri`, `belakang`, `depan`, `atas`, `sorot`. Panggung lain: lihat `shots` di kodenya |
| `anim` | Animasi per tokoh, mis. `{GURU:'marah',WANDIH:'takut'}` (daftar di bawah) |
| `expr` | Ekspresi wajah per tokoh, mis. `{T1:'senang'}`: `normal`, `senang`, `lelah`, `takut`, `marah` |
| `go` | Jalan ke titik (x,z), mis. `{GURU:[[-3,11.4],[-4.5,12.95]]}` |
| `at` | Langsung pindah ke titik (x,z), mis. `{WANDIH:[-2.75,11.5]}` |
| `look` | Arah hadap: nama tokoh atau titik, mis. `{WANDIH:'GURU'}` |
| `spd` | Kecepatan jalan (m/s) |
| `pan` | `true` = kamera bergeser halus ke sudut baru (bawaan: potong langsung) |
| `kalla`, `keep` | Panggung `lab`: `kalla:'creep'` = tiap lampu padam muncul **satu** hantu samar (opacity 30%), bergantian El Kalla lalu Oni, makin dekat. `keep:true` = hantu tidak diulang dari awal |

Field khusus panggung:

| Panggung | Field |
|---|---|
| `kelas` | `board` (`'ajar'`, `'rank'`, `'rapor'`, `'lulus'`, `'remedial'`), `stamp` (stempel TERBAWAH), `zzz`, `paper`, `rapor`, `lulus` (teman bertopi toga bersorak) |
| `teman` | `flick` (lampu berkedip), `ghost` (El Kalla dan Oni bergantian samar), `walk` (teman berjalan atau berlari keluar lewat pintu belakang) |
| `jalan` | `hantu:'K'` atau `'O'` (sosok samar di pinggir jalan, kiri atau kanan), `hdelay` (jeda muncul, bawaan 0,7 dtk) |
| `tangkap` | `lamp`, `gop`, `pintu`, `seret`, `hide`, `padam` (lihat `cerita2.js`) |

**Animasi:** `diam`, `tunduk`, `takut`, `kaget`, `marah`, `tunjuk`, `bicara`, `dorong`, `melayang`, `telp` (berdiri menelpon), `dudukTelp` (duduk menelpon), `tulis`, `tolak`, `lelah`, `rayakan`, `lari`; duduk: `duduk`, `ketik`, `ketik2`, `ngobrol`, `tertawa`, `dudukTakut`, `dudukKaget`, `tidurDuduk`.

Kalau terjadi error di adegan 3D, adegan otomatis memakai `sv`/`img`. Cari pesan `cutscene3d:` di konsol browser untuk melihat penyebabnya. Saat keluar dari adegan, semua tokoh cutscene tambahan otomatis disembunyikan.

### Sound buatan sendiri
Di bagian atas `cerita.js` ada `CUT_SND`. Taruh file (mp3) di folder yang sama dengan `index.html`, lalu isi namanya:

| Nama | Adegan |
|---|---|
| `wandihKaget` | Wandih: "Hah?! Semalaman di lab, Pak? Tapi... saya..." |
| `guruMarah` | Guru: "Kerjakan semua soal di lembar kertas..." (kalau kosong, dibacakan suara bawaan browser) |
| `lorong` | Lampu kelap-kelip, hantu bergantian: "Sunyi... lalu terdengar langkah pelan." |
| `lorongLanjut` | Lanjutan teks: "Cari lembar soal dan selesaikan..." |
| `pintuGuru` | 1 file untuk buka + tutup + kunci pintu saat Guru keluar (bawaan `pintu-guru.mp3`, cadangan `bukapintu.mp3`) |
| `temanCerita` | Adegan "CERITA DARI TEMAN", diputar sekali |
| `temanTeriak` | Teman berlari panik, diputar sekali (langkah berulang diatur otomatis) |
| `motor` | Suara Vespa berulang selama monolog di jalan, berhenti saat Wandih parkir |

### Aset
- **Selimut:** `selimut.png`, ukuran **1500 x 1400 px** (rasio 15:14). Nama file diubah di `BLANKET_URL` (`aset.js`). Tanpa file, dipakai motif bawaan.
- **Skin Wandih:** `SKIN_FULL` di `aset.js` (`kepala_full.png`, `badan_full.png`, dan seterusnya).
- **Wajah hantu:** `hantu.png` dan `oni.png`.
- **Poster kubikel:** `POSTER_URLS` di `aset.js`.

### PWA dan cache
- Aset (audio/gambar) disimpan di cache oleh `sw.js`. **Setiap mengganti aset, naikkan versi `V` di `sw.js`**. Kode (html/js/css) selalu diambil dari jaringan dulu, jadi pembaruan kode otomatis terpakai.
- Kalau menambah file aset baru, tambahkan juga namanya ke daftar `MEDIA` di `sw.js`. Kalau menambah file kode baru, tambahkan ke `CORE`.
- Service worker hanya aktif di HTTPS (GitHub Pages) atau `localhost`, bukan saat membuka file langsung.

## Saran dan peringatan
- **Matikan jumpscare** (ikon gigi di atas layar) jika di bawah umur, mudah takut, memiliki kecemasan, penyakit jantung, atau sensitif terhadap kilatan cahaya dan suara keras.
- **Mainkan Single Player dulu** untuk mengenal denah lab, lemari, dan pola hantu tanpa tekanan pemain lain, atau coba level **Latihan** yang tanpa hantu.
- Istirahat jika merasa pusing, sesak, atau cemas berlebihan.
