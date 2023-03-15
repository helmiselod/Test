<style>
	div{
	text-align:justify;
	}
	h6{
	text-align:center;
	}
</style>
<div>

# PENGENALAN AUTOMATA

**Objektif:**

1. Mahasiswa Mampu Memahami Konsep Dasar Automata.

2. Mahasiswa Mampu Menggunakan Aplikasi JFLAP. 

------

**1.1 Dasar-dasar Automata**

​	Teori automata adalah pembelajaran tentang alat komputasi atau mesin. Automata ditemukan oleh Alan Turing. Tujuan Turing mempelajari automata adalah untuk mendeskripsikan secara tepat tentang apa yang dapat dan tidak dapat dilakukan oleh mesin komputasi. Pada antara tahun 1940 – 1950an, terdapat sebuah mesin sederhana yang sekarang disebut *finite automata.* Mesin ini mirip fungsi otak manusia yang berfungsi untuk banyak tujuan. Pada akhir tahun 1950an, seorang Ahli Bahasa yang bernama Noam Chomsky mempelajari bahasa formal Grammar. Grammar ini memiliki hubungan dekat dengan automata yang merupakan basis utama komponen penting *software,* termasuk *compiler.*

Berikut beberapa alasan mengapa harus mempelajarai automata:

- Aplikasi untuk mendesain dan memeriksa keadaan atau kondisi dari sebuah sirtkuit *digital*.
- *Lexical analyzer*, yaitu komponen *compiler* yang memecah *input* teks menjadi bentuk unit *logical* seperti gambar, *identifier*, kata kunci, dan tanda baca.
- Aplikasi untuk memindai dokumen teks yang berukuran besar seperti koleksi dari halaman web
- Aplikasi utnuk memverifikasi sistem yang mengandung keadaan atau *state* dalam jumlah terbatas.



​	Contoh sederhana dari *finite automata* yaitu ketika menentukan suatu kondisi lampu jika ditekan tombolnya lampu tersebut bisa menyala atau mati dan suatu mesin untuk menerima *input* teks seperti kamus *online*.

​	Pada gambar dibawah terlihat terdapat dua *state* yaitu *state* mati dan *state* nyala, kedua *state* menandakana lampu mati atau menyala jika kita menekan salah satu tombol. Dari gambar diatas menjelaskan bahwa automata memiliki fungsi sebagai *state* yang menandakan suatu keadaan tertentu.

<img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220324145313262.png" style = "zoom:100%;"/>

###### Gambar 1.1 Contoh Kondisi Lampu



​	Selain itu automata juga berfungsi untuk menerima *input* *string*. Bisa dilihat pada gambar dibawah terdapat automata yang menerima *input string* berupa huruf atau alfabet. Jika *input string* tersebut disusun maka akan menjadi sebuah kata tertentu. Salah satu fungsi automata yang sudah sering digunakan dengan menerima *input string* yaitu google *translate*.

<img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220324150026110.png" style = "zoom:100%;">

###### Gambar 1.2 Kondisi Automata Menerima *Input String*



Automata sendiri memiliki notasi representasi struktural, yaitu:

- *Grammar*. Automata memiliki susunan grammar tertentu, seperti grammar pada Bahasa Inggris yang mengenal *noun*, *verb*, *adjective*, atau *grammar* pada Bahasa Indonesia yang mengenal subjek, predikat, objek, dan keterangan. *Grammar* pada automata adalah model untuk mendesain proses data dengan struktur rekursif. Contoh penggunaan *grammar* automata adalah “parser”, yaitu komponen *compiler* yang menangani perulangan bersarang pada Bahasa pemrograman tertentu. 
- *Regular Expression.* Ekspresi regular juga menotasikan struktur data, terutama *string*. Ekspresi regular pada umumnya berbentuk dari susunan huruf “[A - Z] [a - b] * [ ] [A – Z][A - Z]“.



**1.1.1 Himpunan**

​	Himpunan adalah kumpulan dari objek-objek. Dalam automata, objek yang dimaksud adalah suatu *state* atau keadaan tertentu yang terkumpul menjadi himpunan. Himpunan dapat dituliskan sebagai: X = {a, b, c, d}.

Beberapa operasi yang ada pada himpunan:

- Gabungan

  Himpunan gabungan adalah penggabungan dari dua atau lebih himpunan. Himpunan gabungan dilambangkan dengan notasi ∪.

  Contoh:

  A = {1, 2, 3, 4, 5}				B = {6, 7, 8, 9, 10}

  A ∪ B = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}

- Irisan

  Himpunan irisan adalah himpunan yang berisikan anggota yang sama antara dua atau lebih himpunan. Himpunan irisan dilambangkan dengan notasi ∩.

  Contoh:

  A = {1, 2, 3, 4, 5}				B = {1, 3, 5, 7, 9}

  A ∩ B = {1, 3, 5, 7}

- Beda Simetris

  Himpunan beda simetris adalah himpunan yang berisikan anggota dari dua atau lebih himpunan yang tidak mengandung anggota yang sama dari himpunan tersebut. Himpunan beda simetris dilambangkan dengan notasi ⊕.

  Contoh :

  A = {1, 2, 3, 4, 5} 				B = {2, 4, 6, 8, 10}

  A ⊕ B = {1, 3, 5, 6, 8, 10}

- Komplemen

  Himpunan komplemen adalah himpunan yang anggotanya bukan merupakan anggota dari himpunan tersebut, tapi terdapat di himpunan semesta. Himpunan komplemen dilambangkan dengan notasi ` atau c
  
  Contoh:
  
  U = {1, 2, 3, 4, 5, . . . 10}
  
  A = {1, 2, 3, 4, 5}				B = {2, 4, 6, 8, 10}
  
  A' = Ac = {4, 5, 6, 7, 8, 9, 10}
  
  B' = Bc = {1, 3, 5, 7, 9}

**1.1.2 Relasi dan Fungsi**

​	Relasi adalah penggambaran interaksi atau koneksi antara elemen dari dua buah himpunan atau lebih. Dalam automata, relasi menggambarkan hubungan antara masing-masing *state* yang terhubung dengan suatu *input* atau tidak.

Sifat-sifat relasi:

- Refleksif

  Suatu relasi R pada himpunan A dinamakan bersifat refleksi jika (a, a) ∈ R untuk setiap a ∈ A.

  Contoh:

  A = {1, 2, 3, 4, 5} terdapat relasi R yaitu ≥ yang didefinisikan pada himpunan A, maka:

  R = {(1, 1), (2, 1), (2, 2), (3, 2), (3, 3), (4, 3), (4, 4), (5, 4), (5, 5)}

  Terdapat relasi (1, 1), (2, 2), (3, 3), (4, 4), (5, 5) yang merupakan ∈ R. Maka relasi ini bersifat refleksi.

- Simetris

  Suatu relasi pada himpunan A bersifat simetris jika (a, b) ∈ R, untuk setiap a dan b ∈ A, dan (b, a) ∈ R. Suatu relasi bersifat tidak simetris jika (a, b) ∈ R, namun (b, a) ∉ R.

  Contoh:
  
  Terdapat relasi R = {(1, 2), (1, 3), (1, 4), (2, 1), (2, 3), (2, 4), (3, 1), (3, 2), (3, 4), (4, 1), (4, 2), (4, 3)}
  
  Terdapat relasi (1, 2), (2, 1), (1, 3), (3, 1), (1, 4), (4, 1), (2, 3), (3, 2), (2, 4), (4, 2), (3, 4), (4, 3) . Maka relasi ini bersifat simetris
  
- Antisimetris

  Suatu relasi pada himpunan A bersifat antisimetris apabila setiap a, b ∈ A, (a, b) ∈ R, dan (b, a) ∈ R, jika a = b.

  A = {1, 2, 3, 4} terdaoat relasi R yaitu ≥ yang didefinisikan pada himpunan A, maka:

  R = {(1, 1), (2, 2), (2, 1), (3, 3), (3, 2), (3, 1), (4, 4), (4, 3), (4, 2), (4, 1)}

  Apabila a ≥ b, dan b ≥ a, berarti a = b. Maka relasi ini bersifat antisimetris.

- Transitif

  Suatu relasi pada himpunan A bersifat transitif apabila (a, b) ∈ R dan (b, c) ∈ R, maka (a, c) ∈ R untuk a, b, c ∈ A.

  Contoh:

  A = {2, 4, 6, 8} terdapat relasi R yaitu < yang didefinisikan pada himpunan A, maka:

  R = {(2, 4), (2, 6), (2, 8), (4, 6), (4, 8), (6, 8)}

  Terdapat relasi (2, 4), (4, 6), dan (2, 6), relasi (2, 6), (6, 8), dan (2, 8). Maka relasi ini bersifat transitif.

​	Fungsi adalah relasi dari masing-masing anggota himpunan domain yang hanya mempunyai satu bayangan di himpunan kodomain.

Macam-macam jenis fungsi:

- Fungsi Satu-satu

  Fungsi satu-satu adalah fungsi yang masing-masing anggota hanya memiliki satu bayangan pada himpunan domain dan kodomainnya. Fungsi ini hanya berlaku jika jumlah anggota domain dan kodomainnya sama.

  Contoh:

  X = {RPG, Shooter, Sport}

  Y = {Skyrim, Point Blank, PES2021}

  Fungsi f: X → Y
  
  <img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220303213816530.png" style = "zoom:70%;"/>
  
  ###### Gambar 1.3 Fungsi satu-satu
  
  
  
- Fungsi Pada

  Fungsi pada adalah fungsi yang setiap anggota himpunan kodomain merupakan bayangan dari minimal satu dari himpunan domain.

  Contoh:

  X = {darat, laut, udara}

  Y = {motor, mobil, kapal, perahu, pesawat}

  Fungsi f: X → Y

  <img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220303214503920.png" style = "zoom:70%;"/>

  ###### Gambar 1.4 Fungsi pada

  

- Fungsi Konstan

  Funsi konstan adalah fungsi yang satu anggota dan himpunan kodomain menjadi bayangan dari semua anggota domain.

  Contoh:

  X = {tahu, tempe, telur, susu, brokoli}

  Y = {protein, karbohidrat}

  Fungsi f: X → Y

  <img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220303215105418.png" style = "zoom:70%;" />

  ###### Gambar 1.5 Fungsi konstan



**1.1.3 Graph dan Tree**

​	Graph dan Tree merupakan dasar dari automata, karena automata mirip dengan graph berarah, namun memiliki *input*. Suatu graph terdiri dari *vertex*, sejumlah *edge*, dan fungsi yang menunjukkan hubungan antara *vertex* dan *edge*. Ketiga komponen ini dapat ditulis G = {V, E, y}.

Contoh:

Terdapat graph dengan *vertex* = {P, Q, R, S} dan *edge* = {a1, a2, a3, a4, a5} dan

y didefinisikan dengan: 	

y (a1) = {P, Q}

y (a2) = {P, R}

y (a3) = {Q, R}

y (a4) = {Q, S}

y (a5) = {R, S}



Maka graph tersebut:

<img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220303215946847.png" style = "zoom:70%;" />

###### Gambar 1.6 *Graph* 



Fungsi yang menunjukkan hubungan antara *vertex* dan *edge* mirip dengan fungsi transisi pada *finite automata*.



Pohon adalah sebuah *graph* yang tidak memiliki *cycle* atau putaran.

Contoh:

<img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220303220027130.png" style = "zoom:70%;"/>

###### Gambar 1.7 Pohon



**1.1.4 Alfabet**

​	Alfabet adalah sebuah karakter atau simbol. Dalam *finite* automata, alfabet adalah himpunan karakter atau simbol. Himpunan alfabet dalam automata disimbolkan dengan ∑.

Contoh:

∑ = {0, 1, 2, . . . . 100}

∑ = {a, b, c, d, . . . . z}

∑ = {himpunan karakter ASCII}

**1.1.5 *String***

​	*String* adalah kumpulan dari beberapa alfabet. Suatu mesin automata dapat menolak atau menerima *input string* yang diberikan, selain itu mesin automata juga dapat menerima *input string* kosong yang disebut ℇ-*Non Deterministic Finite Automata*.

Contoh:

1. ∑ = {0, 1, 2}, maka *string* yang dibentuk yaitu:

   00, 101, 0101012, 100101, . . . .

   *String* memiliki panjang yaitu banyaknya alfabet yang membentuk *string* dan di notasikan dengan | |.

2. |001120| = 6

   Sebuah *string* dapat juga sebagai operasi perpangkatan dari alfabet.

3. ∑ = {0, 1}, maka:

   ∑1 = {0, 1}		

   ∑2 = {00, 01, 10, 11}

   ∑3 = {000, 001, 010, 011, 100, 101, 110, 111}

   ∑0 = {ℇ}

​			

​	Suatu *string* dapat digabungkan dengan *string* lain. Himpunan seluruh alfabet dalam ∑ dapat di notasikan dengan ∑*. * dalam notasi tersebut disebut *kleene star*. Himpunan seluruh alfabet tanpa ℇ *string* dinotasikan dengan ∑+.

∑* = Alfabet bisa muncul seluruhnya dan bisa tidak muncul dalam suatu *string*

∑+ = Alfabet muncul minimal satu kali dalam suatu *string*

​	Konkatenasi *string* adalah penggabungan dari *string*. Jika terdapat *string* p dan *string* q, maka pq merupakan hasil konkatenasi *string* tersebut.

Contoh:

1. p = beli				q = buku

   Maka:

   pq = belibuku

   qp = bukubeli

2. ∑ = {0, 1}, maka:

   ∑* = {ℇ, 00, 11, 100, 001, . . . .}

   ∑+ = {00, 11, 100, 101, 10101, 111, . . . .}

3. Tuliskan *string* yang dihasilkan dari:

   (0, 1)*11(0)+

   Maka, *string* yang dihasilkan = {110, 01100, 1110, 01110, . . . .}

4. Tuliskan *string* yang dihasilkan dari:

   {a, ab}* 

   Maka, *string* yang dihasilkan = {ℇ, a, ab, aab, aaab, aaaab, . . . .}

**1.1.6 Bahasa**

​	Bahasa pada automata adalah ruang lingkup atau ketentuan dari suati *string*.

Contoh:

1. ∑ = {0, 1}

   Sebuah mesin automata hanya bisa menerima *input* *string* yang memenuhi bahasa L = {diawali *input* 0 dan diakhiri *input* 1}. Maka:

   *String* yang diterima adalah {01, 00001111, 0 . . . . 1} jika dinotasikan maka L = 0(01)*1.

2. ∑ = {0, 1}

   Sebuah mesin automata hanya bisa menerima *input* *string* yang memenuhi bahasa L = {*input* 0 berjumlah genap dan *input* 1 berjumlah ganjil}. Maka:

   *String* yang diterima adalah {001, 00111, 00001, 0000111, . . . .} jika dinotasikan maka L = (00)+1(11)*
   
3. ∑ = {x, y}

   Tedapat bahasa L = {xnyn: n > 0}. Periksa apakah *string* xxyy, xy, xxxyy termasuk di bahasa tersebut?

   xxyy	 -> jumlah x = 2, jumlah y = 2. Memenuhi Bahasa tersebut karena jumlah x dan y sama 

   xy 		-> jumlah x dan jumlah y = 1. Memenuhi Bahasa tersebut karena jumlah x dan y sama 

   xxxyy   -> jumlah x = 3, jumlah y = 2. Tidak memenuhi Bahasa tersebut karena x dan y tidak sama 

4. ∑ = {x, y, z} 

   Terdapat bahasa L = {xy, z}. Tentukan L3 DAN L0! 

   Maka, L3 adalah 3 kata dari Bahasa tersebut 

   L3 = {xyxyxy, xyxyz, xyzxy, xyzz, zxyxy, zxyz, zzxy, zzz} 

   L0 = kata kosong λ 



**1.2 Pengenalan dan Instalasi JFLAP**

​	JFLAP adalah aplikasi yang digunakan untuk merancang Bahasa formal termasuk NFA(non deterministic finite automata), DFA (Deterministic Finite Automata), Pushdown Automata, Mealy Machine, Moore Machine, Turing Machine, dan beberapa tipe grammar. JFLAP menggunakan bahasa pemrograman java dan memiliki ekstensi .jar.

<img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220303205846324.png" style = "zoom:70%;" />

###### Gambar 1.8 JFLAP



Jika memilih menu *Finite Automaton* maka akan muncul tampilan awal pada JFLAP seperti berikut ini.

<img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220303220239302.png" style = "zoom:50%;" />

###### Gambar 1.9 Tampilan Awal JFLAP



​	Pada tampilan awal terdapat menu awal yaitu *File, Input, Test, View, Convert* dan *Help*. Pada menu *File* terdapat beberapa sub menu lagi seperti yang ada pada gambar berikut.

<img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220303220331041.png" style = "zoom:50%;" />

###### Gambar 1.10 Menu *File* JFLAP



​	Pada menu *Input* juga terdapat beberapa sub menu yang berfungsi untuk menguji suatu *string* dari automaton tersebut dapat diterima atau tidak, selain itu juga dapat diketahui langkah-langkah pengecekan pada bagian sub menu ini.

<img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220303220359371.png" style = "zoom:50%;" />

###### Gambar 1.11 Menu *Input*



​	Pada menu *Test* terdapat pilihan untuk menampilkan transisi yang merupakan *nondeterministic* atau transisi yang mengandung ℇ *string*.

<img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220303220422757.png" style = "zoom:50%;"/>

###### Gambar 1.12 Menu *Test* JFLAP



​	Pada tampilan menu *View* terdapat beberapa pilihan yang ada pada sub menunya. Menu ini berfungsi untuk melihat suatu algoritma tertentu pada automaton.

<img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220303220452815.png" style = "zoom:50%;" />

###### Gambar 1.13 Menu *View* JFLAP



​	Pada menu *Convert* digunakan untuk konversi *Nondeterministic Finite Automata* (NFA) menjadi *Deterministic Finite Automata* (DFA), untuk meminimasi DFA yang memiliki banyak *state*, konversi grammar ke ekspresi *regular* atau sebaliknya dan untuk menggabungkan dua atau lebih mesin automaton pada JFLAP.

<img src = "C:\Users\gilan\AppData\Roaming\Typora\typora-user-images\image-20220303220517431.png" style = "zoom:50%;" />

###### Gambar 1.14 Menu *Convert* JFLAP



​	Selain terdapat beberapa menu yang di setiap menunya ada sub menu, pada JFLAP juga terdapat beberapa *icon* yang dapat digunakan untuk membuat atau menggambar automaton.

###### Tabel 1.1 Fungsi *Icon* JFLAP

| Icon                                                         | Fungsi                                                       |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| ![img](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADEAAAA3CAYAAAClxaIBAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAAFiUAABYlAUlSJPAAAAKfSURBVGhD7Zk9ixNBGMdn9uJ5yKkXEPWKA0GsFGtb0cZCuzQWWohfQ7+BVxtRsBEs7Qz4AQSxshDhNi8igsUletjl5dyZ7D/8d3h2TZa8zC75wY/532Z2kifz7IZc9Mfw6FgVnCAeC826CF/QxxFxLix6NBoVv4jhcFj8IgaDQfmKePLsZZz85NGD+3b88O6NHQ263+8nini6/0o9fjie6BMvXo9ftHltl85vq3q9rmq1mqpWqyowNyfWsBFo7wScgfg54S7gg4AzKMdOlKKIeEwQRBN9E3AG63ZapoAzWN+dlingDOZexGZlY6L0eF4BZ5DSTkFuDVprq/R4XgFnIO7EMPqKkVcXaU4eAWew0CLGuzFWmjuLgDNY+E6gtTYrgTh/WgFnIF4T7gKzmIU0f1oBZ7DwnQBmN7a3KlbpvP8JOAOxCPO/g7xmgdY6e+qEeG6WgDNYajsx0rlZAs5gae3EmN04d+akVVpDEnAGKynCgNa6sLMlruMKOIOVtRMjreMKOIOV7ESe5wOcgXx3isa8uvC6TPPX34nSOq6AMyjv3cl9F2aRMet9+3lkxdoGc0Ff2T1tldaQBJyBXERUbV4NWOvrjz+J4xJ8bpaAMxDbyX0XZpFJO87wnCwBZ5DSTvn98v33RPc4Pwc+J67u7STmpQk4g7m3U5ZpSHNdAWcw93bKMg1privgDJa6E5/DQys/n/lbmusKOIO5XxPT+OngcKL0uCTgDFKKiKr3TMAZyNdEVK5vAs6gHDtRiiLiMcFo5J+AM9CdTidR2vO37+PkJ7fv3FM3r120v54C3W63E0U0Gg11+cZddev6bnzET3q9nh3tT8A2OUh95yumGN1qtYrzilPQzWaz8EWI7VQ0dBiGxW+nbrdb8CKU+gerv8TPWPE8IwAAAABJRU5ErkJggg==) | Pointer penunjuk untuk memindahkan state Mengubah bentuk garis transisi Mengubah nama state |
| ![img](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACsAAAAzCAYAAAAO2PE2AAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAAFiUAABYlAUlSJPAAAAFNSURBVGhD7ZldEoIgFEahHeje3IJ70i24kTaB7kBnevanoG5zh8mUgOSCZ4a0GarTx0c9wK/itjAi8OXB6z54+DzPdGSnaaIjO44jHdmqqoKVLYpCXZumUVfW973cY0EhA5QDkPfSk8uHLMvYMAxP+wCAJMuyVNe6rlXKF/WMCKesL05ZX6Qlm+f55nBF/Mni1B5/KpsDz7fBWFYX3AOebyMdZw0gkb1proETNiX+DXYUm7J4+W0rgIEqmNTBWbLwwaYCJqTbWddV0XEq+6kCLiuRZg2gAnoNXNbCW7I+fhXiqgEsrUlS8JpvFZDvtTVHJ80N9g92y8KS2W4aqJPJ8gPGyYIwjD3g+fClfyH+zkI6esprA8+3wTpZLLI2XBF/DY7ilPUFKdmgj5bwAYjkfVoTMnCSpGTVHQF413V0ZNu2JSNL69dACEEkWcbuoZuN7RMF83MAAAAASUVORK5CYII=) | Menambahkan state baru                                       |
| ![img](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACgAAAA0CAYAAAD46nqNAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAAFiUAABYlAUlSJPAAAAD7SURBVGhD7ZkNCoQgEEZ1b2B36wrdSa/QVTpCPzfIC5TtJtm6sC3WQHy480AUDXx8w0CUdM4tAhg5zzO24DRN2IJaa1jBsiyFHMdxUUptWxgYY/xcVdVb0FrrNxGo69rPq+DDr4BhQSosSIUFqbAgFRakwoJFUezjCpzg63VuH1fSvDXBVTKQKvk/Jf5VvvgslDsVkuC3i8PlR2fxXgp5lzhOZuUoNQrkBM9Ixc+kkmeJz6QWcya5QLLgVSkq+ZT4ztRi8mySO2FBKixIhQWpwAtC/4b4+MqPihfc1pDIYRiwBfu+hxbE7+Ku67BLDN8kbdtiCzZNAywoxBPD6ahIydcAPAAAAABJRU5ErkJggg==) | Menambahkan fungsi transisi                                  |
| ![img](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACgAAAAzCAYAAADl70o1AAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAAFiUAABYlAUlSJPAAAAE1SURBVGhD7ZnrCYMwFEZNR3A3V3AnXcFFukR1A4X+9lGTGvhaqjGPwqfmQEgseRzvNQGtuD+eU0LMbalpoRcU08zSpkSM48gtOAwDt2Df99yCRVFQCmZZpmq6TVKWparzPFe1Euy6Tl0wUFWVqrVgPKh9iYK+REFfggimafqzhODcETRFKkQUnQX3Lm66CRPX2CRt2y6tN/L6+zdXggh+p9A3rcg1UvxPnAX3PmO+z+O5U2yKjk/kNHGT+LIpqM+zkOeaxGZOq7c6nND2+do79txvdXrXyrInTdgHx9rgHEFcEEWwYB9XzpViZC1SWLCPK1aCuCCKrIF9cKwNx04x3rUsGBFbcCzOaWJTECeVJRQ2cx47xQxEQV/oBWn/hvj4yq9apIj5LOIWbJqGW7Cua2LBJHkBgkjW+uUYZNwAAAAASUVORK5CYII=) | Menghapus state Menghapus fungsi transisi                    |
| ![img](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADMAAAA6CAYAAAAdrmHiAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAAFiUAABYlAUlSJPAAAAMlSURBVGhD7Zo/SytBFMVnN2oj+Kexs7HUJhBIbW8nCIEUER74DRTULmKTIr2KhY2NWAs2D2x8lZ2NkAh+gEQCadQkL+e6J143Udnd53N3mR8cdnYyu5mTe+/s4Oo0Go2eSQnOr/Lv9Jj5U2ulx0yvj9dOPKmKjOsdU4E1E1fStQB0u90hM0dHR14rnqytrcnx7OxMjgM6nU7Pr4ODgx52BnED84KIf55uX8YvTbPZjI0+A5+7x8fHhmq1WqKk4m5sbHhNY2ZnZ0VJxf0qfEnCPjTjijUDuFh8pJmZGdGoz6Cpqal359PT0yLdFxQbGdDfBok0z8/PIuA4jkiP4TVQJpPB7kMEXNcVRSH01fxyvXMYHx8XARrDGE6a1/A6GIJgjveIgk0zDdMJ0mkzNjYmAjoCBOMJIsV7RIlOZDM6PThp0N/NiqrVqllfXxdtb2+b6+tr0dPT07tr2aYh9gfBphngqsT0eHx8HPRdXV2ZYrEoWlhYMHt7e6LV1VVzenoq2tra8u70Cu+j7xmU16QOAfIcsEbK5bKZmJiQdr1eN+fn59KenJwcpMz8/LzJ5/PSPjk5Mfv7+9Le2dmRI8B9YSgMNs00LHr8+pVKRdRut9+tbEwbFjhUKpXM3d2dCCnK5w+iwnZQIpthnczNzZnl5WVRNpsdTPQjYKxQKIguLi683rf0DYNNMw1TYnNz01xeXopQ2LlcTqRhqlFLS0uih4eHQR9gtIPyz9KMT3wIk2Jt+CfFSbPOIIxhG/xYzcSJ0Gb0rhjCr/ry8iJCRIhOLcBI4vzm5ka0uLgYOhqa0Ffr7T7Rm0ttjIIBPeb29la0srIi5wBj9LIeBJtmmlGp5Y8AUwtj9Pjd3V0Rt0EA/Xr3HYTIZkZ9sTaGdGE9wJA2qeuEhv3tINg0+wquXEA/T/yrlS50HSXdDkJkM0gpnVZg1Lm/D4StjY/4lsj8FNZMXLFm4kpoM/rF6XcpKDYyccUd+i+HBCOvzqmkI6/OoxZeXHDu7+/fdoUe+AtLnGEWHR4eypE49Xp9yAxerIIwL0n/J8wizvNTM0nDqdVqQ2aSiTF/AS7ecbnKdgV6AAAAAElFTkSuQmCC) | Undo                                                         |
| ![img](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACsAAAA/CAYAAAB5GjFNAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAAFiUAABYlAUlSJPAAAAN8SURBVGhD7Vk9TyJRFH2DIo1RSAiJ0crWxNib+AtoCQkJITb0JFbwB3T9A+gPoKGx9R9sIS0FgUBBQQWI0fiFH+cuZ/ZlorzZjcR5Zk5ycy+zd2bOnHfenYnrvL5DWQLnd2diDdnILFuBkOyiYNcGOzs7CyzZTCYjOR6PS3aGw+FrIpGQH0HB+fm55GKxKPnl5UWyS3Y0GsmBIKBer0sm2el0KjmcBl8NzABESHZRCJX9apCscXS5A9lxJD8/P6vl5WWpMf84VqLRqFwQYC+AnkjkryYf9Xjv7R1dDw8Pkn+WDaCArgJVBaAqFEWghop822AFEFCVN4NC+vX0/nnwTZbgCbg4iJEoa5BaWlqSeHp6kodC3N/fuwRjsZjbj+vgHN0iJvwsGxDuCTM1qAhrKEfVdKtAfS43FKf6tIIf8N7GabC+vi6ZFydh1iAANBoNdXFxIfVgMFC7u7tSFwoFlUwmpUb/RxiPx7PqD7zT4Pb2VrJVNvA9Z7G8gG4BLG2pVHLrfD4v9cbGhigNVKtVVS6Xpd7f31eTyURq3JPX5DHCq+zNzY1kI9nV1VXJ8B6AcUQcHx+rra0tqbHculWIu7s7dXh4KPX29rY74E9PT8W7gMkGfBgrbEAYyeqzk/Pz+vpaotVqiaK6qgR+I7DU2CAIqEn/6RPDBJ5jJMub8k0FXF5eSmSzWXcsAax14nigvb09iYODA5VKpSTYp/d+Bt9kgwTjBltbW5Osz9aTkxOpc7mc2tzclJovBoI1+lnDRvgNrKysSAZMX138d9+e5ZJh+fiRghvzG0BfVgR7ANoDfSCJ4PkkPw/ss8oGRrLep4c6Ozs7Ehj8/B5AUEHUfHlAZdawAXtxncfHRwkTfCvrJQKk02mJZrMpvwF8/rFHtw19itB9CuAchAm+yQYJRrLcQFQK4CapVCrucSwnN6O+eTCbWSP0fh4zgX1GstzVvAks4Z787kMC5GkDPBztA3zkX68A8+CbbJDg2wYE1UBAcSpFpRFQVH89U5l59Tyw75+VBRnis4eAb3XwuF7jOvrxefhvst8JK8hapWxIdtEwfs9+B7zfs/1+X3Jog0UhVParYaUNAv0fzZwGvV5Psju6goxutytZyEoVYPAPd06n0wk8WcIKZQmn3W7bQ/bq6soesrVaLfTsIuAcHR3ZQ7b8K7hvMC8ssoFSby0n+6doTjFCAAAAAElFTkSuQmCC) | Redo                                                         |



**Referensi**

[1] Dirgantara, Harya Bima. 2016. *Teori Bahasa dan Automata: Merancang Automata Dengan JFLAP*. Yogyakarta: Penerbit Andi.
