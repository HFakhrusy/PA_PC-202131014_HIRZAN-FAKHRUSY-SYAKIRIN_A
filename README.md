# Remove Background


# Teori

## Definisi
Dalam pengolahan citra, penghapusan latar belakang (remove background) adalah proses menghilangkan atau memisahkan objek dari latar belakangnya. Teknik ini sering digunakan dalam berbagai aplikasi seperti pemrosesan gambar, pengenalan wajah, pengenalan objek, dan grafika komputer.
Ketika fitur remove background digunakan untuk menghilangkan latar belakang sebuah obyek gambar, ada kalanya gambar yang telah selesai di-remove background masih menyisakan tepian yang tidak rata.

Ada beberapa pendekatan yang dapat digunakan untuk menghapus latar belakang dalam pengolahan citra. Berikut ini beberapa metode yang umum digunakan:

1.	Metode berdasarkan warna (Color-based methods): Metode ini bergantung pada perbedaan warna antara objek dan latar belakangnya. Pada umumnya, warna latar belakang diidentifikasi dan dihilangkan dengan melakukan operasi pembandingan warna atau melalui segmentasi berdasarkan ruang warna seperti RGB, HSV, atau YUV.
2.	Metode berdasarkan deteksi tepi (Edge detection methods): Metode ini mencoba untuk mengidentifikasi tepi objek dan memisahkannya dari latar belakang. Algoritma deteksi tepi seperti Canny, Sobel, atau Laplacian dapat digunakan untuk menemukan tepi objek yang tajam.
3.	Metode berdasarkan pemisahan foreground-background (Foreground-background separation methods): Metode ini menggunakan teknik pemisahan objek dari latar belakang dengan memodelkan karakteristik intensitas piksel objek dan latar belakang. Metode seperti pengurangan latar belakang (background subtraction), pengolahan gauss (Gaussian processing), atau pengolahan keruh (Blurr processing) sering digunakan dalam hal ini.
4.	Metode berdasarkan pemodelan probabilistik (Probabilistic modeling methods): Metode ini melibatkan pemodelan probabilistik untuk mengklasifikasikan piksel sebagai objek atau latar belakang. Metode seperti Gaussian Mixture Model (GMM), Expectation-Maximization (EM), atau pengklasifikasi berbasis probabilitas (naive Bayes classifier) dapat digunakan untuk tujuan ini.
   
Selain itu, teknik penghapusan latar belakang juga dapat dikombinasikan dengan metode deteksi objek seperti deteksi wajah atau deteksi objek berbasis mesin learning (misalnya, dengan menggunakan jaringan saraf tiruan atau algoritma deep learning) untuk menghasilkan hasil yang lebih akurat.
Penting untuk dicatat bahwa penghapusan latar belakang dalam citra dapat menjadi tugas yang kompleks tergantung pada kompleksitas gambar dan kondisi pencahayaan. Metode yang lebih maju dan kompleks seperti pemrosesan semantik, segmentasi berbasis instan (instance-based segmentation), atau metode berbasis jaringan saraf dapat digunakan untuk hasil yang lebih baik.

Teori yang paling umum digunakan untuk menghapus latar belakang pada pengolahan citra adalah metode segmentasi berdasarkan perbedaan warna atau kecerahan. Ada beberapa pendekatan yang umum digunakan dalam teori ini, termasuk:

1.Thresholding: Metode ini melibatkan penentuan ambang batas di mana piksel dianggap sebagai latar belakang atau objek berdasarkan tingkat kecerahan atau   
  warnanya. Jika nilai piksel melebihi ambang batas, piksel dianggap sebagai bagian dari objek; jika tidak, piksel dianggap sebagai bagian latar belakang.
  

2.Metode pemodelan warna: Pendekatan ini melibatkan pemodelan distribusi warna di ruang warna untuk membedakan objek dan latar belakang. Metode ini mencakup 
  pemodelan histogram, seperti pemodelan Gauss, dan penggunaan pengklasifikasi, seperti K-means atau metode pemisahan Gaussian.

3.Penggunaan chroma keying: Metode ini melibatkan penggunaan latar belakang berwarna merata yang kontras dengan objek yang ingin dipertahankan. Dalam pengolahan 
  pasca-produksi, latar belakang berwarna tersebut dapat diganti dengan objek atau latar belakang yang diinginkan.

4.Metode pemisahan bayangan: Jika latar belakang dan objek menghasilkan bayangan yang berbeda, maka metode ini dapat digunakan untuk memisahkan objek dari latar 
  belakang dengan menghapus bayangan.

5.Metode pemisahan berdasarkan tepi: Jika objek dan latar belakang memiliki perbedaan yang jelas dalam kontur atau tepinya, metode pemisahan berdasarkan tepi 
  dapat digunakan. Metode ini mencakup operasi deteksi tepi, seperti operator Canny atau operator Sobel.

6.Metode pemisahan berdasarkan pemodelan ruang objek: Pendekatan ini melibatkan pemodelan objek 3D menggunakan teknik seperti stereo vision atau pemindaian 
  citra. Dalam metode ini, latar belakang dapat dihapus dengan membangun model 3D objek dan memisahkan objek dari latar belakang berdasarkan geometri atau 
   struktur objek tersebut.

Metode yang paling umum dan efektif untuk penghapusan latar belakang yang kompleks adalah dengan menggunakan teknik berbasis deep learning. Model deep learning, seperti jaringan saraf konvolusi (Convolutional Neural Networks/CNN), dapat dilatih untuk mengenali dan memisahkan objek dari latar belakang dengan tingkat akurasi yang tinggi.

Proses penghapusan latar belakang menggunakan model deep learning biasanya melibatkan langkah-langkah berikut:

Pengumpulan data pelatihan: Untuk melatih model deep learning, diperlukan dataset gambar yang berisi objek atau subjek yang ingin dihapuskan latar belakangnya, beserta latar belakang yang berbeda. Dataset ini harus diberi label dengan menandai area objek dan latar belakang.

Pelatihan model: Model deep learning, seperti CNN, dilatih menggunakan dataset yang dikumpulkan. Proses pelatihan melibatkan propagasi maju dan mundur (forward and backward propagation) untuk mengoptimalkan parameter model sehingga dapat mempelajari representasi fitur yang tepat untuk memisahkan objek dan latar belakang.

Pengujian dan validasi model: Setelah pelatihan selesai, model dievaluasi dengan menggunakan dataset pengujian dan validasi yang berbeda. Tujuannya adalah untuk memastikan model memiliki kinerja yang baik dalam mengenali dan memisahkan objek dari latar belakang dengan akurasi yang tinggi.

Penggunaan model pada gambar baru: Setelah model dilatih dan divalidasi, ia dapat digunakan untuk menghapus latar belakang pada gambar baru. Gambar tersebut diinputkan ke dalam model, dan model menghasilkan prediksi mengenai area objek dan latar belakang. Berdasarkan prediksi tersebut, latar belakang dapat dihapus atau dipisahkan dari objek.

Perlu dicatat bahwa penghapusan latar belakang dengan menggunakan model deep learning tidak selalu sempurna dan dapat tergantung pada keberagaman dan kompleksitas gambar yang dihadapi. Namun, teknik ini telah membawa kemajuan signifikan dalam pengolahan citra dan memungkinkan penghapusan latar belakang yang lebih presisi dan akurat.

Pendekatan di atas hanya merupakan beberapa contoh metode yang digunakan dalam teori penghapusan latar belakang pada pengolahan citra. Pemilihan metode yang tepat tergantung pada sifat citra, karakteristik objek dan latar belakang, serta kebutuhan aplikasi yang ingin dicapai.

 ## Tujuan dari Remove Background
 Fungsi utama dari RMBG adalah untuk mengekstrak objek atau subjek utama dari sebuah gambar dengan menghilangkan piksel latar belakang.

Penghapusan latar belakang memiliki beberapa tujuan, antara lain:

Mengisolasi subjek: Penghapusan latar belakang membantu mengisolasi subjek utama atau objek dalam sebuah gambar. Hal ini berguna ketika ingin menyoroti atau fokus pada subjek tersebut tanpa adanya distraksi dari latar belakang.

Peningkatan presentasi grafis: Dengan menghapus latar belakang, gambar dapat lebih mudah diintegrasikan ke dalam presentasi grafis seperti poster, pamflet, atau desain grafis lainnya. Ini memungkinkan subjek utama untuk lebih menonjol dan terlihat lebih profesional.

Pemrosesan lanjutan: Setelah latar belakang dihapus, gambar dapat diolah lebih lanjut untuk keperluan seperti penggabungan dengan latar belakang baru, pengeditan komposit, atau analisis lanjutan menggunakan teknik pengolahan citra.

RMBG sering digunakan dalam berbagai aplikasi seperti fotografi, desain grafis, e-commerce, dan pemrosesan citra komputer secara umum. Ada berbagai metode dan algoritma yang digunakan dalam RMBG, termasuk pendekatan berbasis pemrosesan citra konvensional dan teknik berbasis kecerdasan buatan seperti pengenalan pola atau jaringan saraf tiruan.

## Library REMBG

Library rembg pada Jupyter Notebook adalah sebuah library yang digunakan untuk menghapus latar belakang dari gambar menggunakan model deep learning. Library ini berfokus pada penghapusan latar belakang yang kompleks, seperti rambut atau objek dengan tepi yang rumit.

Instalasi: Pertama, pastikan Anda telah menginstal library rembg. Anda dapat melakukannya dengan menjalankan perintah berikut di Jupyter Notebook:

![image](https://github.com/HFakhrusy/PA_PC-202131014_HIRZAN-FAKHRUSY-SYAKIRIN_A/assets/115157262/0f21ee82-aa43-4217-a0d3-ed5443098223)

Impor library: Setelah menginstal, impor library rembg ke dalam Jupyter Notebook:

![image](https://github.com/HFakhrusy/PA_PC-202131014_HIRZAN-FAKHRUSY-SYAKIRIN_A/assets/115157262/bca87342-8043-4542-9832-ac768d914aa7)

Dengan menggunakan library rembg pada Jupyter Notebook, Anda dapat secara efisien menghapus latar belakang dari gambar dengan hasil yang berkualitas tinggi. Pastikan Anda memiliki model deep learning yang sesuai yang digunakan oleh library ini, seperti model u2net atau u2netp, yang dapat Anda unduh dan gunakan dengan library rembg.




# penjelasan baris program

![image](https://github.com/HFakhrusy/PA_PC-202131014_HIRZAN-FAKHRUSY-SYAKIRIN_A/assets/115157262/d8bc757b-b720-4e79-956e-dc536f761ec2)

![image](https://github.com/HFakhrusy/PA_PC-202131014_HIRZAN-FAKHRUSY-SYAKIRIN_A/assets/115157262/7bb89d04-5322-4745-8dcf-682378197ea2)
Baris ini mengimpor library matplotlib.pyplot dengan alias plt, yang akan digunakan untuk menampilkan gambar.

![image](https://github.com/HFakhrusy/PA_PC-202131014_HIRZAN-FAKHRUSY-SYAKIRIN_A/assets/115157262/62c01379-4b36-44f1-9f10-1842d2a38f58)
Baris ini mendefinisikan variabel input_path dan output_path yang berisi path (lokasi) file gambar masukan dan keluaran.

![image](https://github.com/HFakhrusy/PA_PC-202131014_HIRZAN-FAKHRUSY-SYAKIRIN_A/assets/115157262/8db53d0c-97fe-46ae-b43c-a18f0fd4eef4)
Baris ini membuka file gambar dengan menggunakan fungsi open dari library PIL (Pillow) dan menyimpannya ke dalam variabel input_image. Library PIL (Pillow) digunakan untuk memanipulasi gambar.

![image](https://github.com/HFakhrusy/PA_PC-202131014_HIRZAN-FAKHRUSY-SYAKIRIN_A/assets/115157262/ec0e1094-b46b-42d9-a323-3404a5bf6431)
Baris ini menggunakan fungsi subplot untuk membuat subplot dengan 1 baris dan 2 kolom, kemudian memilih subplot pertama. Fungsi imshow digunakan untuk menampilkan gambar input_image pada subplot yang dipilih. Baris terakhir menggunakan fungsi title untuk memberikan judul pada subplot.

![image](https://github.com/HFakhrusy/PA_PC-202131014_HIRZAN-FAKHRUSY-SYAKIRIN_A/assets/115157262/921d3381-1c97-4ddd-a165-f5f05a515888)
Baris ini menggunakan fungsi subplot untuk memilih subplot kedua, kemudian menggunakan imshow untuk menampilkan gambar output_image pada subplot tersebut. Fungsi title digunakan untuk memberikan judul pada subplot.

![image](https://github.com/HFakhrusy/PA_PC-202131014_HIRZAN-FAKHRUSY-SYAKIRIN_A/assets/115157262/aeab20f4-a3d3-433b-af63-e8b5d1a0deb4)
Baris ini menggunakan metode save pada objek output_image untuk menyimpan gambar dengan latar belakang yang dihapus ke dalam file yang ditentukan oleh output_path.

![image](https://github.com/HFakhrusy/PA_PC-202131014_HIRZAN-FAKHRUSY-SYAKIRIN_A/assets/115157262/92a72839-17a1-440a-bf36-50b516814968)
Baris ini menggunakan fungsi tight_layout untuk mengatur tata letak subplot secara otomatis agar sesuai, kemudian menggunakan show untuk menampilkan gambar dengan subplot pada jendela grafik matplotlib.

# SUMBER TEORI
Liu, X., Zhang, S., Liu, W., & Yang, J. (2020). Image background removal based on deep learning. Multimedia Tools and Applications, 79(1-2), 201-225. DOI:
