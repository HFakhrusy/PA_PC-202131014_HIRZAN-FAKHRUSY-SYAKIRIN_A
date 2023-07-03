## Remove Background


## Teori
Dalam pengolahan citra, penghapusan latar belakang (remove background) adalah proses menghilangkan atau memisahkan objek dari latar belakangnya. Teknik ini sering digunakan dalam berbagai aplikasi seperti pemrosesan gambar, pengenalan wajah, pengenalan objek, dan grafika komputer.

Ada beberapa pendekatan yang dapat digunakan untuk menghapus latar belakang dalam pengolahan citra. Berikut ini beberapa metode yang umum digunakan:

1.	Metode berdasarkan warna (Color-based methods): Metode ini bergantung pada perbedaan warna antara objek dan latar belakangnya. Pada umumnya, warna latar belakang diidentifikasi dan dihilangkan dengan melakukan operasi pembandingan warna atau melalui segmentasi berdasarkan ruang warna seperti RGB, HSV, atau YUV.

2.	Metode berdasarkan deteksi tepi (Edge detection methods): Metode ini mencoba untuk mengidentifikasi tepi objek dan memisahkannya dari latar belakang. Algoritma deteksi tepi seperti Canny, Sobel, atau Laplacian dapat digunakan untuk menemukan tepi objek yang tajam.

3.	Metode berdasarkan pemisahan foreground-background (Foreground-background separation methods): Metode ini menggunakan teknik pemisahan objek dari latar belakang dengan memodelkan karakteristik intensitas piksel objek dan latar belakang. Metode seperti pengurangan latar belakang (background subtraction), pengolahan gauss (Gaussian processing), atau pengolahan keruh (Blurr processing) sering digunakan dalam hal ini.

4.	Metode berdasarkan pemodelan probabilistik (Probabilistic modeling methods): Metode ini melibatkan pemodelan probabilistik untuk mengklasifikasikan piksel sebagai objek atau latar belakang. Metode seperti Gaussian Mixture Model (GMM), Expectation-Maximization (EM), atau pengklasifikasi berbasis probabilitas (naive Bayes classifier) dapat digunakan untuk tujuan ini.

Selain itu, teknik penghapusan latar belakang juga dapat dikombinasikan dengan metode deteksi objek seperti deteksi wajah atau deteksi objek berbasis mesin learning (misalnya, dengan menggunakan jaringan saraf tiruan atau algoritma deep learning) untuk menghasilkan hasil yang lebih akurat.

Penting untuk dicatat bahwa penghapusan latar belakang dalam citra dapat menjadi tugas yang kompleks tergantung pada kompleksitas gambar dan kondisi pencahayaan. Metode yang lebih maju dan kompleks seperti pemrosesan semantik, segmentasi berbasis instan (instance-based segmentation), atau metode berbasis jaringan saraf dapat digunakan untuk hasil yang lebih baik.

## Baris program

from rembg import remove
from PIL import Image

import matplotlib.pyplot as a

input_path = 'teko.jpg'
output_path = 'newteko.png'

#  gambar asli
input_image = Image.open(input_path)


a.subplot(1, 2, 1)
a.imshow(input_image)
a.title('Original')

# Penghapusan latar belakang
output_image = remove(input_image)

# Tampilkan gambar setelah penghapusan latar belakang
a.subplot(1, 2, 2)
a.imshow(output_image)
a.title(' Removed Background')

# Save gambar yang telah dihapus latar belakang
output_image.save(output_path)

a.tight_layout()
a.show()



## penjelasan baris program
1.	from rembg import remove: Mengimpor fungsi remove dari library rembg. Fungsi ini digunakan untuk menghapus latar belakang gambar.

2.	from PIL import Image: Mengimpor class Image dari library PIL. Class ini digunakan untuk membaca dan menyimpan gambar.

3.	input_path = 'teko.jpg': Menyimpan path (lokasi) file gambar yang akan diolah. Dalam contoh ini, file gambar bernama "teko.jpg" berada dalam direktori yang sama dengan script program.

4.	output_path = 'newteko.png': Menyimpan path (lokasi) file hasil setelah penghapusan latar belakang. Dalam contoh ini, file hasil akan disimpan dengan nama "newteko.png" dalam direktori yang sama dengan script program.

5.	input_image = Image.open(input_path): Membuka gambar menggunakan fungsi open dari class Image dengan memasukkan path gambar sebagai argumen. Gambar tersebut disimpan dalam variabel input_image.

6.	a.subplot(1, 2, 1): Membuat subplot dengan ukuran 1 baris dan 2 kolom, dan memilih subplot pertama sebagai posisi saat ini untuk menampilkan gambar.

7.	a.imshow(input_image): Menampilkan gambar asli menggunakan fungsi imshow dari library matplotlib.pyplot dengan memasukkan gambar asli sebagai argumen.

8.	a.title('Original'): Memberikan judul "Original" pada subplot pertama.

9.	output_image = remove(input_image): Menghapus latar belakang gambar menggunakan fungsi remove dari library rembg. Gambar hasil penghapusan disimpan dalam variabel output_image.

10.	a.subplot(1, 2, 2): Memilih subplot kedua sebagai posisi saat ini untuk menampilkan gambar hasil penghapusan latar belakang.

11.	a.imshow(output_image): Menampilkan gambar hasil penghapusan latar belakang menggunakan fungsi imshow dengan memasukkan gambar hasil sebagai argumen.

12.	a.title('Removed Background'): Memberikan judul "Removed Background" pada subplot kedua.

13.	output_image.save(output_path): Menyimpan gambar hasil penghapusan latar belakang ke path yang telah ditentukan menggunakan fungsi save dari class Image. Gambar tersebut akan disimpan dalam format PNG sesuai dengan ekstensi file "newteko.png".

14.	a.tight_layout(): Mengatur tata letak subplot agar tampilan lebih rapi.

15.	a.show(): Menampilkan subplot secara keseluruhan.








