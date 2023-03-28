# <h1><b>Customer Segmentation of Olist Brazilian ECommerce</b></h1>

**By: Beta Group**

1. Yosafat Kurniawan
2. Hari Prasetyo
***
## **Problem Statement**
![Olist Data Schema](https://static-s.aa-cdn.net/img/gp/20600011714266/eqLTXWdyygKUf85JsCXmcLSr1GnoYNLJfFVCmY-N8xGFr2T3PWwNcFdJ2Sx7MwcO6ac?v=1)

**Context**

Dataset ini disediakan oleh Olist, department store terbesar di pasar Brazil. Olist menghubungkan bisnis kecil dari seluruh Brazil ke seluruh jaringan tanpa kerumitan dan dengan satu kontrak. Penjual dapat menjual produknya melalui Olist Store dan mengirimkannya langsung ke pelanggan menggunakan mitra logistik dari Olist. Setelah konsumen membeli produk dari Olist Store, penjual akan diberi notifikasi untuk memenuhi pesanan tersebut. Setelah pelanggan menerima produk atau perkiraan tanggal pengiriman, pelanggan mendapatkan survei kepuasan melalui email dimana pelanggan dapat memberikan catatan terhadap pengalaman pembelian dan juga menuliskan komentar.

**Problem Statement**

Bisnis ecommerce tentunya membutuhkan transaksi dari konsumen-konsumennya secara berkelanjutan agar dapat bertahan. Olist Ecommerce perlu mengetahui seperti apa karakteristik dan perilaku dari konsumennya. Dengan demikian, Olist Ecommerce akan dapat menentukan strategi apa yang perlu diambil ke depannya dalam kegiatan pemasarannya.

Segmentasi dan target pasar merupakan salah satu fondasi dasar dalam bisnis Ecommerce. Dengan melakukan prediksi segmentasi pasar, kita dapat mengarahkan strategi kegiatan pemasaran kepada segmen/kelompok konsumen yang disesuaikan dengan karakteristiknya, sehingga kegiatan pemasaran bisa lebih efektif dan efisien. Segmentasi pasar dapat ditinjau dari berbagai sudut pandang, seperti kemampuan bayar, demografi, waktu, dll.

**Goals**

Berdasarkan permasalahan tersebut, perusahaan Olist ingin memiliki kemampuan 
untuk memprediksi segmentasi dari konsumen-konsumennya, sehingga perusahaan dapat melakukan kegiatan pemasaran dengan efektif dan meningkatkan penjualannya.

**Analytic Approach**

Beberapa metode analitik yang akan digunakan yaitu pertama melakukan analisis RFM dan kedua melakukan Clustering dengan metode KMeans. Dengan menggunakan Clustering Kmeans, dapat diperoleh segmentasi konsumen sesuai dengan kemiripan karakteristiknya. Dengan analisis RFM, kita dapat melihat segmen konsumen juga yang ditinjau dari karakteristik Recency, Frequency, dan Monetary nya. Pada akhirnya di tiap metode yang dilakukan akan dapat ditentukan kegiatan pemasaran yang sesuai untuk masing-masing segmen konsumen.

**Metric Evaluation**

Evaluasi metrik yang akan digunakan adalah elbow method dan silhouette score. Kedua metode tersebut digunakan untuk melihat berapa jumlah cluster yang optimal untuk clustering. Elbow method dapat melihat perubahan tingkat kemiripan setiap penambahan satu cluster. Jumlah cluster yang dipilih adalah jumlah cluster dimana tingkat kemiripan clusternya berubah dari perubahan yang signifikan menjadi tidak signifikan. Pada grafik Elbow Method dapat dilihat pada titik yang membentuk siku. Sedangkan Silhouette score pada dasarnya suatu ukuran yang mengkombinasikan seberapa dekat setiap data poin dalam suatu cluster yang sama dengan seberapa dekat setiap data poin pada cluster tersebut dengan data poin pada cluster lainnya. Jumlah cluster yang dipilih adalah yang memiliki nilai shilouete paling tinggi.
***
## **Data Understanding**
Dataset dapat diperoleh di situs [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).<br>
Data terdiri dari 9 dataset dengan skema seperti berikut.
![Olist Data Schema](https://imgur.com/HRhd2Y0.png)


![Olist Data Schema](https://drive.google.com/file/d/1aFm_rMFaOtVehg0czPiAuXCKbQd9-ag6/view?usp=sharing)
