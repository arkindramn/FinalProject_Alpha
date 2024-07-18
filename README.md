# Final-Project_Alpha

## Context
Perkembangan e-commerce di Brazil menunjukkan pertumbuhan yang sangat pesat dalam beberapa tahun terakhir. Pada tahun 2023, pasar ritel e-commerce di Brazil menghasilkan pendapatan lebih dari 36 miliar dolar AS. Menurut estimasi dari Statista, pendapatan e-commerce di Brazil akan melampaui 60 miliar dolar AS pada tahun 2025 ([Statista, 2024](https://www.statista.com/forecasts/289746/e-commerce-revenue-forecast-in-brazil)). Hal ini menunjukkan adanya pertumbuhan yang signifikan dalam industri ini, yang diharapkan terus berlanjut di masa mendatang.

Brazil telah menjadi pangsa pasar yang matang dalam sektor e-commerce. Berdasarkan data  ([Statista (2024)](https://www.statista.com/topics/4697/e-commerce-in-brazil/)), pendapatan e-commerce di Brazil diperkirakan mencapai 49,173 miliar dolar pada tahun 2022, dengan volume pasar yang bisa mencapai 86,532 miliar dolar pada tahun 2025. Pada tahun 2021, pasar ini telah menghasilkan lebih dari 41,130 miliar dolar. Brazil juga merupakan negara dengan jumlah pengguna internet terbesar di Amerika Latin, dengan total 165 juta pengguna pada Januari 2022.

Segmen e-commerce di Brazil telah menghasilkan total pendapatan nasional sebesar 170 miliar real Brazil pada tahun 2022. Angka ini meningkat dua kali lipat dibandingkan dengan tahun 2019 dan mengalami kenaikan sebesar 12% dari tahun 2021. Pertumbuhan ini mencerminkan peningkatan adopsi teknologi digital oleh konsumen Brazil serta peningkatan kepercayaan terhadap transaksi online.
Potensi besar e-commerce di Brazil menjadikan Olist sebagai subjek penelitian yang sangat relevan. Olist adalah salah satu perusahaan marketplace terbesar di Brazil yang beroperasi di sektor e-commerce. Olist memfasilitasi koneksi antara penjual dan pelanggan dengan mudah melalui kontrak tunggal. Ini memungkinkan penjual untuk menjual dan mengirim produk mereka melalui mitra logistik Olist. Ketika pelanggan membeli produk dari toko Olist, penjual menerima notifikasi untuk memenuhi pesanan tersebut. Setelah produk diterima atau estimasi pengiriman tersedia, pelanggan menerima survei kepuasan di mana mereka dapat memberikan ulasan dan rating.

Olist, dengan model bisnisnya yang unik, tidak hanya menghubungkan penjual dan pelanggan tetapi juga menyediakan solusi logistik yang efisien, menjadikannya pionir dalam inovasi e-commerce di Brazil. Penelitian terhadap Olist penting dilakukan untuk mengungkap dinamika kluster pengguna di platform ini. Mengetahui bagaimana Olist berhasil menarik dan mempertahankan berbagai segmen pengguna dapat memberikan wawasan berharga bagi pelaku bisnis e-commerce. Dengan menganalisis kluster pengguna, penelitian ini bertujuan untuk memahami karakteristik dan perilaku konsumen yang berbelanja melalui Olist, yang dapat digunakan untuk mengembangkan strategi pemasaran yang lebih efektif dan meningkatkan pengalaman pelanggan.


## Business Problem
Hasil analisis eksplorasi data awal kami mengungkapkan pola menarik di mana mayoritas pelanggan Olist hanya melakukan pembelian satu kali. Kejutan ini semakin mendalam saat kami meneliti metode pembayaran yang dipilih oleh pelanggan tersebut. Menariknya, hampir semua pembeli satu kali ini menggunakan kartu kredit untuk transaksi mereka. Meskipun kartu kredit menawarkan kemudahan dan opsi pembayaran angsuran, mayoritas pelanggan Olist tetap hanya melakukan satu transaksi.

Hasil analisis ini mengungkapkan adanya celah dalam strategi retensi pelanggan Olist dan menunjukkan kebutuhan akan strategi yang efektif untuk mengubah pembeli satu kali menjadi pelanggan setia.

Berangkat dari permasalah di atas maka proyek riset ini memiliki pertanyaan penelitian, yaitu:  


> *Bagaimanakah strategi pemasaran yang tepat dan efektif untuk meningkatkan revenue pada Olist?*



## Langkah-langkah Pengerjaan
1. **Perumusan Masalah**: Menentukan masalah bisnis yang ingin dipecahkan dan tujuan dari model yang dibangun.
2. **Data Understanding**: Memahami data yang digunakan, termasuk makna setiap kolom dan baris.
3. **Data Cleaning**: Melakukan pembersihan data untuk memastikan data siap digunakan.
4. **Feature Engineering**: Membuat fitur-fitur baru yang relevan dengan permasalahan bisnis.
5. **Pemodelan**: Membangun model machine learning menggunakan pipeline yang terdiri dari preprocessing dengan `ColumnTransformer`, scaling dengan `RobustScaler`, dan pemodelan.
6. **Evaluasi**: Mengevaluasi model menggunakan metrik yang sesuai dan menjelaskan hasilnya.
7. **Kesimpulan dan Rekomendasi**: Memberikan kesimpulan akhir dan rekomendasi berdasarkan hasil proyek.

## Penggunaan Notebook
1. **Persiapan Data**: Import data dan library yang diperlukan.
2. **Preprocessing**: Menggunakan ColumnTransformer, BinaryEncoder dan OrdinalEncoder  untuk mengolah data.
3. **Pemodelan dan Training**: Membuat pipeline lalu melatih model dengan data yang telah diproses.
4. **Evaluasi Model**: Menggunakan metrik evaluasi untuk menilai kinerja model.
