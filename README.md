# WebLab - Tugas Individu 3

**Nama:** Gohan Tua Jeremia Ambarita  
**NIM:** 123140160  
**Kelas:** ISI KODE KELAS  
**Mata kuliah:** Pengembangan Aplikasi Web

Aplikasi simulasi pendaftaran workshop menggunakan HTML dan CSS. Dibuat sesuai instruksi pada halaman 51 materi Pertemuan 4.

## Berkas

| Berkas | Fungsi |
| --- | --- |
| `index.html` | Halaman formulir pendaftaran dengan metode GET |
| `detail.html` | Halaman detail pendaftar dengan data dummy |
| `style.css` | Gaya kedua halaman, Grid, Flexbox, tabel, dan media query |
| `screenshots/` | Screenshot hasil render aplikasi pada desktop dan ponsel |

## Menjalankan

1. Buka `index.html` dengan Chrome, Edge, atau Firefox.
2. Isi data contoh. NIM harus berisi 9 angka. Kolom bertanda `*` wajib diisi.
3. Pilih program studi, semester, sesi, dan persetujuan.
4. Tekan **Lihat detail**. Browser akan membuka `detail.html` dengan query string.
5. Gunakan **Kembali ke formulir** untuk membuka halaman pertama.

Opsional, jalankan server lokal dari folder `task_3`:

```bash
python -m http.server 8000
```

Kemudian buka `http://localhost:8000`.

## Perilaku sesuai instruksi

```html
<form id="form-pendaftaran" class="card" action="detail.html" method="get">
```

Atribut `name` dan `value` pada form membentuk query string. Contoh:

```text
detail.html?nama=Gohan+Tua+Jeremia+Ambarita&nim=123140160&prodi=Informatika&sesi=Pagi&minat=HTML&minat=CSS
```

`detail.html` menampilkan nilai yang ditulis tetap dalam HTML. Sesuai tugas, aplikasi **tidak membaca query string, tidak menyimpan data, dan tidak menggunakan JavaScript atau backend**. Email, telepon, tanggal lahir, program studi, semester, dan pilihan workshop pada contoh merupakan dummy. Gunakan data contoh saat mencoba form.

## Selector CSS

- Elemen: `body`, `fieldset`, `th`, `td`.
- Class: `.card`, `.form-grid`, `.button`.
- ID: `#form-pendaftaran .form-bottom`.
- Atribut: `input[type="radio"]` dan `input[type="checkbox"]`.
- Pseudo-class: `:hover`, `:focus`, `:focus-visible`, `:nth-child(even)`.

Layout menggunakan Grid dan Flexbox, dengan media query pada 1050px dan 760px. Tabel menggunakan `rowspan`, `colspan`, border-collapse, pola zebra, efek hover, dan kontainer gulir horizontal pada ponsel.

## Hasil pemeriksaan

16 pemeriksaan browser lulus: pemuatan HTML/CSS, metode GET, validasi form, pola NIM, format email, query string, parameter checkbox berulang, penggabungan sel tabel, data dummy yang tetap, tautan kembali, tombol reset, layout mobile, dan ketiadaan script.

Screenshot desktop diambil pada viewport 1280 x 1000, sedangkan screenshot ponsel pada 390 x 844. Penjelasan setiap bagian kode beserta nomor baris terdapat pada laporan PDF dan Word.

## Pengumpulan GitHub

1. Tambahkan folder `task_3` ini ke repositori mata kuliah kamu. Letaknya di root repositori, bukan di dalam folder `task_3` lain.
2. Isi kelas pada README dan laporan Word.
3. Isi link repositori pada sampul laporan. Gunakan URL folder `task_3`, misalnya pola `https://github.com/USERNAME/REPOSITORI/tree/main/task_3`. Sesuaikan nama branch bila berbeda.
4. Ekspor laporan Word yang telah dilengkapi menjadi PDF.
5. Ganti awalan `KELAS` pada nama PDF dengan kode kelas yang benar.

Format pengumpulan: `kelas-Nama-Nim-Tugas3-Pemweb.pdf`.

Profil GitHub pembuat: https://github.com/14-123140160-GohanTuaJeremiaAmbarita

**URL repositori tugas:** ISI URL REPOSITORI DAN FOLDER task_3 SEBELUM DIKUMPULKAN.
