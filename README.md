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


<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Kesejahteraan rakyat merupakan salah satu tujuan nasional yang tertuang dalam pembukaan UUD 1945 untuk memajukan kesejahteraan umum, mencerdaskan kehidupan bangsa serta mewujudkan suatu keadilan sosial bagi seluruh rakyat Indonesia. Berdasarkan tujuan yang tertuang dalam pembukaan UUD 1945 tersebut menandakan bahwa kesejahteraan rakyat merupakan hak yang harus dijamin oleh negara. Kesejahteraan hidup ini dapat diartikan pula sebagai suatu proses dinamis yang mengajarkan suatu nilai bagaimana kehidupan mereka akan berubah dan bertambah lebih baik maupun sebaliknya [1]. Keadaan lingkungan dari beberapa dimensi yang merosot secara tidak langsung dinilai mampu menjelaskan kualitas kehidupan dan kesejahteraan masyarakatnya [2]. Pada realitanya, tidak ada indikator khusus yang mutlak mampu menggambarkan suatu kualitas kesejahteraan rakyat sebab kesejahteraan ini bersifat subjektif karena memusat kepada kepuasan dan kebaikan hidup manusia saja [3]. Sehingga dalam hal ini kualitas kesejahteraan rakyat tidak bisa hanya diukur melalui satu aspek saja, ekonomi atau pembangunan misalnya melainkan harus mempertimbangkan beberapa aspek lain yang turut mendukung seperti kondisi penduduk, kondisi kesehatan, psikologi dan budaya. Pengukuran kesejahteraan masyarakat metropolitan Amerika Serikat yang dilakukan oleh Liu menguraikan bahwa kualitas kesejahteraan ini dapat diukur melalui lima komponen utama antara lain ekonomi, politik, sosial, kesehatan, pendidikan, dan lingkungan sekitar [4].
<br/>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Jawa Timur merupakan suatu Provinsi dengan luas wilayah 47.800 km persegi lebih luas dibandingkan Jawa Barat dan Jawa Tengah [5]. Dengan wilayah provinsi yang tergolong luas, tentunya Provinsi Jawa Timur ini memiliki kondisi geografis yang beragam dari wilayah yang mudah untuk dijangkau sampai wilayah yang membutuhkan akses yang lebih dalam menjangkaunya. Wilayah yang luas namun memiliki kondisi geografis sulit di Jawa Timur ini misalnya terdapat di Kabupaten Madiun, Probolinggo, dan Sampang [6]. Kondisi geografis Provinsi Jawa Timur ini menjadi perhatian karena saat ini kebijakan pemerinatah dalam meningkatkan kesejahteraan rakyat adalah dengan melakukan berbagai program pembangunan. Namun untuk wilayah-wilayah tertentu yang memiliki akses sulit dan merupakan wilayah terpencil tentu dikhawatirnya tidak maupun kurang terjangkau program pembangunan pemerintah sehingga menyebabkan capaian pembangunan di suatu wilayah provinsi khususnya akan berbeda-beda.
<br/>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Perkembangan hasil dari pembangunan ini apakah sudah tercapai atau belum tentu dibutuhkan suatu instrumen yang dapat memberikan gambaran kepada pemerintah secara cepat dan akurat sebagai  sarana untuk evaluasi dan pengambilan keputusan selanjutnya untuk mewujudkan suatu pemerataan pembangunan yang adil. Jika kesuksesan pembangunan suatu wilayah dikaitkan dengan kesejahteraan rakyatnya, maka kesuksesan pembangunan ini dapat diukur melalui indikator-indikator kesejahteraan rakyat. Pengukuran indikator kesejahteraan rakyat ini dilakukan Badan Pusat Statistik (BPS) melalui Survei Sosial Ekonomi Nasional (SUSENAS).
<br/>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Dengan demikian, dalam menjawab kebutuhan pemerintah untuk mewujudkan suatu instrument yang dapat memvisualisasikan kesejahteraan rakyat secara cepat dan akuran sebagai tolok ukur tercapainya pemerataan pembangunan maka dibuatlah dashboard visualisasi indikator kesejahteraan rakyat Provinsi Jawa Timur untuk melihat daerah kabupaten/kota mana yang masih memiliki penyusun indikator tersebut yang rendah sehingga daerah tersebut diduga pencapaian pembangunannya pun juga masih rendah. Namun karena indikator pengukur kesejahteraan rakyat ini sangat beragam dan subjektif sedangkan konsep dari penyusunan dashboard visualisasi informasi harus menyajikan informasi yang sederhana dan efektif namun dapat mewakili keseluruhan informasi yang ingin disampaikan, maka dalam pembuatan dashboard visualisasi ini hanya digunakan beberapa dimensi indikator saja yang diduga cukup kuat dalam mengukur kualitas kesejahteraan rakyat. Dimensi tersebut antara lain dimensi penduduk, dimensi ekonomi, dan dimensi kesehatan. Dengan dibuatkannya dashboard visualisasi indikator kesejahteraan rakyat Provinsi Jawa Timur ini diharapkan pemerintah dapat melakukan pemantauan terkait kondisi indikator kesejahteraan rakyat pada daerah kabupaten/kota di Jawa Timur untuk mencari wilayah yang kualitas kesejahteraannya masih rendah sehingga dapat dilakukan evaluasi serta penindaklanjutan dengan segera terkait pembangunan yang ada di wilayah tersebut sehingga pemerataan pembangunan dapat tercapai dan tujuan nasional terkait memajukan kesejahteraan umum pun dapat tercapai.
</p> 
<br></br>

<h2 align='center'>BAB 2 <br/> TUJUAN PENELITIAN</h2>

<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
Adapun tujuan dalam penelitian ini adalah untuk memberikan gambaran berupa visualisasi data terkait indikator kesejahteraan rakyat Provinsi Jawa Timur pada rentang waktu 2016-2021. Dengan demikian melalui visualisasi ini nantinya dapat dipaantau bagaimana perkembangan indikator-indikator penyusun tingkat kesejahteraan rakyat tersebut  apakah terdapat kenaikan maupun penurunan yang akan berimplikasi pada perubahan tingkat kesejahteraan rakyat secara visual melalui data yang disajikan sebelum melalui penelusuran yang lebih lanjut.
</p>

<br></br>
<h2 align='center'>BAB 3 <br/> KAJIAN PUSTAKA</h2>

## A. Statistik Kesejahteraan Rakyat
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Statistik Kesejahteraan rakyat merupakan data yang dikumpulkan oleh Badan Pusat Statistik (BPS) berupa indikator-indikator yang mempengaruhi kesejahteraan rakyat [7]. Data dikumpulkan melalui Survei Sosial Ekonomi Nasional (SUSENAS) pada bulan Maret 2021. Statistik dari indikator kesejahteraan rakyat yang dikumpulkan meliputi kependudukan, kesehatan, balita, pendidikan, fertilitas dan keluarga berencana, perumahan, pengeluaran perkapita, jaminan sosial rumah tangga, teknologi dan informasi, kuesioner dan Nilai Relatif Standar Error (RSE). Namun dalam rangkan pembuatan dashboard visualisasi indikator kesejahteraan  rakyat ini tidak semua data indikator tersebut akan dtampilkan pada dashboard. Hal ini disebabkan oleh penyusunan dashboard visualisasi yang harus efektif dan tidak terlalu melebar jadi akan dipilih beberapa indikator saja yang dinilai bisa menjadi suatu pusat dalam menentukan kualitas kesejahteraan rakyat.</p>

## B. Dashboard Informasi  
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Dashboard informasi merupakan suatu media dalam menampilkan informasi melalui bentuk-bentuk grafik tertentu seperti indikator visual, diagram, maupun bentuk grafik yang menyajikan informasi dinamis serta relevan [8]. Dashboard berperan dalam mewujudkan penyusunan dan penggabungan suatu informasi dalam bentuk visual yang dapat disesuaikan sehingga informasi yang ditampilkan efektif dan sesuai kebutuhan [9]. Disamping itu, dashboard merupakan tampilan visual dari informasi terpenting yang diperlukan untuk mengelola suatu bidang organisasi (bisa suatu organisasi data) yang diatur pada satu layar computer sehingga mempermudah pemantauan [10]. Dashboard informasi mampu digunakan untuk monitoring sistem drainase secara realtime [11]. Selain itu perancangan sistem dashboard juga merupakan media yang bisa digunakan untuk monitoring indikator kinerja pada Universitas [12]. Dari pengertian dan beberapa penelitian sebelumnya terkait dashboard ini jelas bahwa dashboard merupakan media yang digunakan untuk memantau/monitoring suatu informasi yang ingin didapatkan maknanya dengan mudah. Dengan pembangunan suatu dashboard informasi harapannya adalah mampu mempercepat pemahaman dan penngambilan keputusan berdasarkan kondisi dari data/informasi yang saat ini dilihat dan lebih baik lagi jika bisa terus dilakukan pemantauan secara realtime.</p>

## B. Visualisasi Data 
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Visualisasi data merupakan teknik penyajian data efektif yang melalui proses abstraksi suatu data yang detail menjadi informasi yang lebih mudah diterima dan diserap oleh pembaca [13]. Dengan melakukan visualisasi, suatu data dapat diubah menjadi informasi yang dapat dimengerti secara universal [14]. Visualisasi data hampir mirip konsepnya dengan proses manusia dalam berkomunikasi, hanya saja bedanya visualisasi ini tidak melalui pembicaraan namun melalui sebuah tampilan yang ada di layar. Dengan demikian sukses tidaknya suatu visualisasi data dalam menyampaikan informasi yang terkandung adalah bergantung dengan bagaimana car akita menyampaikan dan mengemas informasi yang akan diberikan dengan fokus, memberi jawaban yang jelas, dan tidak terlalu detail.</p>
<br></br>

<h2 align='center'>BAB 4 <br/> METODE PENELITIAN</h2>

## A. Data dan Sumber Data
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Data yang digunakan dalam penelitian ini merupakan data sekunder yang diambil dari website Badan Pusat Statistik (BPS) Provinsi Jawa Timur beserta publikasi statistik kesejahteraan rakyat Provinsi Jawa Timur tahun 2021. Variabel yang diammbil untuk mengukur indikator kesejahteraan eakyat meliputi dimensi penduduk yaitu variabel jumlah penduduk total, jumlah penduduk miskin, IPM, TPT dan TPAK di setiap Kabupaten/Kota [15]. Selanjutnya adalah dimensi ekonomi yang meliputi variabel pengeluaran per kapita dan pertumbuhan ekonomi. Kemudian disertakan juga dimensi kesehatan yang meliputi variabel penduduk penerima layanan jaminan kesehatan dan jumlah desa menurut ketersediaan fasilitas kesehatan. Selain ketiga dimensi tersebut, disertakan pula variabel pendukung lain seperti rata-rata lama sekolah, angka harapan hidup, dan PDRB ADHK.</p>

## B. Seleksi Data
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Data yang telah diambil dari website maupun publikasi BPS Provinsi Jawa Timur selanjutnya diseleksi untuk memilih kolom data yang dibutuhkan dan menghapus kolom yang tidak dibutuhkan. Selanjutnya pada masing-masing sheet diberikan kolom khusus berupa ID untuk memudahkan proses penggabungan tabel pada Tableau.</p>

## C. Penggabungan Data
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Data yang digunakan dalam proses pembuatan visualisasi ini tidak terdapat dalam satu sheet yang sama sebab terdapat file shp untuk peta yang diperoleh secara terpisah. Dengan demikian ketika akan melakukan pengolahan pada Tableau harus digabungkan terlebih dahulu agar menjadi satu file data yang telah memuat semua informasi. Penggabungan ini dilakukan melalui atribut ID yang sama di setiap sheet nya.</p>

## D. Visualisasi Data
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Tahap selanjutnya pada data yang telah digabungkan adalah memvisualisasikan dengan berbagai macam grafik yang sesuai dengan struktur data. Proses visualisasi data dalam penelitian ini menggunakan software Tableau versi 2022.1.
</p>

## D. Pembuatan Dashboard
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Setelah visualisasi data pada masing-masing komponen selesai dilakukan, tahap selanjutnya adalah menyatukan seluruh visualisasi tersebut dalam dashboard informasi supaya visualisasi yang ditampilkan lebih tersusun dengan kategori yang tepat. Pada penelitian ini dibuat empat halaman dashboard yang terdiri dari beranda, dimensi penduduk, dimensi ekonomi, dan dimensi kesehatan. Pada masing-masing dashboard tersebut akan saling terhubung dan setiap dimensi akan menampilkan visualisasi yang masih dalam lingkup dimensi tersebut.
</p>
<br></br>

<h2 align='center'>BAB 5 <br/> HASIL DAN PEMBAHASAN </h2>

<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Hasil dari pembuatan dashboard ini antara lain dashboard yang dapat diakses secara publik</p>

[di sini](https://public.tableau.com/app/profile/windy.rahmatul.azizah/viz/UjianAkhirSemesterVisualisasiData/DashBeranda).

<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Pada proses pembuatan dashboard visualisasi yang telah dilakukan, dihasilkan empat halaman dashboard yang saling terhubung di antaranya halaman beranda, halaman dashboard untuk visualisasi dimensi penduduk, halaman dashboard untuk visualisasi dimensi ekonomi, dan halaman dashboard untuk visualisasi dimensi kesehatan. Di masing-masing dashboard berisikan grafik visualisasi data yang sesuai dengan kelompok dimensinya. 
Untuk halaman dashboard beranda, ditampilkan pada gambar 1 berikut.
</p>

![Gambar 1](/images/gbr1.png)
<p align='justify'>
Pada dashboard beranda ini bertujuan untuk menampilkan atau memvisualisasikan data secara umum terkait beberapa variabel yang memberikan gambaran tentang penduduk yang ada di Jawa Timur disesuaikan juga dengan variabel-variabel yang menjadi penyusun indikator kesejahteraan rakyat.
</br> &nbsp; &nbsp; &nbsp; &nbsp; &nbspVisualisasi pertama yaitu peta persebaran penduduk berdasarkan kabupaten/kota di Jawa Timur. Visualisasi ditunjukkan pada gambar 2 berikut.
</p>

![Gambar 2](/images/gbr2.png)

<p align='justify'>
Banyaknya jumlah penduduk yang mendiami suatu kota/kabupaten di Jawa Timur ditunjukkan oleh kepekatan warna pada peta tersebut. Warna yang terang menunjukkan jumlah penduduk  yang lebih rendah daripada daerah yang memiliki warna pekat. Data jumlah penduduk yang dihasilkan pun tidak hanya terbatas dalam rentang satu tahun saja. Pada pojok kanan terdapat menu dropdown untuk mengganti tahun yang diinginkan untuk melihat kondisi persebaran penduduk menurut kabupaten/kota. Selain itu, meskipun pada peta tidak terdapat keterangan label nama kabupaten/kota namun nantinya pada tampilan dashboard sesungguhnya ketika kursor diarahkan ke bagian wilayah peta tersebut maka akan menampilkan keterangan tentang nama kabupaten/kota neserta jumlah penduduk di wilayah tersebut pada tahun yang telah dipilih.
</p>

![Gambar 3](/images/gbr3.png)

<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; 
Angka Harapan Hidup (AHH) saat lahir merupakan rata-rata atau perkiraan usia hidup seseorang yang dapat ditempuh sejak seseorang tersebut dilahirkan. AHH ini dimasukkan dalam indikator kesejahteraan rakyat sebab AHH dapat mengukur kualitas kesehatan masyarakat. Selanjutnya adalah Rata-rata Lama Sekolah (RLS) yang merupakan perkiraan jumlah tahun yang ditempuh seorang penduduk dalam menjalani pendidikan formal. Dengan menggunakan RLS ini kualitas pendidikan masyarakat suatu wilayah dapat diketahui. Kemudian Produk Domestik Regional Bruto Atas Dasar Harga Konstan (PDRB ADHK) merupakan nilai tambah barang dan jasa hasil dari kegiatan ekonomi suatu daerah yang dihitung dengan menggunakan harga pada tahun tertentu sebagai tahun dasar. Dengan melihat PDRB ini diharapkan dapat menjadi suatu ukuran kondisi perekonomian suatu daerah. Ketiga variabel tersebut penting dalam menggambarkan indikator kesejahteraan rakyat. Pada halaman dashboad ini dapat dilihat nilai dari ketiga variabel tersebut sesuai dengan tahun yang dipilih. Dengan demikian pada visualisasi ini diharapkan dapat menjadi unstrumen pemantau nilai dari variabel penting penyusun indikator kesejahteraan rakyat. Interpretasi pada tahun 2021 penduduk Jawa Timur rata-rata memiliki kesempatan hidup selama kurang lebih 72 tahun sejak dia lahir, memiliki penduduk yang rata-rata menempuh pendidikan formal selama 9 tahun, dan PDRB ADHK nya sebesar 39.447.
</br>&nbsp; &nbsp; &nbsp; &nbsp;Pada halaman dashboard beranda terdapat menu penduduk, ekonomi, dan kesehatan yang tujuannya adalah ketika menu tersebut diklik/dipilih oleh pengguna maka akan mengarahkan pengguna tersebut pada halaman dashboard yang dipilih. Misalkan pengguna memilih dashboard penduduk maka akan dialihkan ke halaman dashboard penduduk seperti pada gambar 4 berikut.
</p>

![Gambar 4](/images/gbr4.png)

<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; Pada dashboard penduduk ini memuat visualisasi terkait karakteristik penduduk yang memiliki dampak terhadap kesejahteraan rakyat. Karakteristik tersebut antara lain variabel jumlah penduduk miskin, nilai IPM, dan Tingkat Pengangguran Terbuka (TPT) serta Tingkat Partisipasi Angkatan Kerja (TPAK). 
</br>&nbsp; &nbsp; &nbsp; &nbsp;Pertama, visualisasi persebaran penduduk miskin di Jawa Timur berdasarkan kabupaten/kota yang ditampilkan dengan menggunakan peta Provinsi Jawa Timur pata gambar 5 Sama halnya seperti peta yang menampilkan persebaran penduduk di Jawa Timur, pada peta kemiskinan ini, warna yang gelap menunjukkan bahwa jumlah penduduk miskin di kabupaten/kota tersebut lebih tinggi daripada wilayah yang memiliki warna lebih terang pada peta. Selain itu untuk grafik peta ini sendiri disertai filter tahun untuk memfilter data sendiri sebab ketersediaan data antara ketiga grafik pada halaman dashboard penduduk ini tidak sama. Oleh karena itu pada peta ini diberikan filter tahun untuk mengetahui persebaran penduduk miskin berdasarkan tahun yang dipilih oleh user.
</p>

![Gambar 5](/images/gbr5.png)

<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; 
Selanjutnya pada halaman dashboard penduduk ini juga terdapat visualisasi buble chart yang ditunjukkan pada gambar 6 berikut.
</p>

![Gambar 6](/images/gbr6.png)

<p align='justify'>
Penafsiran data yang disajikan dengan menggunakan buble chart tersebut dilihat dari ukuran dan warna lingkaran-lingkaran yang terbentuk. Lingkaran dengan ukuran lebih besar dari yang lain dan warna yang lebih gelap menunjukkan pada wilayah tersebut memiliki IPM yang tinggi dibandingkan wilayah lainnya. Misalnya, pada buble chart gambar 6 tersebut terlihat bahwa Kota Surabaya merupakan wilayah dengan nilai IPM paling tinggi di antara wilayah lain di Jawa Timur yang kemudian disusul oleh Kota Pasuruan dan Kota Mojokerto sebagai peringkat 3 besar IPM di Provinsi Jawa Timur pada tahun 2021. Jumlah buble atau lingkaran yang ditampilkan hanya 10 kabupaten/kota karena semakin banyak buble yang divisualisasikan akan terlihat semakin kurang efektif karena informasi yang ditampung terlalu berlebihan sehingga pembaca akan kehilangan fokus saat ingin menangkap informasi inti apa sebenarnya yang ingin disampaikan.
</p>

<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; Visualisasi selanjutnya yaitu diagram batang 2 kategori yang menampilkan TPT dan TPAK di setiap kabupaten/kota pada gambar 7 berikut.
</p>

![Gambar 7](/images/gbr7.png)

<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp;
Sama seperti visualisasi buble chart, wilayah Kabupaten/Kota yang divisualisasikan pada halaman dashboard ini hanya diambil 10 kabupaten/kota yang memiliki TPT dan TPAK tertinggi di Jawa Timur pada tahun yang dipilih pengguna di menu dropdown tahun. Tingkat Pengangguran Terbuka (TPT) merupakan presentase jumlah penganggur terhadap jumlah angkatan kerja yang ada di wilayah tersebut. Dengan adanya visualisasi TPT ini diharapkan mampu untuk menilai seberapa besar penyerapan tenaga kerja yang ada, semakin banyak tenaga kerja yang terserap maka seseorang akan lebih mudah mencapai tingkat kesejahteraan. Dalam hal ini berarti TPT yang rendah lah yang diharapkan karena mencerminkan tingkat penyerapan tenaga kerja yang baik. Sedangkan Tingkat Partisipasi Angkatan Kerja (TPAK) merupakan presentase banyak angkatan kerja terhadap banyaknya penduduk yang berumur sepuluh tahun ke atas. Antara TPT dan TPAK ini seperti memiliki hubungan yang tidak searah, artinya dengan rendahnya nilai TPT maka akan meningkatkan angka TPAK. Contohnya pada diagram gambar 7 tersebut Kabupaten Pacitan memiliki nilai TPT rendah dan TPAK nya tinggi diantara 9 kabupaten/kota yang lain. Hal ini menandakan bahwa di Kabupaten Pacitan tersebut penyerapan tenaga kerja nya sudah baik sehingga tingkat penganggurnya rendah. Dengan demikian harapannya di Kabupaten Pacitan ini tingkat kesejahteraan rakyat nya lebih baik karena dari segi penyerapan tenaga kerja nya tinggi. Namun ini hanya penglihatan dari satu dimensi, untuk mendapatkan interpretasi yang lebih meyakinkan maka perlu dilihat juga pada dimensi penyusun indikator kesejahteraan rakyat yang lain.
</br>&nbsp; &nbsp; &nbsp; &nbsp; Pada dashboard penduduk terdapat menu yang dapat mengalihkan menuju dashboard ekonomi yang ditunjukkan pada gambar 8. Dashboard ekonomi ini lebih fokus untuk memvisualisasikan data terkait perkembangan ekonomi Provinsi Jawa Timur dari tahun 2016 sampai 2021 yang dicirikan dengan variabel pengeluaran per kapita dan pertumbuhan ekonomi. 
</p>

![Gambar 8](/images/gbr8.png)

<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; 
Data pertumbuhan ekonomi digambarkan dengan visualisasi grafik garis karena data dengan tipe runtun waktu (time series) dari tahun 2016-2021. Visualisasi tersebut ditunjukkan pada gambar 9 berikut. 
</p>

![Gambar 9](/images/gbr9.png)

<p align='justify'>
Pada visualisasi pertumbuhan ekonomi ini terlihat bahwa dari tahun 2019 menuju 2020 terjadi penurunan tajam. Hal ini sejalan dengan terjadinya pandemo Covid-19 yang menyebabkan pembatasan bahkan sampai penghantian beberapa kegiatan ekonomi sehingga penurunan inilah sebagai dampaknya. Pada visualisasi ini nantinya pengguna dapat memilih ingin memvisualisasikan pertumbuhan ekonomi pada kabupaten/kota tertentu di Jawa Timur. Secara otomatis pada halaman dashboard ini ketika pengguna memilih untuk memvisualisasikan pertumbuhan ekonomi untuk kabupaten A misalnya, maka untuk grafik pengeluaran per kapita juga akan menampilkan visualisasi data untuk kabupaten yang dipilih yaitu kabupaten A.
</br>&nbsp; &nbsp; &nbsp; &nbsp; Selanjutnya, pada gambar 10 ditampilkan visualisasi perkembangan pengeluaran per kapita tahun 2016-2021 yang dapat dipilih sesuai kabupaten/kota tertentu yang ada di Provinsi Jawa Timur.
</p>

![Gambar 10](/images/gbr10.png)

<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; 
Pengeluaran per kapita ini mencerminkan biaya yang dikeluarkan untuk keperluan konsumsi seluruh anggota rumah tangga selama sebulan baik yang bersumber dari pembelian, pemberian, maupun hasil produksi sendiri kemudian dibagi dengan banyaknya anggota rumah tangga dalam keluarga tersebut. Contoh pada grafik tersebut Kabupaten Nganjuk mengalami puncak pengeluaran per kapita pada tahun 2019 kemudian menurun perlahan hingga menuju tahun 2021. Jika dikaitkan dengan penurunan ekonomi di gambar 9 yang terjadi pada tahun 2020 maka pengeluaran per kapita pun juga ikut menurun sebab sumber ekonominya sedang melemah. Dari visualisasi yang ada pada dashboard ekonomi ini diharapkan juga dapat secara sekilas atau secara satu dimensi saja untuk melihat kondisi kesejahterahteraan rakyat di kabupaten/kota tertentu di Jawa Timur.
</br>&nbsp; &nbsp; &nbsp; &nbsp; Halaman dashboard terakhir dari indikator kesejahreraan rakyat Provinsi Jawa Timur ini adalah dashboard Kesehatan yang ditampilkan pada gambar 11 berikut.
</p>

![Gambar 11](/images/gbr11.png)

<p align='justify'>
Pada dashboard kesehatan ini ditampilkan visualisasi donut chart yang menggambarkan jumlah desa menurut ketersediaan faskes dan presentase penduduk penerima layanan jaminan kesehatan berdasarkan jenis jaminan kesehatan yang diterimanya.
</br>&nbsp; &nbsp; &nbsp; &nbsp; Pada grafik visualisasi presentase penduduk penerima layanan jaminan kesehatan gambar 12 berikut dibuat dengan gradasi warna yang mencerminkan jenis jaminan kesehatan yang diterima.
</p>

![Gambar 12](/images/gbr12.png)

<p align='justify'>
Dari kiri ke kanan, bagian yang berwarna gelap merupakan cerminan presentase penduduk yang menerima jaminan kesehatan berupa jamkesda, berlanjut ke kanan merupakan presentase penduduk dengan jamkes BPJS Kesehatan PBI. Selanjutnya merupakan presentase penduduk penerima layanan jamkes berupa asuransi swasta lalu diikuti BPJS Kesehatan Non PBI dan asuransi perusahaan/kantor. Berdasarkan visualisasi presentase penduduk Jawa Timur yang menerima jaminan kesehatan pada tahun 2020 didominasi dengan jenis jaminan kesehatan berupa BPJS PBI sebab memiliki interval yang paling lebar. Visualisasi ini dapat diubah sesuai dengan data pada tahun yang ingin dilihat.
</br>&nbsp; &nbsp; &nbsp; &nbsp; Selanjutnya terdapat donut chart  yang menggambarkan jumlah desa menurut ketersediaan fasilitas kesehatan berdasarkan jenis fasilitas kesehatan. Visualisasi tersebut ditampilkan pada gambar 13 berikut.
</p>

![Gambar 13](/images/gbr13.png)

<p align='justify'>
Pada visualisasi donut chart tahun 2020 untuk Provinsi Jawa Timur ini apotek mendominasi keberadaan fasilitas kesehatan dengan jumlah desa terbanyak. Selanjutnya terdapat poliklinik, disusul dengan puskesmas, dan yang terakhir adalah rumah sakit. Dengan demikian dapat disimpulkan bahwa ketersediaan rumah sakit di Provinsi Jawa Timur ini masih tergolong sedikit jika dibandingkan dengan keberadaan puskesmas, poliklinik, maupun apotek ini. Dengan adanya visualisasi dimensi kesehatan ini diharapkan pembaca dapat menganalisis bagaimana tingkat kesejahteraan rakyat Jawa Timur secara sekilas berdasarkan kondisi ketersediaan fasilitas kesehatan dan kepemilikan jaminan kesehatan. Tentunya masyarakat yang memiliki jaminan kesehatan dan memiliki fasilitas kesehatan yang sangat mendukung di wilayahnya maka akan merasa lebih aman sehingga dapat meningkatkan kesejahteraan hidupnya.
</p>
<br></br>

<h2 align='center'>BAB 6 <br/>KESIMPULAN DAN SARAN</h2>

## A. Kesimpulan
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Berdasarkan dashboard visualisasi indikator kesejahteraan rakyat Provinsi Jawa Timur dan pembahasan yang telah dilakukan, maka dapat diambil kesimpulan bahwa variabel yang terdapat dalam dashboard visualisasi sudah cukup baik dalam memberikan gambaran kasar terkait indikator kesejahteraan rakyat Provinsi Jawa Timur. Harapan peneliti adalah dengan adanya dashboard visualisasi ini maka pembaca dapat melihat dan memperkirakan bagaimana letak tingkat kesejahteraan rakyat Provinsi Jawa Timur ini. Dimensi penduduk, dimensi ekonomi, dan dimensi kesehatan dapat dikatakan merupakan suatu kombinasi yang tepat dalam menjadi instrument penentu tingkat kesejahteraan rakyat.</p>  

## B. Saran
<p align='justify'>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;Adapun saran yang dapat penulis berikan untuk memberikan hasil visualisasi yang lebih baik antara lain :
<ol align = 'justify'>
  <li>Visualisasi bisa dikembangkan lebih lanjut untuk menampung data-data ter-update setiap dimensi nya supaya informasi yang ditangkap dan dicerna pengguna dari melihat hasil visualisasi indikator kesejahteraan rakyat Provinsi Jawa Timur tersebut bisa lebih sesuai dengan situasi terbaru.</li>
  <li>Karena dashboard visualisasi informasi ini terbatas hanya menyajikan indikator penyusun kesejahteraan rakyat Jawa Timur saja, maka untuk selanjutnya bisa dijadikan acuan dalam mengembangkan dashboard visualisasi informasi ini untuk daerah lain. Dengan demikian analisis kualitas kesejahteraan rakyat untuk tiap daerah di Indonesia dapat dilihat secara visual sekilas sebagai gambaran awal sebelum adanya kajian mendalam.</li>
  <li>Dalam penyusunan dashboard visualisasi indikator kesejahteraan Provinsi Jawa Timur ini masih berdasrkan tiga dimensi saja yaitu penduduk, ekonomi, dan kesehatan. Untuk pengembangan selanjutnya bisa dilakukan penelitian lebih lanjut terkait dimensi apa lagi yang berkaitan erat dalam memvisualisasikan kualitas kesejahteraan rakyat mengingat banyaknya dimensi indikator yang disajikan dalam publikasi statistik kesejahteraan rakyat Provinsi Jawa Timur 2021 namun dalam pembuatan dashboard visualisasi harus menampilkan informasi sesederhana mungkin yang mudah dipahami.</li>
</ol>
</p>  

<br></br>

<h2 align='center'> DAFTAR PUSTAKA </h2>

<p align='justify'>
</br>
[1]	Sari ME, Pratiwi DA. Faktor-Faktoryang Mempengaruhi Kesejahteraan Hidup Masyarakat Suku Laut Pulau Bertam Kota Batam. Jurnal Trias Politika. 2018 Oct 16;2(2):137-52.
</br> </br>
[2]	Shafii H, Miskam N. Pembentukan penunjuk dan indeks kualiti hidup bagi mengukur kesejahteraan hidup masyarakat di Pekan Parit Raja, Johor. Persidangan Kebangsaan Geografi dan Alam Sekitar, Universiti Pendidikan Sultan Idris. 2011.
</br></br>
[3]	Norizan Md. Nor. Petunjuk bandar sebagai alat penerapan konsep mapan dalam pengurusan dan pembangunan bandar di Malaysia. Prosiding National Seminar : Environmental Management Issues and Challenges in Malaysia. 2000.
</br></br>
[4]	Liu BC. Quality of life indicators in US metropolitan areas, 1970: a comprehensive assessment. Washington Environmental Research Center; 1975.
</br></br>
[5]	BPS Jatim (2020). Tabel Dinamis Luas Wilayah Menurut Kabupaten [Online]. Available : https://jatim.bps.go.id/indicator/153/81/1/luas-wilayah-menurut-kabupaten-kota.html.
</br></br>
[6]	Pramono MS, Sadewo FS. Analisis keberadaan bidan desa dan dukun bayi di Jawa Timur. Buletin Penelitian Sistem Kesehatan. 2012;15(3):21355.
</br></br>
[7]	Statistik BP. Statistik Kesejahteraan Rakyat Provinsi Jawa Timur. Jawa Timur: Badan Pusat Statistik. 2021
</br></br>
[8]	Rahardja U, Aini Q, Enay N. Optimalisasi Dashboard pada Sistem Penilaian Sebagai Media Informasi di Perguruan Tinggi. Sisfotenika. 2017 Aug 21;7(2):167-76.
</br></br>
[9]	Nurmalasari, D., Wahyuni, R. T., & Palapa, Y. (2015). Informational Dashboard untuk Monitoring Sistem Drainase secara Real-Time. Jurnal Nasional Teknik Elektro dan Teknologi Informasi (JNTETI), 4(3).
</br></br>
[10]	Hariyanti, E., & Purwanti, E. (2014). Perancangan Sistem Dashboard Untuk Monitoring Indikator Kinerja Universitas. SESINDO 2014.
</br>
[11]	Jayanti ED, Ani N. Pembangunan dashboard untuk visualisasi analisa keuangan. Format. 2017;6(2):57-66.
</br></br>
[12]	Stephen Few. 2006, “Information Dashboard Design : The Effective Visual Communication of Data”. O’Reilly Media.
</br></br>
[13]	Syaripul NA, Bachtiar AM. Visualisasi data interaktif data terbuka Pemerintah Provinsi DKI Jakarta: topik ekonomi dan keuangan daerah. Jurnal Sistem Informasi. 2016 Nov 1;12(2):82-9.
</br></br>
[14]	I. J. Asmara, E. Achelia, W. Maulana, R. Wijayanti and Y. Rianto, "Teknik Visualisasi Grafik Berbasis Web di Atas Platform Open Source," Seminar Nasional Aplikasi Teknologi Informasi 2009 (SNATI 2009), pp. 44-47,2009.
</br></br>
[15]	Hidayatullah KH. Analisis klaster untuk pengelompokan kabupaten/kota di provinsi Jawa Tengah berdasarkan indikator kesejahteraan rakyat. Jurnal Statistika Universitas Muhammadiyah Semarang. 2014;2(1).
</br>
</br>
</p>
