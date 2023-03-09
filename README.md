# Revenue Management: Hotel Booking Analysis & Cancellation Prediction
**by Beami MW**

Berdasarkan data yang dimiliki perusahaan, tingkat persentase pembatalan pemesanan kamar hotel di tahun 2017 adalah sebesar 38.7% yang mengalami peningkatan pembatalan pemesanan kamar hotel dibandingkan tahun 2016 yang hanya sebesar 35.9% dan tahun 2015 sebesar 37%. Tingkat pembatalan pemesanan kamar hotel dapat berdampak pada berkurang/hilangnya revenue pada suatu bisnis perhotelan. Menurut Asosiasi Hotel Portugis, kerugian akibat pembatalan pemesanan kamar hotel bisa mencapai sekitar 3,6 miliar euro, yang diperkirakan bahwa hotel-hotel Portugis bisa mengalami penurunan pendapatan hingga 80% sehubungan dengan angka-angka dari tahun 2019 [hotel revenue](https://www.theportugalnews.com/news/2020-11-11/hotel-revenue-could-drop-by-80-percent/56644). 

Dalam menyiasati revenue agar tidak berkurang/hilang, maka dilakukan upaya melalui revenue management. Revenue management adalah landasan menjalankan bisnis yang sukses dan menguntungkan, terutama di industri perhotelan. Revenue management melibatkan analisis data historikal untuk membantu memprediksi perilaku customer di industri perhotelan serta pendekatan dengan bantuan model prediksi 'cancel'. Kunci utama untuk strategi revenue management yang efektif adalah memiliki cara untuk membuat perkiraan yang tepat tentang kemungkinan kebiasaan customer yang membatalkan pemesanan kamar hotel, ini dapat terdiri dari pemesanan masa lalu dan informasi data customer lainnya. Dengan memprediksi perilaku customer yang akan membatalkan pemesanan kamar hotel diharapkan nantinya dapat digunakan terbatas untuk kalangan staff management hotel yang berupa website/aplikasi mobile, untuk membedakan reservasi yang diprediksi akan dibatalkan sehingga nantinya reservasi yang diprediksi akan dibatalkan tersebut dapat ditawarkan kembali kepada customer lain yang lebih potensial agar kamar tidak menjadi kosong/sia-sia dan mendapatkan keuntungan revenue dari F&B service melalui customer potensial yang menginap. Kemudian dengan adanya analisis historikal data berupa pemesanan kamar hotel yang dibatalkan maupun tidak, dapat membantu staff management hotel dalam menetapkan penyusunan anggaran yang lebih terkontrol di masa mendatang untuk Departemen Food and Beverage (F&B), Departemen Housekeeping, dan Departemen Personalia. Tujuan akhir dari revenue & Budget management adalah untuk memiliki kamar yang tepat untuk customer yang tepat pada waktu dan tempat yang tepat. Ketika ini terjadi, revenue hotel akan cenderung maksimal & budget planning dapat terkontrol, dan pada akhirnya berpengaruh pada profit hotel [budget planning](https://www.studocu.com/id/document/universitas-nusa-mandiri/science/41258620-simple/30127587).

# Tujuan
1.  memprediksi kemungkinan reservasi akan dibatalkan dari platform dengan bantuan model machine learning klasifikasi, dengan target nilai metric evaluation sebesar 0.70, sehingga perusahaan dapat memfokuskan strategi untuk kamar yang akan dibatalkan agar dialihkan kepada customer lain yang lebih berpotensi, sehingga kamar tidak menjadi kosong/sia-sia dan hotel akan mendapatkan revenue dari F&B service dari customer yang menginap.
2. serta untuk mengetahui faktor/variabel pemesanan kamar hotel yang dibatalkan dan tidak dari platform mereka, sehingga staff management hotel dapat membuat perencanaan anggaran yang lebih terkontrol untuk departemen personalia, departemen housekeeping dan departemen F&B.

# Dataset
- Data historikal customer yang melakukan pemesanan kamar hotel dengan status "cancel/tidak cancel" yang terjadi di tanggal 1 Juli 2015 sampai dengan 31 Agustus 2017
- Terdiri dari 32 kolom dan 119390 baris
- Target menjelaskan apakah reservasi cancel atau tidak

# Hotel Booking Analysis
Untuk membantu staff management hotel dalam menentukan perencanaan anggaran yang lebih terkontrol untuk departemen personalia, departemen housekeeping dan departemen F&B. Maka saya akan membuat pertanyaan serta mencoba menjawab pertanyaan-pertanyaan berikut:
1. Berapa total penjualan kamar berdasarkan bulan di tahun 2015-2017?
2. Berapa banyak total tamu yang menginap berdasarkan bulan di tahun 2015-2017?
3. Berapa total penjualan tipe meal berdasarkan bulan di tahun 2015-2017?

# **1. Berapa total penjualan kamar berdasarkan bulan di tahun 2015-2017?**
# Insight
Berdasarkan trend harian reservasi yang tidak cancel dan yang di cancel, dapat terlihat bahwa pada pola antara yang cancel dan tidak cancel memiliki pola yang hampir mirip. Apabila pada hari yang sama, yang tidak cancel meningkat maka yang cancel juga  meningkat. Namun tetap dari hari ke hari, jumlah yang cancel lebih sedikit dibandingkan yang tidak cancel.
### Penjualan City hotel:
- pada tahun 2015 antara bulan Juli-Desember, penjualan meningkat di bulan Agustus,September, Oktober dibanding bulan lainnya dan penjualan paling sedikit ada di bulan Juli. 
- Pada tahun 2016 antara bulan januari-desember, penjualan meningkat di bulan Juli, Agustus, September dan penjualan paling sedikit ada di bulan Januari dan Desember. 
- Pada tahun 2017 antara bulan januari-Agustus, penjualan meningkat di bulan Mei dan paling sedikit di bulan januari.
### Penjualan Resort hotel:
- pada tahun 2015 antara bulan Juli-Desember, penjualan meningkat di bulan Juli, Agustus, September, Oktober dibanding bulan lainnya dan penjualan paling sedikit ada di bulan November dan Desember. 
- Pada tahun 2016 antara bulan januari-desember, penjualan meningkat di bulan Oktober dan penjualan paling sedikit ada di bulan Januari. 
- Pada tahun 2017 antara bulan januari-Agustus, penjualan meningkat di bulan Mei dan paling sedikit di bulan januari dan Februari.

Dapat diambil kesimpulan bahwa penjualan kamar di city hotel dan resort hotel paling banyak ada di antara bulan Mei-Oktober.

# **2. Berapa banyak total tamu yang menginap berdasarkan bulan di tahun 2015-2017?**
# Insight
- Total tamu paling banyak ada di bulan Juli-Agustus.
- Tiap bulan, tamu hotel paling banyak berasal dari benua Eropa dan paling banyak ada di bulan Juli-Agustus dan paling sedikit dari benua Oceania

# **3. Berapa total penjualan tipe meal berdasarkan bulan di tahun 2015-2017?**
# Insight
- Total penjualan tipe meal paling banyak adalah tipe meal BB (sarapan saja) dengan total paling banyak adalah di bulan Agustus, July

# Data Preprocessing
- Missing Values Handling
- Duplicate Handling
- Outlier Handling
- feature Selection using Correlation
- Target Imbalance Handling
- Encoding
- Scaling

# Metric
- TN = diprediksi tidak cancel dan aktualnya memang tidak cancel 
- FP = diprediksi cancel padahal aktualnya tidak cancel
- FN = diprediksi tidak cancel padahal aktualnya cancel
- TP = diprediksi cancel dan aktualnya memang cancel

Type 1 error : False Positive  
Konsekuensi: mismanagement hotel service karena diprediksi cancel padahal aktualnya tidak cancel

Skenario:
Jika model memprediksi pemesanan kamar hotel dibatalkan dan sudah menjual kamar ke customer lain, tetapi kemudian customer asli tidak membatalkan dan datang ke hotel di tanggal mereka check in, lalu tidak ada kamar yang tersedia pada saat itu untuk customer asli atau ada kamar yang tersedia tetapi dengan kelas lebih rendah, maka reputasi hotel akan rusak. Namun jika kamar yang tersedia adalah kelas yang lebih tinggi dengan harga yang lebih mahal, maka hotel akan mengalami kerugian revenue dari menjual kamar yang lebih mahal itu dengan harga yang lebih murah.


Type 2 error : False Negative  
Konsekuensi: Revenue hotel akan hilang karena diprediksi tidak cancel padahal aktualnya cancel

Skenario:
Jika model memprediksi pemesanan kamar hotel tidak dibatalkan, tetapi customer tidak datang, maka hotel akan mengalami kerugian berupa revenue yang hilang karena hotel tidak menjual kamar kepada customer potensial lainnya dan hotel tidak akan mendapatkan revenue penjualan dari hotel service berupa F&B dan revenue dari hotel service lainnya.

Berdasarkan konsekuensi diatas, saya merasa kerugian dari konsekuensi FN lebih besar daripada kerugian dari konsekuensi FP. saya perlu meminimalisir bagian False Negative. Maka metric yang akan saya gunakan adalah recall.

# Modeling
Setelah melakukan beberapa percobaan dengan mencoba 6 algoritma untuk menemukan model terbaik. Saya menemukan Light GBM adalah model yang terbaik dengan skor:
- Recall training data : 0.866
- Recall test data : 0.851
- Recall setelah hyperparameter tuning : 0.996

# Recommendation for Hotel
 1. Untuk City hotel maupun Resort hotel, Paling banyak kamar terjual yaitu antara bulan Mei-Oktober. Di Eropa pada bulan Mei-Juli adalah musim panas dan bulan Agustus-Oktober adalah musim gugur. Pada kedua musim itu adalah waktu dengan suhu yang cocok untuk keluar rumah dan pergi berlibur menginap di hotel dibandingkan dengan musim dingin dan musim semi yang suhunya kurang mendukung. Musim semi sendiri suhunya masih terlalu dingin yaitu antara 6-13°C. Staff management hotel dapat menentukan perencanaan anggaran untuk departemen personalia dalam merekrut karyawan magang untuk bagian housekeeping dan front office di bulan Mei-Oktober selama 6 bulan. Budget pengeluaran dalam bentuk gaji untuk karyawan magang sendiri lebih sedikit dibandingkan merekrut karyawan tetap. Sehingga hal tersebut bisa meningkatkan pendapatan hotel.
2. Paling banyak kamar terjual yaitu di bulan Mei-Oktober, Staff management hotel dapat berkoordinasi dengan staff departemen housekeeping untuk pengecekan alat dan bahan untuk kebersihan kamar hotel maupun area hotel. Apabila ada alat yang rusak, staff management hotel dapat menetapkan pembuatan anggaran operasional dan pengadaan barang hotel untuk departemen housekeeping pada bulan-bulan ramai pengunjung tersebut. Namun apabila tidak ada, penetapan pembuatan anggaran operasional dan pengadaan barang hotel untuk departemen housekeeping dapat diturunkan. Namun untuk bahan-bahan pembersih tentu saja staff management hotel harus menentukan budget lebih banyak untuk departemen housekeeping di bulan Mei-Oktober. Staff management hotel dapat mengontrol pembelian yang mana pelaksanaannya dilakukan oleh purchasing staff sehingga akan terhindar dari pengeluaran yang berlebihan, dengan kontrol yang baik akan terjadinya keseimbangan antara pembelian dengan pemasukan sehingga target pendapatan tercapai. 
3. Penjualan tipe meal yang terbanyak dari bulan ke bulan selalu tipe meal BB (sarapan saja). Asal tamu yang menginap paling banyak adalah dari benua Eropa. Informasi mengenai asal tamu hotel dapat membantu departemen F&B service untuk menyiapkan jenis masakan yang dapat disiapkan agar dapat menyesuaikan dengan lidah tamu dan dapat membuat anggaran pembelian bahan baku makanan untuk masakan yang cocok dengan lidah tamu. Maka staff management hotel dapat membuat penentuan anggaran pembelian bahan baku makanan untuk masakan yang cocok dengan lidah orang Eropa karena tamu hotel kebanyakan berasal dari benua Eropa. Serta Budgetnya bisa dikontrol agar tidak berlebihan karena tamu kebanyakan memesan tipe meal BB (sarapan saja). Penentuan budget untuk F&B service bisa ditingkatkan di bulan Juli-Agustus karena lebih ramai pengunjung di bulan-bulan tersebut serta dapat disesuaikan dengan tipe makanan untuk musim panas dan musim gugur.
4. Batasi tenggat waktu pembatalan maksimal 5 hari dari tanggal kedatangan dan berikan notifikasi melalui email/platform/aplikasi untuk mengonfirmasi kedatangan/tidak.
5. Buat kebijakan uang deposit tidak kembali apabila tidak mengonfirmasi pembatalan H-15 kedatangan dan bisa hapus sistem no deposit
6. Jika reservasi diperkirakan akan dibatalkan dan kamar telah terjual ke customer lain, namun customer asli tetap datang. Maka bisa geser jam check in untuk customer asli atau geser jam check out untuk tamu yang akan check out. Sehingga akan kebagian kamar.
7. Jika customer reservasi kamar kelas lebih tinggi namun yang tersedia kamar kelas yang lebih rendah maka coba tawarkan cashback sebesar selisih harga kamar yang dipesan/ voucher sebesar selisih harga kamar
8. Bulan ramai tamu menginap adalah Juli-Agustus, pada bulan tersebut bisa membuat event menarik di hotel atau menyewakan area hotel untuk bazar misalnya. Hal tersebut juga bisa meningkatkan revenue hotel.

# Recommendation for Model
1. menggunakan algoritma boosting lainnya yang belum dicoba.
2. Menganalisa data-data yang model yang masih salah tebak (False Negative dan terutama False Positive) untuk mengetahui alasan dan karakteristiknya.
3. Menambahkan jumlah data terutama pada kategori cancel agar memperoleh informasi yang lebih akurat.
4. Menerapkan threshold

# Conclusion
Berdasarkan hasil classification report dari model, saya dapat menyimpulkan bahwa bila seandainya nanti menggunakan model ini untuk memfilter reservasi yang akan nanti coba dialihkan kepada customer lain untuk meningkatkan pendapatan, maka model ini dapat mengurangi 31% reservasi yang tidak cancel untuk tidak dialihkan kepada customer lain, dan model ini dapat mendapatkan 100% reservasi yang akan cancel dari seluruh reservasi yang cancel. (semua ini berdasarkan recallnya)

Model ini memiliki ketepatan prediksi reservasi yang akan cancel sebesar 35% (precisionnya), jadi setiap model ini memprediksi bahwa reservasi itu cancel, maka kemungkinan tebakannya benar itu sebesar 35% kurang lebih. Maka masih akan ada reservasi yang sebenarnya tidak akan cancel tetapi di prediksi sebagai reservasi yang cancel sekitar 69% dari keseluruhan reservasi yang tidak cancel (berdasarkan recall).

Statistik Cancel menggunakan y_test (20%):

0: 3.809
1: 13.098
Total data: 16.907
Tanpa model:

Apabila pada periode tertentu ada 16.907 customer yang melakukan reservasi dengan tarif rata-rata harian 100 euro. Dan ada 4.568 akan cancel dan 12.339 tidak akan cancel. Maka tanpa model, kita tidak akan tahu mana yang akan cancel dan yang tidak cancel. Maka perhitungannya:

Total pendapatan reservasi = 16.907 x 100 euro = 1.690.700 euro (apabila semua reservasi terjadi)
Total kerugian = 4.568 customer x 100 euro = 456.800 euro (karena tidak dialihkan kepada customer lain)
Total pendapatan ADR = 1.690.700 - 456.800 = 1.233.900 euro (setelah dikurangi kerugian)
Dengan model:

TP = 4.551 reservasi akan dialihkan kepada customer lain maka 4.551 x 100 euro = 455.100 euro (pendapatan)
TN = 3.792 reservasi terjadi maka 3.792 x 100 euro = 379.200 euro (pendapatan)
FP = 8.547 reservasi terjadi namun mismanagement service karena reservasi dialihkan kepada customer baru dan customer asli bisa dapat kamar lebih mahal atau lebih murah. Namun hotel masih untung. Maka 8.547 x 100 euro = 854.700 euro (pendapatan)
FN = 17 reservasi tidak terjadi karena cancel dan tidak dialihkan kepada customer lain, maka 17 x 100 euro = 17.100 euro (kerugian)
Total pendapatan ADR = 1.689.000 euro
Dengan model, kita bisa meningkatkan pendapatan sebesar 455.100 euro

% Kenaikan = 455.100 / 1.233.900 x 100 = 37%
