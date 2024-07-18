# Brazilian E-Commerce Public Dataset by Olist

![logo_blue_background_8b55024b33](https://github.com/user-attachments/assets/3d8953f1-f350-4514-9386-33514466aa39)

This Project was carried out by Alpha's Team:
1. Arkirndra Muhammad Nikola
2. Valeria Trisna Yunita
3. Erza Anandhika Valerian Vacquier

## Context
Perkembangan e-commerce di Brazil menunjukkan pertumbuhan yang sangat pesat dalam beberapa tahun terakhir. Pada tahun 2023, pasar ritel e-commerce di Brazil menghasilkan pendapatan lebih dari 36 miliar dolar AS, dan menurut estimasi dari Statista, pendapatan ini akan melampaui 60 miliar dolar AS pada tahun 2025. Hal ini mencerminkan pertumbuhan yang signifikan dalam industri ini, yang diperkirakan akan terus berlanjut.

Segmen e-commerce di Brazil menghasilkan total pendapatan nasional sebesar 170 miliar real Brazil pada tahun 2022, meningkat dua kali lipat dibandingkan tahun 2019 dan naik sebesar 12% dari tahun 2021. Pertumbuhan ini mencerminkan peningkatan adopsi teknologi digital oleh konsumen Brazil serta peningkatan kepercayaan terhadap transaksi online.

Olist adalah salah satu perusahaan marketplace terbesar di Brazil yang beroperasi di sektor e-commerce. Olist memfasilitasi koneksi antara penjual dan pelanggan melalui kontrak tunggal, memungkinkan penjual untuk menjual dan mengirim produk mereka melalui mitra logistik Olist. Setelah produk diterima atau estimasi pengiriman tersedia, pelanggan menerima survei kepuasan di mana mereka dapat memberikan ulasan dan rating.

Model bisnis unik Olist yang tidak hanya menghubungkan penjual dan pelanggan tetapi juga menyediakan solusi logistik yang efisien, menjadikannya pionir dalam inovasi e-commerce di Brazil. Penelitian terhadap Olist penting untuk mengungkap dinamika kluster pengguna di platform ini, memberikan wawasan berharga bagi pelaku bisnis e-commerce. Dengan menganalisis kluster pengguna, penelitian ini bertujuan untuk memahami karakteristik dan perilaku konsumen yang berbelanja melalui Olist, yang dapat digunakan untuk mengembangkan strategi pemasaran yang lebih efektif dan meningkatkan pengalaman pelanggan.


## Business Problem
Hasil analisis eksplorasi data awal kami mengungkapkan pola menarik di mana mayoritas pelanggan Olist hanya melakukan pembelian satu kali. Kejutan ini semakin mendalam saat kami meneliti metode pembayaran yang dipilih oleh pelanggan tersebut. Menariknya, hampir semua pembeli satu kali ini menggunakan kartu kredit untuk transaksi mereka. Meskipun kartu kredit menawarkan kemudahan dan opsi pembayaran angsuran, mayoritas pelanggan Olist tetap hanya melakukan satu transaksi.

Hasil analisis ini mengungkapkan adanya celah dalam strategi retensi pelanggan Olist dan menunjukkan kebutuhan akan strategi yang efektif untuk mengubah pembeli satu kali menjadi pelanggan setia.

Berangkat dari permasalah di atas maka proyek riset ini memiliki pertanyaan penelitian, yaitu:  


> *Bagaimanakah strategi pemasaran yang tepat dan efektif untuk meningkatkan revenue pada Olist?*

## Goal/Tujuan

Berdasarkan permasalahan yang telah diidentifikasi, perusahaan Olist ingin memperoleh jawaban yang jelas untuk beberapa pertanyaan strategis guna menemukan solusi dan rekomendasi yang tepat. Tujuan utama adalah memperbaiki dan mempertahankan kinerja perusahaan melalui segmentasi customer dan rekomendasi berbasis data historis. Dengan demikian, perusahaan dapat menyusun program bisnis yang tepat sasaran, meningkatkan retensi customer, dan menarik customer baru. Hasil temuan dan model yang dibuat akan dipresentasikan kepada stakeholder untuk mendukung pengambilan keputusan dan penyusunan strategi pemasaran yang lebih efisien.


## Analytic Approach

Dalam proyek ini, kami menerapkan Analisis RFM dan Klasterisasi K-Means untuk melakukan segmentasi pelanggan. Analisis RFM mengelompokkan kebiasaan pelanggan berdasarkan:

1. Recency: jumlah hari sejak transaksi terakhir pelanggan.
2. Frequency: seberapa sering pelanggan melakukan pembelian.
3. Monetary: total nilai transaksi pelanggan.

Untuk menentukan jumlah klaster dengan algoritma K-Means, kami menggunakan:
1. Silhouette Score: Silhouette Score menilai sejauh mana setiap data berada dalam klaster yang tepat dibandingkan dengan klaster lain di sekitarnya. Skor ini berkisar antara -1 hingga 1, dengan skor lebih tinggi menunjukkan penempatan yang lebih baik dalam klaster tersebut dan terpisah dari klaster lainnya. Skor mendekati 1 menunjukkan klaster yang tepat, sedangkan skor mendekati -1 menunjukkan bahwa data mungkin lebih baik ditempatkan di klaster lain. Nilai sekitar 0 menunjukkan adanya tumpang tindih antar klaster.

2. Metode Elbow: Metode ini menilai varian dalam klaster sebagai fungsi dari jumlah klaster. Tujuannya adalah untuk mengukur jumlah kuadrat jarak antara setiap titik data dengan pusat klasternya. Jumlah klaster optimal dipilih pada titik "elbow" di grafik, di mana penurunan varian mulai melambat.

3. Domain of Knowledge: untuk penyesuaian dan tujuan bisnis.

## Dataset Description
![HRhd2Y0](https://github.com/user-attachments/assets/efb0df9e-8d08-472e-9dc6-946087e92f60)


Dataset Olist ini memiliki 9 file yang terpisah, untuk menggabungkannya diperlukan primary key sesuai pada gambar diatas.

## Conclusion
### For Model
Setelah menjalani modelling diatas dan menganalisanya, dapat diambil kesimpulang bahwa:
- Dari 2 metode clustering k-means menggunakan PCA dan RFM,
- Cluster 0 (Bargain Spenders):

    - Rata-rata memiliki recency sekitar 241.54 hari, dengan frekuensi pembelian sekitar 1.18 kali, dan nilai pembelian rata-rata sebesar 102.58 unit mata uang.
    - Median recency adalah 222 hari, dengan median frequency pembelian sebesar 1 kali, dan median monetary sebesar 81.75 unit mata uang.
    - Mereka cenderung melakukan pembelian dengan nilai yang lebih rendah dibandingkan cluster lainnya, tetapi dengan frekuensi yang relatif stabil.
- Cluster 1 (Big Spenders):

    - Rata-rata memiliki recency sekitar 248.43 hari, dengan frekuensi pembelian sekitar 2.70 kali, dan nilai pembelian rata-rata sebesar 2391.31 unit mata uang.
    - Median recency adalah 221 hari, dengan median frequency pembelian sebesar 1 kali, dan median monetary sebesar 1999 unit mata uang.
    - Mereka adalah kelompok dengan nilai pembelian tertinggi dan frekuensi pembelian yang cukup tinggi juga.
- Cluster 2 (Value Spenders):

    - Rata-rata memiliki recency sekitar 243.79 hari, dengan frekuensi pembelian sekitar 1.87 kali, dan nilai pembelian rata-rata sebesar 624.39 unit mata uang.
    - Median recency adalah 223 hari, dengan median frequency pembelian sebesar 1 kali, dan median monetary sebesar 549 unit mata uang.
    - Meskipun tidak sebesar Cluster 1, mereka cenderung melakukan pembelian dengan nilai yang lebih tinggi daripada Cluster 0, namun dengan frekuensi yang tidak terlalu tinggi.

- Dari hasil clustering, akan digunakan hasil dari K-Means clustering RFM dibandingkan PCA dengan total cluster 3.
- Keempat sistem rekomendasi ini memiliki tujuan untuk meningkatkan kepuasan pelanggan, mendorong pembelian lebih lanjut, dan mengoptimalkan nilai sepanjang perjalanan pembelian pelanggan. Dengan menggunakan data mengenai pola pembelian dan preferensi pelanggan, bisnis dapat menghadirkan pengalaman yang lebih personal dan menguntungkan bagi setiap pelanggan mereka.

### For Business
Setelah menjalani analisis dan modelling, berikut merupakan konklusi untuk bisnis Olist:
1. Metode pembayaran yang paling umum digunakan di Brasil adalah kartu kredit. Hal ini berlaku merata di semua klaster pelanggan. Popularitas kartu kredit di Brasil disebabkan oleh fleksibilitas pembayaran cicilan tanpa bunga, program poin dan hadiah, serta promosi dan diskon eksklusif yang ditawarkan oleh berbagai merchant.

2.  Semua klaster pelanggan, baik Bargain Spenders, Value Spenders, maupun Big Spenders, menunjukkan bahwa pengiriman barang di 5 kota utama umumnya lebih cepat daripada estimasi yang diberikan. Pengiriman yang lebih cepat ini dapat meningkatkan kepercayaan pelanggan terhadap e-commerce tersebut. Namun, terdapat variasi dalam pengiriman di beberapa kota untuk klaster Big Spenders, seperti di Salvador yang membutuhkan waktu lebih lama.

3.  Lonjakan signifikan dalam jumlah pesanan dan pendapatan pada November 2017, yang bertepatan dengan Black Friday, menunjukkan bahwa promosi besar sangat efektif, terutama untuk klaster Big Spenders. Setelah periode Black Friday, pendapatan dan volume pesanan dari klaster ini tetap lebih tinggi dibandingkan klaster lainnya, menandakan bahwa mereka cenderung tetap aktif setelah tertarik dengan promosi besar.

4.  Klaster Big Spenders konsisten menghasilkan pendapatan tertinggi dengan tren peningkatan pesanan yang stabil. Bargain Spenders memiliki pendapatan dan volume pesanan yang stabil namun lebih rendah dibanding Big Spenders, sedangkan Value Spenders menunjukkan volume pesanan dan pendapatan terendah. Tren musiman menunjukkan peningkatan signifikan selama Q4, dipengaruhi oleh periode belanja liburan.

5. Untuk menjaga loyalitas klaster Big Spenders, penting untuk menjaga ritme pengiriman yang cepat dan menambah jasa kirim/kurir agar pesanan tidak overload pada beberapa mitra pengiriman. Standar pengiriman dalam negeri sebaiknya ditetapkan, misalnya dalam waktu 5 hari. Selain itu, program loyalitas atau penawaran khusus akan lebih efektif jika ditargetkan kepada klaster Big Spenders yang memberikan kontribusi terbesar terhadap pendapatan.

6. Berdasarkan analisis Customer Lifetime Value (CLV), kluster Big Spender memberikan keuntungan yang signifikan dibandingkan dengan kluster lainnya. Namun, penting untuk tidak mengabaikan kluster lainnya. Meskipun kluster Bargain Spender memberikan keuntungan per transaksi yang rendah, volume transaksi yang besar dari kluster ini tetap berkontribusi secara signifikan terhadap total revenue Olist. Oleh karena itu, diperlukan upaya maintenance yang berkelanjutan untuk menjaga dan meningkatkan loyalitas dari semua kluster pelanggan, termasuk Bargain Spender, guna memastikan pertumbuhan pendapatan yang berkelanjutan.

7. Penentuan strategi pemasaran berdasarkan kluster terbukti lebih efektif dibandingkan dengan pendekatan yang menyasar seluruh pelanggan secara umum. Segmentasi ini memungkinkan pemahaman yang lebih mendalam tentang perilaku pelanggan yang berbeda, sehingga memungkinkan penerapan strategi pemasaran yang lebih terarah dan memberikan keuntungan yang lebih tinggi.

## Rekomendation

### Recomendation for Model
Untuk meningkatkan performa model, berikut merupakan rekomendasi yang dapat dilakukan di penelitian selanjutnya:
- Menggunakan algoritma lain seperti DBScan, agglomerative clustering, dll untuk perbandingannya lebih lanjut.
- Feature Engineering Lebih Lanjut: dapat dilakukan penambahan fitur interaksi dan polinomial untuk menangkap hubungan non-linear antara variabel.
- Investigasi Pengaruh Faktor Eksternal: Melakukan studi tentang pengaruh faktor eksternal seperti kebijakan pemerintah, perubahan iklim, dan perkembangan infrastruktur terhadap harga rumah. Mengintegrasikan data eksternal ini dalam model untuk meningkatkan akurasi prediksi.

Dengan melaksanakan rekomendasi ini, penelitian selanjutnya dapat memperbaiki model prediksi harga rumah, menghasilkan estimasi yang lebih akurat, dan memberikan wawasan yang lebih mendalam bagi pengambilan keputusan bisnis.

### Recomendation for Business
Berikut merupakan rekomendasi untuk bisnis OLIST:
1. Mengingat efektivitas promosi besar seperti Black Friday dalam meningkatkan volume pesanan dan pendapatan terutama dari klaster Big Spenders, perusahaan e-commerce harus merencanakan dan melaksanakan promosi besar secara teratur. Selain itu, memperkuat program poin dan hadiah pada kartu kredit akan mendorong lebih banyak transaksi dari klaster ini, karena mereka cenderung memanfaatkan manfaat tersebut.

2. Untuk menjaga dan meningkatkan kepercayaan pelanggan, terutama dari klaster Big Spenders, penting untuk terus meningkatkan efisiensi pengiriman. Menambah mitra pengiriman/kurir dapat menghindari overload pada beberapa mitra yang ada dan memastikan pengiriman tetap cepat dan tepat waktu. Menetapkan standar waktu pengiriman yang konsisten, misalnya dalam 5 hari, juga akan membantu dalam menjaga kepuasan pelanggan.

3. Targetkan Penawaran Khusus kepada Klaster Big Spenders:
Mengingat klaster Big Spenders memberikan kontribusi terbesar terhadap pendapatan, perusahaan harus fokus pada strategi retensi yang diarahkan kepada mereka. Penawaran khusus, program loyalitas yang eksklusif, dan layanan pelanggan yang dipersonalisasi akan meningkatkan kepuasan dan loyalitas klaster ini. Selain itu, evaluasi rutin terhadap respon mereka terhadap berbagai promosi dapat membantu dalam merancang strategi pemasaran yang lebih efektif.


