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

***
## **Analytics**
Visualisasi Tableau dapat dilihat pada link berikut : [Tableau Dashboard](https://public.tableau.com/app/profile/hari.prasetyo/viz/FinalProject_16797569810040/Dashboard1)
<br>
<br>

![Tableau Dashboard 1](https://github.com/PurwadhikaDev/BetaGroup_JC_DS_OL_08_FinalProject/blob/main/Picture/Tableau%201.png)
<br>
<br>

#### Sales Overview
Jumlah order mengalami peningkatan dari tahun 2016 sampai 2018. Hal ini menunjukkan perusahaan Olist berkembang dengan baik. Jumlah order terbanyak terdapat pada November 2017 yaitu sebanyak 7188. Olist Ecommerce sendiri baru didirikan pada tahun 2015 . Artinya sebagai Ecommerce yang baru berdiri dan mengalami perkembangan yang cukup cepat dari tahun 2016-2018 menunjukkan bahwa Olist Ecommerce sudah cukup baik dalam menjangkau konsumen. Total Sales tahun 2018 mencapai R$ 11,113,007, **meningkat 20,4%** dari tahun 2017 walaupun tahun 2018 belum selesai.

Ref: https://www.crunchbase.com/organization/olist

<br>
<br>

![Tableau Dashboard 2](https://github.com/PurwadhikaDev/BetaGroup_JC_DS_OL_08_FinalProject/blob/main/Picture/Tableau%202.png)

#### Kategoti Produk
Top 5 kategori produk berdasarkan jumlah penjualan berbeda dengan apabila berdasarkan quantity penjualannya. Artinya, Olist Ecommerce dapat menyesuaikan kategori produk yang ingin ditingkatkan sesuai dengan tujuannya (apakah meningkatkan quantity ataupun jumlah penjualan). Hal yang dapat dilakukan misalnya dengan memperbanyak variasi barang yang ditawarkan pada kategori-kategori tersebut dan juga bisa dengan memperbanyak merchant yang berkualitas di kategori produk tersebut
 Hal ini juga dapat meningkatkan Brand Image dari Olist Ecommerce sendiri, sehingga Olist Ecommerce dapat lebih dikenal dan meningkatkan penjualannya.

#### Waktu Transaksi
Jumlah transaksi tertinggi dimulai dari jam 10 pagi hingga jam 4 sore dan kemudian menurun. Jumlah order kembali naik pada jam 8 hingga jam 10 malam. Hal tersebut disebabkan pada jam tersebut orang-orang mulai aktif melakukan kegiatannya, termasuk berbelanja online. sedangkan pada jam 1 hingga jam 6 pagi adalah jumlah transaksi terendah disebabkan orang-orang sedang beristirahat.
<br>
<br>
![Cohort](https://github.com/PurwadhikaDev/BetaGroup_JC_DS_OL_08_FinalProject/blob/main/Picture/Cohort.png)
<br>
<br>
#### Cohort Analysis
Berdasarkan hasil cohort analysis di atas yang menggunakan periode bulanan, diperoleh bahwa hanya kurang dari 1% customer yang kembali melakukan transaksi di bulan-bulan berikutnya. Hal ini sejalan dengan analisa pada poin 5.7 dimana mayoritas customer baru pernah bertransaksi sebanyak 1x saja di Olist Ecommerce. Tentunya hal ini perlu diperhatikan oleh Olist Ecommerce. 
***
## **Customer Segmentation**
### Recency, Frequency & Monetary

![RFM](https://github.com/PurwadhikaDev/BetaGroup_JC_DS_OL_08_FinalProject/blob/main/Picture/RFM.png)

Berdasarkan segmentasi RFM yang sudah dilakukan, diperoleh 6 segmen dengan 3 segmen yang dominan secara jumlah yaitu Recent Users, Lost Customers, dan Can't Lose Them, sedangkan 3 segmen lainnya yaitu Loyal Customers, About to Sleep, dan Champions jumlah nya tidak dominan. Berikut beberapa rekomendasi yang dapat dilakukan melalui kegiatan pemasaran :
1. Recent Users <br>
Jika dilihat dari data historical, Olist Ecommerce kesulitan untuk mempertahankan customernya (terbukti dari frekuensi transaksi dari unique customer mayoritas hanya 1x saja). Segmen Recent Users akan menjadi potensi yang baik bagi Olist Ecommerce dimana customer baru saja melakukan transaksi di Olist Ecommerce. Olist Ecommerce perlu tetap menjaga relationship nya dengan segmen Recent Users ini. 

2. Lost Customers <br>
Segmen ini merupakan customer yang churn. Untuk mendapatkan kembali customer ini perlu usaha yang lebih. 

3. Can't Lose Them <br>
Segmen ini perlu dimonitor dan diberi perlakuan khusus untuk dapat mempertahankannya.

4. Loyal Customers <br>
Segmen ini sudah puas dengan produk Olist namun perlu dijaga agar customer merasa dihargai.

5. About To Sleep <br>
Segmen ini sudah lama tidak melakukan transaksi dan sebentar lagi akan menjadi Lost Customers jika tidak diberi perlakuan apapun. 

6. Champions <br>
Segmen ini merupakan segmen terbaik yang dimiliki Olist Ecommerce sehingga sangat penting sekali untuk menjaga kepercayaan dari segmen ini.

### KMeans Clustering Using Combined Database and RFM
![Cluster](https://github.com/PurwadhikaDev/BetaGroup_JC_DS_OL_08_FinalProject/blob/main/Picture/Cluster.png)
***

## Conclusion


## Recommendation


