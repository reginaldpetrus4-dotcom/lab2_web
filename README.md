Membuat dokumen HTML

Menggunakan < !DOCTYPE > untuk memberi tahu browser bahwa dokumen yang akan dibuat menggunakan HTML, kalo < html > adalah elemen utama yang membungkus seluruh halaman, < head > itu berisi informasi tentang halaman seperti judul, link CSS, dan metadata. title yaitu untuk menambahkan judul

<img width="1919" height="1132" alt="ss 1" src="https://github.com/user-attachments/assets/4e9cc598-88d7-4169-a180-be35e6ada1c7" />

Mendeklarasikan CSS

- body: menentukan jenis huruf utama untuk seluruh halaman menggunakan font open sans

- header: memberi bagian atas halaman dengan tinggi minimal 80px dan garis bawah tipis berwarna biru muda

- h1: mengatur tampilan elemen judul utama Berukuran 24px (besar), Berwarna biru tua, Berada di tengah (center), Memiliki jarak ruang di sekelilingnya (padding).

- h1 i: Mengubah warna teks miring < i > di dalam judul < h1 > menjadi abu-abu gelap.

<img width="1919" height="1134" alt="ss 2" src="https://github.com/user-attachments/assets/926f564d-f09a-4589-b727-3f49eee90350" />


Menambahkan Inline CSS

Menambahkan deklarasi inline CSS pada tag < p >

- text-align: center;: Membuat teks di dalam paragraf tersebut menjadi rata tengah (center).

- color: #ccd8e4;: Mengubah warna teks paragraf menjadi biru muda/abu-abu terang (#ccd8e4).

<img width="1919" height="1134" alt="ss 3" src="https://github.com/user-attachments/assets/dce86ec2-a632-4ee3-88a9-76fedb4c9782" />

Membuat CSS Eksternal

1. Pengaturan Navigasi (nav)
   
- background: #20A759;: Memberi latar belakang navigasi warna hijau tua.
  
- color: #fff;: Menetapkan warna teks utama di navigasi menjadi putih.

- padding: 10px;: Memberi jarak kosong 10px di sekeliling konten navigasi.
  
2. Pengaturan Tautan di Navigasi (nav a)
   
- color: #fff;: Membuat warna teks tautan tetap putih.
  
- text-decoration: none;: Menghilangkan garis bawah pada tautan.
  
- padding: 10px 20px;: Memberi jarak kosong 10px di atas/bawah dan 20px di kiri/kanan setiap tautan, membuatnya terlihat seperti tombol.
  
3. Efek Interaksi (nav .active, nav a:hover)
   
- nav .active, nav a:hover { ... }: Mengatur tampilan ketika tautan aktif (menggunakan kelas .active) atau ketika kursor diarahkan ke tautan (:hover).
  
- background: #0B6B3A;: Mengubah latar belakang tautan menjadi warna hijau yang lebih gelap saat kursor diarahkan atau saat tautan sedang aktif.
  
- Menggunakan (Tag ) Untuk menerapkan tag link, file HTML harus "memanggil" file CSS tersebut menggunakan tag < link > di dalam bagian < head >:
  
< link rel="stylesheet" href="style_eksternal.css" ... >: Ini memberitahu browser untuk mengambil dan menggunakan semua aturan gaya dari file style_eksternal.css pada halaman HTML tersebut.
<img width="1919" height="1132" alt="ss 4" src="https://github.com/user-attachments/assets/99fea138-8186-4ef6-8175-fa898638cd37" />

Menambahkan CSS Selector

1. ID Selector ( #intro )
   
- Mengatur area konten utama (ID: intro).

- Memberi latar belakang biru, garis tepi hijau, dan tinggi minimum 100px.

- Mengatur judul < h1 > di dalamnya agar rata kiri dan berwarna putih.

2. Class Selector ( .button )
   
- Membuat gaya dasar untuk tombol.
  
- Memberi padding (ruang dalam), latar belakang abu-abu, teks putih, dan menghilangkan garis bawah tautan.
  
3. Modifikasi Class ( .btn-primary )
   
- Kelas tambahan untuk membuat tombol "utama".
  
- Hanya mengganti warna latar belakang tombol menjadi merah (menimpa warna abu-abus standar).
<img width="1920" height="1080" alt="495207106-b77d71fe-0ecf-438e-93c9-23f7a57d9f10" src="https://github.com/user-attachments/assets/3cf616df-d8c4-4227-9227-e130babcc93f" />

Pertanyaan dan Tugas

1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.

2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!

3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!

4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! < p id=paragraf-1" class="text-paragraf" >

Jawaban
1. Menggunakan border-radius untuk mengubah bentuk radius sebuah blok
   
<img width="1920" height="1080" alt="495210822-6b2e04fe-94c7-43ad-95eb-eaf4dc454e65" src="https://github.com/user-attachments/assets/beb931c7-ba73-4f88-af62-fffc0ec9f892" />

2. h1 adalah aturan umum untuk semua judul level 1. Sedangkan #intro h1 adalah aturan spesifik yang hanya berlaku jika judul level 1 tersebut berada di dalam container #intro.

3. Jika ada elemen yang sama dideklarasikan menggunakan CSS Internal, Eksternal, dan Inline, maka yang akan ditampilkan oleh browser adalah Inline CSS. Ini adalah aturan Spesifisitas dan Urutan Cascading CSS: Inline CSS memiliki prioritas tertinggi karena berada langsung di dalam elemen. Di bawah itu, CSS yang terakhir dimuat (baik Eksternal maupun Internal) akan diutamakan, tetapi biasanya Inline selalu menang dari Internal/Eksternal.

Contoh: Misalnya memiliki elemen < p >:

Lokasi CSS Aturan CSS Eksternal/Internal p { color: green; } Inline CSS < p style=color: blue;" >Ini paragraf.< /p > Hasil: Teks paragraf akan berwarna BIRU karena Inline CSS menimpa aturan yang lebih umum (Eksternal/Internal).
<img width="905" height="848" alt="495214424-3a4a1810-1a40-4943-9906-b21577ffa09f" src="https://github.com/user-attachments/assets/0dfa0b05-5cb6-4e68-a852-6bf4cb8bff8d" />
4. Apabila sebuah elemen memiliki ID dan Class yang masing-masing mendeklarasikan properti yang sama, maka deklarasi dari ID Selector akan ditampilkan (ditampilkan dalam hal ini berarti ID akan menimpa Class).

ID Selector (#) memiliki Spesifisitas lebih tinggi daripada Class Selector (.).

Contoh: Misalnya Anda memiliki elemen <p id=paragraf-1" class="text-paragraf"> dan deklarasi CSS ini:

Selector Deklarasi CSS Class .text-paragraf { color: red; } ID #paragraf-1 { color: blue; } Hasil: Teks paragraf akan berwarna BIRU. Meskipun kedua aturan berlaku, ID Selector lebih "spesifik" (nilai spesifisitas ID = 100, Class = 10), sehingga aturan warna birunya yang akan diterapkan.

<img width="887" height="856" alt="495219141-930e5c45-68ba-4f31-9d42-808c583ed61e" src="https://github.com/user-attachments/assets/8b3a0304-17c8-494c-b43d-80024b4d31f2" />
