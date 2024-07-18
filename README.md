# Final-Project_Alpha

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


Setiap fitur atau kolom dari dataset dijelaskan di bawah ini:

* fitur pada tabel `customers`:

Fitur | Deskripsi
----------|---------------
**customer_id** | kunci untuk order dataset. Setiap order memiliki id yang unik.
**customer_unique_id**    | identifikasi  unik setiap customer.
**customer_zip_code_prefix** | 5 digit pertama kode pos customer.
**customer_city** | nama kota customer.
**customer_state** |  provinsi customer.

* fitur pada tabel `sellers` :

Fitur | Deskripsi
----------|---------------
**seller_id** |   identifikasi unik setiap penjual.
**seller_zip_code_prefix** | 5 digit pertama kode pos penjual.
**seller_city** | nama kota penjual.
**seller_state** | provinsi penjual.


* fitur pada tabel `order_items`:

Fitur | Deskripsi
----------|---------------
**order_id** | identifikasi unik setiap order.
**order_item_id** | nomor urut untuk mengidentifikasi jumlah item yang termasuk dalam pesanan yang sama.
**product_id** |identifikasi unik setiap produk.
**seller_id** | identifikasi unik setiap penjual.
**shipping_limit_date** | menunjukkan tanggal batas pengiriman penjual untuk menangani pesanan ke mitra logistik.
**price** | harga item.
**freight_value** | biaya ongkos kirim tiap satu produk.

* fitur pada tabel  `order_payments`:

Feature | Description
----------|---------------
**order_id** | identifikasi unik setiap order.
**payment_sequential** | pelanggan dapat membayar pesanan dengan lebih dari satu metode pembayaran. Jika dia melakukannya, urutan akan dibuat untuk mengakomodasi semua pembayaran.
**payment_type** |  metode pembayaran yang dipilih oleh customer.
**payment_installments** | jumlah angsuran yang dipilih oleh customer.
**payment_value** | total transaksi.



* fitur pada tabel  `orders`:

Fitur | Deskripsi
----------|---------------
**order_id** | identifikasi unik setiap order.
**customer_id** | identifikasi unik setiap customer.
**order_status** | status pesanan (delivered, shipped, etc).
**order_purchase_timestamp** | menunjukkan waktu pembelian.
**order_approved_at** | menunjukkan waktu persetujuan pembayaran.
**order_delivered_carrier_date** | menunjukkan waktu pengiriman pesanan. Saat itu ditangani ke mitra logistik.
**order_delivered_customer_date** | Menunjukkan waktu penerimaan pesanan. Saat itu ditangani oleh pelanggan.
**order_estimated_delivery_date** | Menunjukkan perkiraan tanggal pengiriman yang diinformasikan kepada pelanggan pada saat pembelian.


* fitur pada tabel  `order_reviews`:

Fitur | Deskripsi
----------|---------------
**review_id** | identifikasi unik setiap review.
**order_id** |  identifikasi unik setiap order.
**review_score** | Nilai kepuasan dengan rentang dari 1 sampai 5 yang diberikan oleh pelanggan.
**review_comment_title** | Judul komentar dari ulasan yang ditinggalkan oleh pelanggan, dalam bahasa Portugis.
**review_comment_message** | Isi komentar dari ulasan yang ditinggalkan oleh pelanggan, dalam bahasa Portugis.
**review_creation_date** | Menunjukkan tanggal pengiriman survei kepuasan kepada pelanggan.
**review_answer_timestamp** | Menampilkan Tanggal waktu jawaban survei kepuasan.


* fitur pada tabel  `products`:

Fitur | Deskripsi
----------|---------------
**product_id** | id setiap produk.
**product_category_name** | kategori nama produk, dalam bahasa Portugis.
**product_name_lenght** | Panjang karakter tiap nama produk.
**product_description_lenght** | Panjang karakter tiap deskripsi produk.
**product_photos_qty** | jumlah foto produk yang diterbitkan.
**product_weight_g** | berat produk diukur dalam gram.
**product_length_cm** | Panjang produk diukur (cm).
**product_height_cm** | Tinggi produk diukur  (cm).
**product_width_cm** | Lebar produk diukur (cm).


* fitur pada tabel `geolocation`:

Fitur | Deskripsi
----------|---------------
**geolocation_zip_code_prefix** | 5 digit pertama kode pos.
**geolocation_lat** | kordinat latitude.
**geolocation_lng** | kordinat longitude.
**geolocation_city** | nama kota.
**geolocation_state** | nama provinsi.


* fitur pada tabel  `category_name`:

Fitur | Deskripsi
----------|---------------
**product_category_name** | nama kategori produk dalam bahasa portugis.
**product_category_name_english** | nama kategori produk dalam bahasa inggris.
