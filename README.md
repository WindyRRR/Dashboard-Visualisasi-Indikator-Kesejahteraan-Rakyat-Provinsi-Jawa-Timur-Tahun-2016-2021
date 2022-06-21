<h1 align='center'> Pembangunan Dashboard Visualisasi Indikator Kesejahteraan Rakyat
 </h1>
<h2 align='center'>
Studi Kasus : Provinsi Jawa Timur Tahun 2016-2021
</h2>
<h3 align='center'>
Windy Rahmatul Azizah  (221910914, 3SD1)
</h3>
<br></br>

<h2 align='center'>Ringkasan</h2>
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 
Ringkasan— Kesejahteraan rakyat merupakan salah satu tujuan nasional dalam pembukaan UUD 1945. Kebijakan pemeerintah dalam meningkatkan kesejahteraan rakyat adalah pembangunan. Jawa Timur sebagai provinsi yang luas tentu memiliki kondisi geografis beragam sehingga ketercapaian pembangunan di setiap kabupaten/kota nya berbeda. Padahal pemerataan pembangunan harus diwujudkan untuk mencapai kesejahteraan rakyat yang adil. Oleh karena itu dibuatlah dashboard visualisasi indikator kesejahteraan rakyat Provinsi Jawa Timur untuk memudahkan pemerintah dalam melakukan pemantauan daerah yang memiliki indikator kesejahteraan rendah secara cepat dan akurat sehingga dapat ditindaklanjuti segera. Pembuatan dashboard ini memanfaatkan software Tableau 2022.1 dengan dimensi indikator antara lain dimensi penduduk, ekonomi, dan kesehatan. Data diperoleh dari website dan publikasi statistik kesejahteraan rakyat tahun 2021 BPS Provinsi Jawa Timur. Data yang digunakan berada dalam rentang waktu tahun 2016-2021. Visualisasi diawali dengan preprocessing yang meliputi seleksi data dan penggabungan data. Terdapat 4 halaman dashboard yang dihasilkan meliputi dashboard beranda, dashboard penduduk, dashboard ekonomi, dan dashboard kesehatan yang didalamnya berisi informasi garafik visual yang bersesuaian dengan masing-masing dimensi.
Kata Kunci— Dashboard, indikator kesejahteraan rakyat, informasi, tableau.
</p>
<h2 align='center'>BAB 1 <br/> LATAR BELAKANG</h2>


<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; yang tertuang dalam pembukaan UUD 1945 untuk memajukan kesejahteraan umum, mencerdaskan kehidupan bangsa serta mewujudkan suatu keadilan sosial bagi seluruh rakyat Indonesia. Berdasarkan tujuan yang tertuang dalam pembukaan UUD 1945 tersebut menandakan bahwa kesejahteraan rakyat merupakan hak yang harus dijamin oleh negara. Kesejahteraan hidup ini dapat diartikan pula sebagai suatu proses dinamis yang mengajarkan suatu nilai bagaimana kehidupan mereka akan berubah dan bertambah lebih baik maupun sebaliknya [1]. Keadaan lingkungan dari beberapa dimensi yang merosot secara tidak langsung dinilai mampu menjelaskan kualitas kehidupan dan kesejahteraan masyarakatnya [2]. Pada realitanya, tidak ada indikator khusus yang mutlak mampu menggambarkan suatu kualitas kesejahteraan rakyat sebab kesejahteraan ini bersifat subjektif karena memusat kepada kepuasan dan kebaikan hidup manusia saja [3]. Sehingga dalam hal ini kualitas kesejahteraan rakyat tidak bisa hanya diukur melalui satu aspek saja, ekonomi atau pembangunan misalnya melainkan harus mempertimbangkan beberapa aspek lain yang turut mendukung seperti kondisi penduduk, kondisi kesehatan, psikologi dan budaya. Pengukuran kesejahteraan masyarakat metropolitan Amerika Serikat yang dilakukan oleh Liu menguraikan bahwa kualitas kesejahteraan ini dapat diukur melalui lima komponen utama antara lain ekonomi, politik, sosial, kesehatan, pendidikan, dan lingkungan sekitar [4].
<br/>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Jawa Timur merupakan suatu Provinsi dengan luas wilayah 47.800 km persegi lebih luas dibandingkan Jawa Barat dan Jawa Tengah [5]. Dengan wilayah provinsi yang tergolong luas, tentunya Provinsi Jawa Timur ini memiliki kondisi geografis yang beragam dari wilayah yang mudah untuk dijangkau sampai wilayah yang membutuhkan akses yang lebih dalam menjangkaunya. Wilayah yang luas namun memiliki kondisi geografis sulit di Jawa Timur ini misalnya terdapat di Kabupaten Madiun, Probolinggo, dan Sampang [6]. Kondisi geografis Provinsi Jawa Timur ini menjadi perhatian karena saat ini kebijakan pemerinatah dalam meningkatkan kesejahteraan rakyat adalah dengan melakukan berbagai program pembangunan. Namun untuk wilayah-wilayah tertentu yang memiliki akses sulit dan merupakan wilayah terpencil tentu dikhawatirnya tidak maupun kurang terjangkau program pembangunan pemerintah sehingga menyebabkan capaian pembangunan di suatu wilayah provinsi khususnya akan berbeda-beda.
<br/>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Perkembangan hasil dari pembangunan ini apakah sudah tercapai atau belum tentu dibutuhkan suatu instrumen yang dapat memberikan gambaran kepada pemerintah secara cepat dan akurat sebagai  sarana untuk evaluasi dan pengambilan keputusan selanjutnya untuk mewujudkan suatu pemerataan pembangunan yang adil. Jika kesuksesan pembangunan suatu wilayah dikaitkan dengan kesejahteraan rakyatnya, maka kesuksesan pembangunan ini dapat diukur melalui indikator-indikator kesejahteraan rakyat. Pengukuran indikator kesejahteraan rakyat ini dilakukan Badan Pusat Statistik (BPS) melalui Survei Sosial Ekonomi Nasional (SUSENAS).
<br/>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Dengan demikian, dalam menjawab kebutuhan pemerintah untuk mewujudkan suatu instrument yang dapat memvisualisasikan kesejahteraan rakyat secara cepat dan akuran sebagai tolok ukur tercapainya pemerataan pembangunan maka dibuatlah dashboard visualisasi indikator kesejahteraan rakyat Provinsi Jawa Timur untuk melihat daerah kabupaten/kota mana yang masih memiliki penyusun indikator tersebut yang rendah sehingga daerah tersebut diduga pencapaian pembangunannya pun juga masih rendah. Namun karena indikator pengukur kesejahteraan rakyat ini sangat beragam dan subjektif sedangkan konsep dari penyusunan dashboard visualisasi informasi harus menyajikan informasi yang sederhana dan efektif namun dapat mewakili keseluruhan informasi yang ingin disampaikan, maka dalam pembuatan dashboard visualisasi ini hanya digunakan beberapa dimensi indikator saja yang diduga cukup kuat dalam mengukur kualitas kesejahteraan rakyat. Dimensi tersebut antara lain dimensi penduduk, dimensi ekonomi, dan dimensi kesehatan. Dengan dibuatkannya dashboard visualisasi indikator kesejahteraan rakyat Provinsi Jawa Timur ini diharapkan pemerintah dapat melakukan pemantauan terkait kondisi indikator kesejahteraan rakyat pada daerah kabupaten/kota di Jawa Timur untuk mencari wilayah yang kualitas kesejahteraannya masih rendah sehingga dapat dilakukan evaluasi serta penindaklanjutan dengan segera terkait pembangunan yang ada di wilayah tersebut sehingga pemerataan pembangunan dapat tercapai dan tujuan nasional terkait memajukan kesejahteraan umum pun dapat tercapai.
</p> 

## B. Rumusan Masalah
<ol>
  <li>Belum tersedia visualisasi data gempa bumi di wilayah teritorial Indonesia tahun 2017-2021.</li>
  <li>Belum tersedia dashboard yang menyajikan visualisasi data gempa bumi di wilayah teritorial  Indonesia tahun 2017-2021.</li>
</ol>

## C. Tujuan
<ol>
  <li>Membuat visualisasi data gempa bumi di wilayah teritorial Indonesia tahun 2017-2021.</li>
  <li>Membuat dashboard yang menyajikan visualisasi data gempa bumi di wilayah teritorial Indonesia tahun 2017-2021.</li>
</ol>

<br></br>

<h2 align='center'>BAB 2 <br/> KAJIAN PUSTAKA</h2>

## A. Gempa Bumi
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Gempa bumi merupakan salah satu bencana alam yang sering terjadi di Indonesia. Menurut Badan Meteorologi Klimatologi dan Geofisika, gempa bumi adalah peristiwa bergetarnya bumi akibat pelepasan energi di dalam bumi secara tiba-tiba yang ditandai dengan patahnya lapisan batuan pada kerak bumi. Akumulasi energi penyebab terjadinya gempa bumi dihasilkan dari pergerakan lempeng-lempeng tektonik. Energi yang dihasilkan dipancarkan ke segala arah berupa gelombang gempa bumi sehingga efeknya dapat dirasakan sampai ke permukaan bumi. Gempa bumi dengan kekuatan yang besar dapat berpotensi menimbulkan tsunami.</p>

## B. Visualisasi Data  
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Visualisasi data merupakan cara untuk merepresentasikan data dengan tampilan yang menarik sehingga lebih mudah dipahami. Menurut Kirk (2012:17), visualisasi data adalah representasi dan penyajian data yang memanfaatkan kemampuan persepsi visual seseorang untuk memperkuat kognisi. Representasi data adalah cara seseorang memutuskan untuk menggambarkan data melalui pilihan bentuk fisik. Sedangkan penyajian data lebih dari proses representasi data, penyajian data mencakup bagaimana seseorang mengintegrasikan representasi data kedalam keseluruhan pekerjaan yang dikomunikasikan, termasuk pemilihan warna, anotasi, dan fitur interaktif. 
<br/>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Visualisasi data memanfaatkan kemampuan persepsi visual seseorang yang berhubungan dengan pemahaman ilmiahnya tentang bagaimana mata dan otak mengolah informasi dengan lebih efektif. Sehingga dengan visualisasi data, informasi yang akan disampaikan dapat lebih mudah diterima dan dipahami. Selain itu, memperkuat kognisi pada visualisasi data merupakan proses untuk memaksimalkan seberapa efisien dan efektif seseorang dalam mengolah informasi menjadi pemikiran, wawasan dan pengetahuan.</p>

<br></br>

<h2 align='center'>BAB 3 <br/> METODOLOGI</h2>

## A. Pengumpulan Data
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Data yang digunakan dalam penelitian ini merupakan data sekunder, yaitu Earthquake  Around Indonesian Territory dari Kaggle. Data ini juga dapat ditemukan di situs resmi Badan Meteorologi, Klimatologi, dan Geofisika (BMKG). Seperti judulnya, data ini berisi kejadian gempa bumi di sekitar wilayah Indonesia beserta keterangan waktu, lokasi, kedalaman dan besar magnitudonya dari tanggal 1 Januari 2017 hingga 12 April 2021.</p>

## B. Analisis Data
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Metode analisis yang digunakan pada penelitian adalah analisis deskriptif dengan pendekatan kuantitatif.</p>

## C. Perancangan
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Visualisasi data yang akan dibuat dalam penelitian ini adalah dashboard informasi. Perancangan dimulai dengan cara membuat mock up dari desain dashboard yang akan dibuat. Sebaran titik-titik gempa akan divisualisasikan dalam peta dengan titik koordinatnya (longitude dan latitude). Frekuensi gempa akan divisualisasikan dengan menggunakan bar chart, sementara sebaran magnitudo gempa divisualisasikan dengan histogram. Visualisasi ini kemudian akan di-filter berdasarkan tahunnya.</p>

## D. Implementasi
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Implementasi dilakukan dengan cara membuat dashboard untuk menampilkan visualisasi data gempa bumi di wilayah teritorial Indonesia tahun 2017-2021 sesuai dengan mock up yang sudah dibuat pada tahap perancangan. Dashboard dibuat dengan menggunakan Tableau.
</p>

<br></br>

<h2 align='center'>BAB 4 <br/> HASIL DAN PEMBAHASAN </h2>

## A. Pengolahan Data
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Data yang digunakan dalam penelitian ini tidak memiliki missing value sehingga data dapat langsung digunakan. Selanjutnya data ditambahkan kategori day dan night. Day digunakan untuk mengkategorikan gempa bumi yang terjadi pada siang hari, sedangkan night digunakan untuk mengkategorikan gempa bumi yang terjadi pada malam hari.</p>

## B. Visualisasi Data
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Visualisasi data yang digunakan dalam penelitian ini disesuaikan dengan kebutuhan informasi yang perlu disampaikan dari data yang akan disajikan. Berikut adalah visualisasi data yang dibuat pada penelitian ini:</p>  

### 1. Visualisasi data persebaran gempa bumi di wilayah teritorial Indonesia  
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Warna pada visualisasi data persebaran gempa bumi di Indonesia menggambarkan kedalaman dari pusat gempa, dengan kedalaman terdangkal sampai terdalam digambarkan dengan perubahan warna dari merah sampai biru. Sedangkan ukuran bubble menggambarkan kekuatan magnitudo gempa, semakin besar ukurannya semakin tinggi magnitudo gempanya.</p>  

![Map](/img/map.png)

### 2. Visualisasi data frekuensi gempa bumi di wilayah teritorial Indonesia per bulan dalam setahun

![Frekuensi](/img/frekuensi.png)

### 3. Visualisasi data frekuensi gempa bumi di wilayah teritorial Indonesia per bulan dalam setahun, serta kategori day dan night
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Warna orange untuk kategori day (gempa bumi yang terjadi pada siang hari) dan warna biru untuk kategori night (gempa bumi yang terjadi pada malam hari).</p>

![DayNight](/img/daynight.png)

### 4. Visualisasi data magnitude gempa bumi di wilayah teritorial Indonesia dalam bentuk histogram

![Histogram](/img/histogram.png)

## C. Dashboard
Visualisasi data yang sudah dibuat selanjutnya akan diintegrasikan menjadi satu kesatuan dalam suatu dashboard. Dashboard yang dibuat akan ditampilkan pada aplikasi web menggunakan aplikasi Tableau Public yang linknya dapat diakses
  [di sini](https://public.tableau.com/views/DashboardGempaDiBumiIndonesia/DS2017?:language=en-US&:display_count=n&:origin=viz_share_link "Dashboard Gempa Bumi").
  <br></br>
Berikut adalah tampilan dashboard yang sudah dibangun:

![Dashboard](/img/dashboard.png)

<br></br>

<h2 align='center'>BAB 5 <br/> PENUTUP</h2>

## A. Kesimpulan
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Dashboard yang dibangun sudah mampu menampilkan visualisasi data gempa bumi di wilayah teritorial Indonesia tahun 2017-2021. Visualisasi data yang dibuat pada penelitian ini sudah cukup untuk menggambarkan informasi dasar terkait gempa bumi di Indonesia seperti frekuensi gempa bumi, kekuatan dan kedalaman gempa bumi, serta persebaran gempa bumi di Indonesia.</p>  

## B. Saran
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Berikut adalah saran untuk pengembangan lebih lanjut visualisasi data gempa bumi di Indonesia:
<ol>
  <li>Pada visualisasi data persebaran gempa bumi, dapat disajikan persebaran gempa bumi berdasarkan provinsi dan disertai dengan batas wilayah yang jelas.</li>
  <li>Dapat ditambahkan ringkasan kejadian gempa untuk masing-masing provinsi.</li>
  <li>Dapat dibuat klasifikasi wilayah yang rawan gempa atau tidak.</li>
</ol>
</p>  

<br></br>

<h2 align='center'> DAFTAR PUSTAKA </h2>

<p align='justify'>
 <ol>
   <li>Badan Meteorologi Klimatologi dan Geofisika. 2021.“Apakah Gempabumi itu?”. Dalam http://inatews2.bmkg.go.id/. Diunduh pada 1 Juni 2021.
</li>
   <li>Kirk, Andy. 2012. Data Visualization: a successful design process. Birmingham. Packt Publishing Ltd.
</li>
</ol>
</p>

<br></br>
## Kelompok 2 Tugas Akhir Mata Kuliah Visualisasi Data 3SD2
- Daris Azhar	(221810233) 
- Emir Lutfi	(221810266)
- Joice Evangelista Lase	(221810359)
- Muhammad Ibrah Reynaldi Tanjung	(221810459)
- Talitha Nabila Saifana	(221810619)
- Zuhrotur Rofiah	(221810682)
