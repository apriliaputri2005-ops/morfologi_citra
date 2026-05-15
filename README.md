# Praktikum Morfologi Citra Digital

## Identitas

- Nama: Aprilia Putri
- Mata Kuliah: Pengolahan Citra Digital
- Materi: Morfologi Citra

---

# Deskripsi Praktikum

Praktikum ini bertujuan untuk mempelajari operasi morfologi pada citra digital menggunakan bahasa pemrograman Python dan library OpenCV. Operasi morfologi digunakan untuk melakukan pengolahan bentuk objek pada citra biner sehingga objek dapat diperjelas, diperbesar, diperkecil, maupun dibersihkan dari noise.

Pada praktikum ini dilakukan beberapa tahapan pengolahan citra, yaitu:
- Konversi citra menjadi grayscale
- Thresholding (binerisasi)
- Dilasi
- Erosi
- Opening
- Closing

---

# Tools dan Library

Software dan library yang digunakan pada praktikum ini:
- Visual Studio Code
- Python 3.14
- OpenCV (cv2)
- NumPy
- Matplotlib

Install library menggunakan perintah berikut:

```bash
pip install opencv-python matplotlib numpy
```
**Dokumentasi Praktek**

![foto](https://github.com/apriliaputri2005-ops/morfologi_citra/blob/e6f5bbee37e9f348c8dc4aeeaa7b7a750069ffb7/Screenshot%20(580).png)

***Penjelasan Operasi Morfologi***

**1. Thresholding / Binerisasi**

Tahap awal dilakukan dengan mengubah citra grayscale menjadi citra biner (hitam putih). Tujuannya agar objek lebih mudah diproses pada operasi morfologi.

**2. Dilasi**

Dilasi digunakan untuk memperbesar objek putih pada citra. Operasi ini membantu menutup celah kecil dan memperjelas bentuk objek.

Hasil:

Objek terlihat lebih tebal
Noise kecil dapat tertutup

**3. Erosi**

Erosi digunakan untuk mengikis atau mengecilkan objek putih pada citra.

Hasil:

Objek menjadi lebih tipis
Noise kecil dapat dihilangkan

**4. Opening**

Opening merupakan kombinasi operasi:

Erosi
Dilasi

Opening digunakan untuk membersihkan noise kecil tanpa merusak bentuk utama objek.

**5. Closing**

Closing merupakan kombinasi operasi:

Dilasi
Erosi

Closing digunakan untuk menutup lubang kecil pada objek sehingga bentuk objek menjadi lebih utuh.

Hasil Praktikum

Program berhasil menampilkan beberapa hasil pengolahan citra, yaitu:

Citra asli
Citra biner
Hasil dilasi
Hasil erosi
Hasil opening
Hasil closing

Dari hasil tersebut dapat dilihat bahwa operasi morfologi mampu memperbaiki kualitas objek pada citra dan membantu proses segmentasi objek.

***Kesimpulan***

Berdasarkan praktikum yang telah dilakukan, dapat disimpulkan bahwa operasi morfologi citra sangat penting dalam pengolahan citra digital, terutama untuk proses segmentasi dan pengurangan noise. Operasi seperti dilasi, erosi, opening, dan closing dapat digunakan untuk memperjelas bentuk objek sehingga citra lebih mudah dianalisis.

Penggunaan Python dan OpenCV mempermudah proses implementasi morfologi citra karena memiliki fungsi yang lengkap dan mudah digunakan.


## Jawaban Pertanyaan yg di web ##

**1.jelaskan lebih lanjut tentang skimage measure untuk analisis sel**

skimage.measure adalah salah satu modul pada library scikit-image yang digunakan untuk melakukan pengukuran dan analisis objek pada citra digital. Dalam analisis sel, modul ini sangat berguna untuk mendeteksi, menghitung, dan mengambil informasi dari setiap sel yang terdapat pada gambar mikroskopis.

Biasanya skimage.measure digunakan setelah proses preprocessing seperti grayscale, thresholding, segmentasi, atau morfologi citra selesai dilakukan. Setelah objek sel berhasil dipisahkan dari background, modul ini dapat menghitung berbagai karakteristik dari sel tersebut.

**2 apa perbedaan top hat dan black hat transform pada deteksi cacat?**

Perbedaan utama antara Top Hat Transform dan Black Hat Transform terletak pada jenis objek atau cacat yang ingin ditonjolkan pada citra.

Dalam pengolahan citra digital, kedua metode ini termasuk operasi morfologi yang digunakan untuk mendeteksi detail kecil, noise, atau cacat pada permukaan objek.

**3 jelaskan perbedaan zhang-suen vs hilditch untuk thinning**

Zhang-Suen dan Hilditch adalah dua algoritma thinning (penipisan citra) yang digunakan dalam pengolahan citra digital untuk mengubah objek menjadi bentuk kerangka (skeleton) tanpa menghilangkan struktur utama objek.

Biasanya thinning digunakan pada:

OCR (pengenalan tulisan tangan)
sidik jari
analisis pola
analisis bentuk objek
citra medis

Tujuan utama thinning:

mengurangi ketebalan objek menjadi 1 piksel
mempertahankan bentuk dan konektivitas objek

**4.Bagaimana cara menggabungkan NDVI dengan morfologi untuk anailisis vegetasi**

NDVI (Normalized Difference Vegetation Index) dan operasi morfologi sering digabungkan dalam pengolahan citra satelit untuk meningkatkan kualitas analisis vegetasi. NDVI digunakan untuk mendeteksi area tumbuhan berdasarkan nilai pantulan cahaya, sedangkan morfologi digunakan untuk membersihkan noise, memperjelas bentuk area vegetasi, dan memperbaiki hasil segmentasi.

**5. bagaimana cara menggunakan watershed untuk memisahkan sel yg saling menyentuh**

Metode Watershed adalah teknik segmentasi citra yang digunakan untuk memisahkan objek yang saling menempel atau menyentuh, seperti sel pada citra mikroskopis. Metode ini sangat populer dalam analisis citra medis karena mampu memisahkan objek yang sulit dibedakan secara manual.

Konsep Watershed dianalogikan seperti permukaan topografi:

area terang dianggap sebagai gunung
area gelap dianggap sebagai lembah
proses segmentasi dilakukan seperti air yang mengalir dan membentuk batas antar objek

Dalam analisis sel, Watershed digunakan untuk:

memisahkan sel yang berhimpitan
menghitung jumlah sel
segmentasi objek biologis
analisis bakteri atau jaringan
