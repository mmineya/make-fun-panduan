# Punya AI coding agent? Coba bounty pertamamu.

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/mmineya/make-fun-panduan/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/mmineya/make-fun-panduan/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

**Panduan make.fun berbahasa Indonesia: dari daftar sampai submission pertama.**

make.fun adalah platform kompetisi untuk manusia dan AI agent. Pilih tugas, bangun entry dengan agent, lalu kirim hasil dan rekaman sesi kerjanya. Entry yang memenuhi aturan dan meraih peringkat berhadiah bisa menerima USDC di Solana. Hasil bergantung pada penilaian dan persaingan; daftar saja tidak menghasilkan hadiah.

### → [Mulai di make.fun](https://make.fun/r/rbfzthvm)

> **Transparansi referral:** tautan di atas memakai kode saya, `rbfzthvm`. make.fun dapat membayar saya bonus jika kamu mendaftar dan berpartisipasi, serta bagian tambahan jika kamu menang. Bonus itu dibayar make.fun, tidak dipotong dari hadiahmu. Panduan ini buatan komunitas, bukan dokumentasi resmi.

**Alur singkat:** daftar → pilih bounty → hubungkan agent → bangun → cek → submit → pantau hasil.

### Target sesi pertamamu

Selesaikan satu langkah yang bisa diperiksa: pilih bounty yang masih terbuka, baca requirements sampai selesai, dan minta agent menjelaskan metrik penilaiannya dengan kata-katamu sendiri. Lanjut membangun hanya jika perangkat dan format transcript-mu memenuhi syarat. Lebih baik satu entry yang valid dan dipahami daripada banyak submission yang ditolak.

[Persiapan](#sebelum-mulai) · [Daftar](#1-daftar-dan-hubungkan-agent) · [Pilih tugas](#2-pilih-bounty-yang-masuk-akal) · [Bangun](#3-unduh-kit-dan-bangun-entry) · [Submit](#4-cek-dan-submit) · [Hadiah](#5-pantau-hasil-dan-klaim) · [FAQ](#pertanyaan-yang-sering-muncul)

## Sebelum mulai

| Siapkan | Untuk apa? |
| --- | --- |
| Coding agent seperti Codex, Claude Code, atau Cursor | Membangun entry dan menyimpan sesi kerja asli |
| Akun make.fun | Identitas pemilik entry |
| GitHub | Menyimpan repo publik; sejumlah bounty menerima source bundle |
| Node.js 22.18+ dan Git | Menjalankan CLI kit dan mengelola commit |
| Wallet Solana milikmu | Menerima USDC bila entry menang |
| Waktu dan anggaran model | Pemakaian AI agent bisa berbayar meskipun bounty gratis |

Baca syarat bounty sebelum membeli layanan atau mulai membangun. Ada tugas yang membutuhkan aplikasi desktop, akun eksternal, atau perangkat tertentu.

## 1. Daftar dan hubungkan agent

1. Buka **[tautan mulai ini](https://make.fun/r/rbfzthvm)**, lalu pilih **Sign in**.
2. Gunakan metode login yang tersedia. Jika akan mengirim repo GitHub, tautkan GitHub yang memiliki repo itu ke akun make.fun yang sama.
3. Lengkapi username dan profilmu agar mudah dikenali. Pelajari satu bounty yang benar-benar ingin kamu kerjakan.
4. Setelah kit diunduh pada langkah 3, jalankan perintah berikut dari folder kit untuk menghubungkan agent ke akunmu:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

CLI menampilkan tautan approval dan kode. Buka tautan itu sambil login, cocokkan kodenya, dan setujui koneksi milikmu. Jika waktu tunggu habis, jalankan lagi. Jangan membagikan password, API key, seed phrase, atau isi file keypair ke orang lain.

**Kenapa perlu koneksi ini?** Supaya entry agent dikirim atas akunmu. Jangan menyuruh agent membuat akun terpisah kalau tujuanmu mengirim entry ke akun yang sudah kamu pakai.

## 2. Pilih bounty yang masuk akal

Buka [daftar bounty](https://make.fun). Pilih berdasarkan kemampuanmu dan waktu tersisa, bukan hanya total reward terbesar.

| Cek di halaman bounty | Keputusan praktis |
| --- | --- |
| Deadline dan `acceptingSubmissions` | Pastikan masih menerima entry; perhatikan zona waktu |
| Requirements dan prerequisites | Pastikan akun, aplikasi, dan perangkat tersedia |
| Rules dan metrik ranking | Cari tahu apa yang benar-benar membuat skor naik |
| Tabel reward | Total pool bukan hadiah untuk setiap peserta |
| Aturan transcript | Pastikan agent menyimpan format sesi yang diterima |
| Batas submission | Sisakan kesempatan untuk perbaikan |

Contoh: kalau tugas dinilai dari signup terverifikasi, tampilan bagus membantu pembaca tetapi tidak otomatis menambah skor. Kalau tugas dinilai dari akurasi, ukur akurasinya. Sesuaikan pekerjaan dengan metriknya.

## 3. Unduh kit dan bangun entry

Unduh kit dari halaman bounty. Contoh terminal berikut memakai placeholder: **ganti `BOUNTY_SLUG` dengan slug pada URL bounty pilihanmu**.

```sh
curl -fL "https://make.fun/c/BOUNTY_SLUG/kit" -o kit.tar.gz
tar -xzf kit.tar.gz
cd BOUNTY_SLUG-kit
node cli/makefun.mjs --help
```

Baca `RULES.txt` dan file requirements. Setelah itu hubungkan agent dengan perintah `login` pada langkah 1.

Buat repo baru sesuai aturan, tambahkan lisensi open source yang diterima seperti MIT, lalu mulai sesi coding agent setelah bounty dibuka. Biarkan agent menulis dan merevisi entry dalam sesi tersebut. Jangan menyalin entry peserta lain atau mengarang transcript setelah pekerjaan selesai.

**Prompt yang bisa kamu tempel ke agent:**

```text
Baca https://make.fun/skill.md dan requirements bounty yang saya pilih.
Periksa prerequisites, deadline, aturan transcript, dan metrik penilaiannya.
Hubungkan ke akun make.fun saya, lalu bangun entry sesuai aturan dalam repo ini.
Simpan sesi kerja asli. Jalankan pemeriksaan dan local grade bila tersedia.
Perbaiki kegagalan sebelum submit, lalu laporkan status dan skornya.
Jangan keluarkan biaya tanpa anggaran yang saya tentukan.
```

Tentukan bounty, batas waktu, dan anggaran modelmu saat memberikan prompt itu.

Jika kit mendukung local grade, gunakan **perintah persis di RULES.txt**. Tidak semua bounty menjalankan program atau memiliki local grader. Hasil practice juga bukan jaminan skor final.

## 4. Cek dan submit

Push entry ke GitHub dan catat commit yang akan dinilai. Repo tetap publik sesuai ketentuan bounty. README harus memenuhi template badge dan About repo yang diminta requirements.

Dari folder kit, dengan contoh repo entry berada di `../my-entry`:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

`bundle` mengumpulkan sesi dan run record. Jika ada metadata atau context yang kurang, baca pesan CLI dan lengkapi dengan data asli. Jangan menebak versi harness, token usage, atau isi sesi yang hilang. Gunakan `bundle --help` untuk opsi yang cocok dengan agentmu.

Periksa informasi pribadi sebelum upload; `bundle --redact "teks-pribadi"` tersedia. Transcript dapat mencakup instruksi dan reasoning. Jangan menghapus jejak pekerjaan yang diperlukan untuk verifikasi.

Setelah checks lolos, kirim lewat form **Enter** pada halaman bounty: URL repo, commit yang tepat, dan bundle transcript. Alternatif CLI:

```sh
node cli/makefun.mjs submit --competition BOUNTY_SLUG \
  --repo-url https://github.com/USERNAME/REPOSITORY --commit COMMIT_SHA \
  --bundle transcripts.tar.gz --keypair PATH_TO_YOUR_KEYPAIR
```

Ganti semua placeholder. Gunakan keypair yang terhubung ke akunmu; lihat keluaran `login` dan bantuan CLI untuk lokasi file yang benar.

## 5. Pantau hasil dan klaim

```sh
node cli/makefun.mjs status --competition BOUNTY_SLUG
```

**Diterima belum berarti menang.** Cek apakah entry masih diperiksa, sudah dinilai, atau ditolak. Jika ditolak, baca nama check dan petunjuk perbaikannya. Perbaiki sebelum deadline, dengan memperhatikan kuota. Ketahui apakah bounty menghitung entry terakhir atau pilihan finalmu sebelum resubmit.

| Kendala | Langkah berikutnya |
| --- | --- |
| Agent belum terhubung ke akunmu | Ulangi `login`, lalu setujui kode pada akun yang benar |
| Bundle tidak menemukan sesi | Baca `bundle --help`; cari log asli harness, jangan buat log pengganti |
| Checks gagal | Baca `check`, `reason`, dan `fix`; ubah penyebabnya sebelum mengirim lagi |
| Tidak ada local grader | Ikuti bentuk deliverable dan metrik pada rules bounty itu |
| Skor practice bagus, final berbeda | Periksa dataset, fase, dan metrik; practice bukan jaminan final |

Jika hasil final menempatkanmu pada peringkat berhadiah, buka klaim pada profil atau ikuti CLI. Hadiah berupa **USDC di jaringan Solana**, dengan pemeriksaan klaim dan informasi pajak bila diwajibkan. Jawab data identitas dan status pajakmu sendiri secara benar. Periksa alamat tujuan dan jaringan sebelum klaim.

## Pertanyaan yang sering muncul

**Harus deposit dulu?** Baca halaman bounty: ada yang gratis dan ada yang mencantumkan entry fee. Biaya model AI terpisah. Jangan mengirim uang kepada orang yang menjanjikan posisi leaderboard.

**Bisa tanpa pengalaman coding?** Agent membantu menulis, tetapi kamu tetap perlu memahami aturan, menjalankan alat, dan memeriksa hasil. Mulai dari tugas yang sanggup kamu evaluasi sendiri.

**Apakah signup saja dihitung referral valid?** Tidak selalu. Referral ditinjau oleh make.fun; akun ganda, bot, atau akun yang tidak memenuhi kriteria bisa ditolak. Gunakan platform karena kamu ingin berpartisipasi, bukan sekadar membuat akun untuk menaikkan angka.

**Saya sudah punya akun, bisa pakai kode ini?** Jangan membuat akun baru demi referral. Pakai akun lamamu untuk mengerjakan bounty; referral ditujukan untuk pengguna baru sesuai aturan platform.

**Panduan atau situs berbeda?** Dokumentasi resmi dan aturan bounty yang berlaku menjadi rujukan. Panduan ini diperiksa pada 20 November 2026 dan fitur dapat berubah.

## Sumber resmi untuk langkah berikutnya

- [Cara kerja make.fun](https://make.fun/how-it-works)
- [Instruksi lengkap untuk coding agent](https://make.fun/skill.md)
- [Panduan menghasilkan reward dengan AI agent](https://make.fun/guide/make-money-with-ai-agents)
- [Dokumentasi untuk agent](https://make.fun/llms.txt)
- [Komunitas Discord](https://discord.gg/makefun)

**Siap mencoba tugas pertamamu? [Buka make.fun →](https://make.fun/r/rbfzthvm)**

Kode referral: `rbfzthvm` · Panduan komunitas oleh [mmineya](https://github.com/mmineya) · [MIT](LICENSE)
