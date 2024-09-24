<h3><p align="center">Laporan Tugas Pemrosesan Citra Digital</p></h3>
<h3><p align="center">Tugas 3</p></h3>
<h3><p align="center">Halftoning, Patterning, dan Dithering</p></h3>
<p align="center"><img src="https://ulm.ac.id/id/wp-content/uploads/2023/03/lambangULM2021warna.png" alt="Logo ULM" width="400"/></p>

<p align="center"> oleh :</p>
<p align="center"> Sazidan Abrar Surya</p>
<p align="center"> 2310131110002 </p>
<p align="center"> Pemrosesan Citra Digital (ABKC6306)</p>
<br>
<p align="center"> Dosen Pengampu: </p>
<p align="center"> Dr. Harja Santana Purba, M.Kom </p>
<p align="center"> Novan A. B. Saputra, S.Kom., M.T </p>
<br>
<h3><p align="center"> PROGRAM STUDI PENDIDIKAN KOMPUTER</p></h3>
<h3><p align="center"> FAKULTAS KEGURUAN DAN ILMU PENDIDIKAN</p></h3>
<h3><p align="center">UNIVERSITAS LAMBUNG MANGKURAT</p></h3>
<h3><p align="center">2024</p></h3>
<br>
<p align="center"> i </p>
<br><br><br><br><br><br>
<p align="center"> Daftar isi: </p>
Penjelasan Halftoning....................................................................................................................................................................................1

Klasifikasi Metode Halftoning.....................................................................................................................................................................2  

Contoh Digital Halftoning............................................................................................................................................................................3  
  
Tiga Metode Umum Halftoning.................................................................................................................................................................4    
1. Patterning.................................................................................................................................................................................................5  
2. Dithering...................................................................................................................................................................................................6
3. Error diffusion.........................................................................................................................................................................................7  
  
Daftar Pustaka...................................................................................................................................................................................................8
<br><br><br><br><br><br><br><br><br><br>

### Apa itu Halftoning?

Halftone adalah teknik reprografi yang mensimulasikan citra tone berkelanjutan melalui penggunaan titik, bervariasi baik dalam ukuran, dalam bentuk atau dalam jarak. "Halfton" juga dapat digunakan untuk merujuk secara khusus untuk gambar yang dihasilkan oleh proses ini.

Dimana citra tone berkelanjutan berisi berbagai warna tak tebatas atau abu-abu, proses halfton mengurangi reproduksi visual untuk gambar biner yang dicetak dengan hanya satu warna tinta. Reproduksi biner ini bergantung pada ilusi optis dasar - bahwa titik-titik halfton kecil dicampur ke dalam nada halus dengan mata manusia. Pada tingkat mikroskopis, dikembangkan film fotografi hitam-putih yang juga terdiri dari hanya dua warna, dan bukan jangkauan ton yang berlanjut tak terbatas.

Sama seperti fotografi berwarna berkembang dengan penambahan filter dan lapisan film, pencetakan warna ini dimungkinkan dengan mengulangi proses halfton untuk setiap warna subtraktif yang paling umum menggunakan apa yang disebut "model warna CMYK". Properti semi-opak tinta memungkinkan halfton titik-titik warna yang berbeda untuk menciptakan efek-citra lain yang penuh warna optik.  

Metode Halftoning dapat diklasifikasikan menjadi 3 metode yaitu: 
1. Amplitude Modulation (AM) Halftoning
* Prinsip: Mengubah amplitudo (besarnya) titik-titik untuk mewakili tingkat keabuan.
* Metode:
    * Ordered dithering: Menggunakan pola matriks yang teratur untuk mengatur ukuran titik-titik.
    * Error diffusion: Mendistribusikan kesalahan dari satu titik ke titik-titik di sekitarnya.

2. Frequency Modulation (FM) Halftoning
* Prinsip: Mengubah frekuensi titik-titik untuk mewakili tingkat keabuan.
* Metode:
    * Random dithering: Menggunakan pola acak untuk mengatur jarak antara titik-titik.
    * Blue noise dithering: Menggunakan pola noise dengan spektrum frekuensi yang miring untuk mengurangi artefak.

3. Hybrid Halftoning
* Prinsip: Menggabungkan teknik AM dan FM untuk mencapai kualitas yang lebih baik.
* Metode:
    * Hybrid ordered dithering: Menggunakan pola matriks yang teratur untuk mengatur ukuran titik-titik dan pola acak untuk mengatur jarak.
    * Hybrid error diffusion: Menggunakan error diffusion dengan elemen acak.
  

Contoh digital Halftoning  

Visualisasi:  

![Contoh digital halftoning](https://people.ece.ubc.ca/irenek/techpaps/introip/Img00022.gif)  

Titik kecil yang terletak di tengah disimulasikan dalam halftoning digital dengan mengisi sel halftone tengah;   
Demikian pula, titik berukuran sedang yang terletak di sudut kiri atas disimulasikan dengan mengisi empat sel di sudut kiri atas. Titik besar yang menutupi sebagian besar area pada gambar ketiga disimulasikan dengan mengisi semua sel halftone.

Tiga metode umum untuk menghasilkan gambar halftoning digital adalah:
1. Patterning
2. Dithering
3. Error diffusion.

### 1. Patterning
Patterning adalah teknik paling sederhana dari ketiga teknik untuk menghasilkan gambar halftoning digital. Teknik ini menghasilkan gambar dengan resolusi spasial yang lebih tinggi dibandingkan gambar sumber. Jumlah sel halftone pada gambar keluaran sama dengan jumlah piksel pada gambar sumber. Namun, setiap sel halftone dibagi menjadi grid 4x4. Setiap nilai piksel input diwakili oleh jumlah kotak terisi yang berbeda dalam sel halftone. Karena grid 4x4 hanya dapat mewakili 17 tingkat intensitas yang berbeda, gambar sumber harus diquantisasi. Gambar 4.2 menunjukkan matriks pola rekursif Rylander, yang akan digunakan dalam daftar 4.1, dan contoh operasi patterning.

![](https://people.ece.ubc.ca/irenek/techpaps/introip/Img00023.gif)
Gambar 4.2 Matriks pola rekursif Rylander
![](https://people.ece.ubc.ca/irenek/techpaps/introip/Img00024.gif)
Gambar 4.3 Operasi Patterning

pola menghasilkan gambar halftoning digital dari gambar input menggunakan teknik pola. Pola program membaca gambar input, mengkuantisasi nilai piksel, dan memetakan setiap piksel ke pola yang sesuai. Gambar yang dihasilkan 16 kali lebih besar dari aslinya. 

Gambar yang dihasilkan ditulis ke file output sebagai file TIFF. Sebuah kata peringatan: "pola" memerlukan sejumlah besar perhitungan, gambar berukuran kurang dari 100x100 direkomendasikan.

![gambar ori](https://people.ece.ubc.ca/irenek/techpaps/introip/Img00025.gif) Gambar ori

![](https://people.ece.ubc.ca/irenek/techpaps/introip/Img00026.gif) Contoh Halftoning menggunakan Patterning

Contoh algoritma Patterning untuk matriks 2x2:
```
1. Atur semua piksel gambar dengan ukuran 0 (menunjukkan warna hitam).
2. Mulai loop berdasarkan ukuran baris dan kolom (I, j).
3. Jika image(i, j) > 50 // 50 adalah rentang ambang   
Newimage(i2, j2+1) = 1; End
4. if image(i, j) > 101 // 101 adalah rentang ambang   
Newimage(i2+1, j2) = 1; Endif
5. Jika image(i, j) > 152 // 152 adalah rentang ambang   
Newimage(i2+1, j2+1) = 1; Endif
6. Jika image(i, j) > 203 // 203 adalah rentang ambang   
Newimage(i2, j2) = 1; Endif
7. Ulangi hingga semua piksel dalam gambar dibaca.  
```
  
### 2. Dithering
Teknik lain yang digunakan untuk menghasilkan gambar halftoning digital adalah dithering.   
Tidak seperti patterning, dithering menghasilkan gambar keluaran dengan jumlah titik yang sama dengan jumlah piksel pada gambar sumber.   
Dithering dapat dianggap sebagai thresholding gambar sumber dengan matriks dither. Matriks diletakkan berulang kali di atas gambar sumber.   
Dimana jika nilai piksel gambar lebih besar daripada nilai dalam matriks, titik pada gambar output akan jadi putih.   
![matriks dither](matriks%20dither.png)matriks dither

![](https://people.ece.ubc.ca/irenek/techpaps/introip/Img00030.gif) contoh output dithering

Algoritma Dithering  
```
for all x & y do  
 if f(x,y) > m(x,y) then
 g(x,y) = white
 else
 g(x,y) = black
 end if
End for
```
### 3. Error Diffusion
Error Diffusion adalah teknik lain yang digunakan untuk menghasilkan gambar halftone digital. Teknik ini sering disebut dithering spasial. Error Diffusion secara berurutan melintasi setiap piksel dari gambar sumber.   
Setiap piksel dibandingkan dengan ambang batas. Jika nilai piksel lebih tinggi dari ambang batas, nilai 255 dikeluarkan; jika tidak, nilai 0 dikeluarkan.   
Kesalahan—perbedaan antara nilai piksel input dan nilai output—disebarkan ke tetangga yang dekat.   
Error Diffusion adalah operasi lingkungan karena tidak hanya beroperasi pada piksel input, tetapi juga pada tetangganya. Secara umum, operasi lingkungan menghasilkan hasil yang lebih berkualitas dibandingkan dengan operasi titik. Error Diffusion, jika dibandingkan dengan dithering, tidak menghasilkan artefak yang diperkenalkan oleh matriks ambang tetap. Namun, karena difusi kesalahan memerlukan operasi lingkungan, teknik ini sangat memakan komputasi.

Langkah-Langkah  
1. Konversi ke Skala Abu-abu:Jika gambar asli berwarna, langkah pertama adalah mengkonversi gambar menjadi skala abu-abu. Setiap piksel akan memiliki nilai antara 0 (putih murni) hingga 255 (hitam murni).
2. Inisialisasi Matriks Error: Buat sebuah matriks error yang akan digunakan untuk menyimpan error pada setiap iterasi. Matriks ini biasanya berukuran sama dengan gambar asli.
3. Proses Iteratif:
* Pilih Piksel: Mulai dari piksel kiri atas, proses setiap piksel secara berurutan.
* Kuantisasi: Bandingkan nilai grayscale piksel dengan nilai ambang batas (misalnya, 127). Jika nilai piksel lebih besar dari ambang batas, maka piksel tersebut diubah menjadi hitam (1), jika tidak, menjadi putih (0).
* Hitung Error: Hitung selisih antara nilai grayscale asli dan nilai biner yang dihasilkan. Selisih ini adalah error.
* Distribusikan Error: Gunakan matriks error diffusion untuk mendistribusikan error ke piksel-piksel tetangga yang belum diproses. Kalikan nilai error dengan bobot yang sesuai pada matriks error diffusion, lalu tambahkan hasil perkalian tersebut ke nilai grayscale piksel tetangga.
* Ulangi: Lanjutkan ke piksel berikutnya dan ulangi langkah-langkah di atas hingga semua piksel telah diproses.    

Contoh dengan Matriks Floyd-Steinberg:

Misalkan kita memiliki piksel dengan nilai grayscale 150. Ambang batasnya adalah 127.

* Kuantisasi: Karena 150 > 127, maka piksel diubah menjadi hitam (1).
* Hitung Error: Error = 150 - 127 = 23.
* Distribusikan Error:
    * Piksel di sebelah kanan: 23 * 7/16 = 10.125 (dibulatkan menjadi 10).
    * Piksel di bawah-kiri: 23 * 3/16 = 4.3125 (dibulatkan menjadi 4).
    * Piksel di bawah: 23 * 5/16 = 7.1875 (dibulatkan menjadi 7).
    * Piksel di bawah-kanan: 23 * 1/16 = 1.4375 (dibulatkan menjadi 1).

* Nilai-nilai error yang telah dibulatkan ini kemudian ditambahkan ke nilai grayscale piksel tetangga sebelum diproses pada iterasi berikutnya.

Contoh Sederhana:

gambar grayscale 3x3 dengan nilai piksel sebagai berikut:
```
100 150 200
120 170 220
140 190 240
```
Ambang batasnya adalah 127. Kita akan menggunakan matriks error diffusion Floyd-Steinberg.

Proses:

1. Piksel Pertama (100):


* Karena 100 < 127, piksel diubah menjadi putih (0).
* Error = 100 - 0 = 100.  
Distribusikan error:
    * Piksel kanan (150): 100 * 7/16 = 43.75 (dibulatkan menjadi 44). Nilai baru piksel kanan menjadi 150 + 44 = 194.
    * Piksel bawah (120): 100 * 3/16 = 18.75 (dibulatkan menjadi 19). Nilai baru piksel bawah menjadi 120 + 19 = 139.

Gambar menjadi:
```
0 194 200
139 170 220
140 190 240
```
2. Piksel Kedua (194):

* Karena 194 > 127, piksel diubah menjadi hitam (1).
* Error = 194 - 255 = -61.

* Distribusikan error:
    * Piksel kanan (200): -61 * 7/16 = -26.81 (dibulatkan menjadi -27). Nilai baru piksel kanan menjadi 200 - 27 = 173.
    * Piksel bawah (170): -61 * 3/16 = -11.44 (dibulatkan menjadi -11). Nilai baru piksel bawah menjadi 170 - 11 = 159.

... (lanjutkan untuk piksel lainnya)  

Output:

Setelah memproses semua piksel, kita akan mendapatkan gambar biner 3x3. Misalnya, outputnya bisa seperti ini:
```
0 1 1
1 1 1
1 1 1
```  

![](https://encrypted-tbn3.gstatic.com/images?q=tbn:ANd9GcTPzDd1E4IJyij8oZhsHq1AxxxxVDIfChsfAs4NH-HTQtoYDsNTmYYMxe92BdeH)  
Contoh Output  

  
Pseudocode:  
```
for setiap baris dalam gambar:
    for setiap kolom dalam baris:
        nilai_asli = nilai_grayscale_piksel
        nilai_biner = 1 jika nilai_asli >= ambang_batas, 0 jika tidak
        error = nilai_asli - nilai_biner * 255
        // Distribusikan error menggunakan matriks Floyd-Steinberg
        piksel_kanan.nilai_grayscale += error * 7/16
        piksel_bawah_kiri.nilai_grayscale += error * 3/16
        piksel_bawah.nilai_grayscale += error * 5/16
        piksel_bawah_kanan.nilai_grayscale += error * 1/16
 ```
Visualisasi:  

![Proses error diffusion](https://www.researchgate.net/profile/panagiotis-metaxas/publication/237675301/figure/fig1/as:645699800670215@1530958237531/error-diffusion-process.png)    

<br><br><br><br><br><br><br>  
Daftar Pustaka  
* https://engineering.purdue.edu/~bouman/ece637/notes/pdf/Halftoning.pdf
* https://cv.ulichney.com/papers/2000-halftoning-review.pdf
* https://people.ece.ubc.ca/irenek/techpaps/introip/manual04.html
* https://medium.com/analytics-vidhya/how-to-create-a-readme-md-file-8fb2e8ce24e3
* https://journal.uii.ac.id/jurnal-teknoin/article/download/687/609/678?__cf_chl_tk=1MVbqAm1WkIFPXQ4oW2H6BJVYewrodM0I9WbHs7zY.o-1727200894-0.0.1.1-8362
* https://id.wikipedia.org/wiki/Halfton




























