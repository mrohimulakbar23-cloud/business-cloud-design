# Minggu 06 – Desain High Availability dan Efisiensi Infrastruktur

## 1. Pendahuluan

Materi minggu keenam mata kuliah Business Cloud Design membahas desain High Availability (HA) dan efisiensi infrastruktur cloud.

Dalam penerapan cloud, organisasi tidak hanya membutuhkan infrastruktur yang mampu menjalankan aplikasi, tetapi juga layanan yang tetap dapat digunakan ketika terjadi gangguan pada komponen, jaringan, atau lokasi.

Di sisi lain, peningkatan ketersediaan membutuhkan kapasitas, biaya, dan kompleksitas tambahan. Oleh karena itu, desain infrastruktur harus menyeimbangkan ketahanan layanan dengan kebutuhan efisiensi bisnis.

## 2. Capaian Pembelajaran

Setelah mempelajari materi ini, mahasiswa diharapkan mampu:

1. Menjelaskan konsep availability, reliability, fault tolerance, RTO, dan RPO.
2. Mengidentifikasi Single Point of Failure pada arsitektur cloud.
3. Memilih pola redundansi, load balancing, failover, backup, dan disaster recovery.
4. Menganalisis trade-off antara performa, kapasitas, biaya, dan risiko.
5. Menyusun rancangan awal infrastruktur yang andal dan efisien untuk suatu kasus bisnis.

## 3. Konsep High Availability

### 3.1 Pengertian High Availability

High Availability (HA) adalah kemampuan suatu layanan untuk tetap dapat diakses dengan tingkat gangguan yang dapat diterima.

HA bukan berarti sistem tidak pernah mengalami kegagalan. Desain HA bertujuan mengurangi peluang kegagalan dan mempercepat proses pemulihan ketika gangguan terjadi.

Availability dipengaruhi oleh berbagai komponen, antara lain:

- Aplikasi.
- Komputasi.
- Penyimpanan.
- Jaringan.
- Identitas dan DNS.
- Fasilitas pusat data.
- Operasional dan pengelolaan layanan.

Dalam perspektif Sistem Informasi, keberhasilan HA sebaiknya diukur dari dampaknya terhadap proses bisnis dan pengguna, bukan hanya berdasarkan status server.

### 3.2 Availability, Reliability, dan Fault Tolerance

| Konsep | Pengertian |
|---|---|
| Availability | Persentase waktu layanan tersedia dan dapat digunakan. |
| Reliability | Kemampuan sistem menjalankan fungsi secara konsisten tanpa mengalami kegagalan selama periode tertentu. |
| Fault Tolerance | Kemampuan sistem tetap menjalankan fungsi meskipun sebagian komponen mengalami kegagalan. |
| High Availability | Pendekatan desain untuk mengurangi gangguan dan mempercepat pemulihan layanan. |

### 3.3 Metrik Availability

Terdapat dua metrik penting yang digunakan untuk memahami ketersediaan sistem:

**1. MTBF (Mean Time Between Failures)**

MTBF merupakan rata-rata waktu antara satu kegagalan dengan kegagalan berikutnya.

**2. MTTR (Mean Time To Repair/Recover)**

MTTR merupakan rata-rata waktu yang diperlukan untuk memperbaiki atau memulihkan sistem setelah terjadi kegagalan.

Rumus pendekatan availability:

**Availability ≈ MTBF ÷ (MTBF + MTTR)**

Contoh target availability tahunan berdasarkan 365 hari:

| Availability | Perkiraan Downtime |
|---|---|
| 99% | 3 hari 15 jam |
| 99,9% | 8 jam 46 menit |
| 99,99% | 52 menit 34 detik |
| 99,999% | 5 menit 15 detik |

Angka tersebut merupakan ilustrasi. Definisi SLA dan pengecualian downtime harus disepakati terlebih dahulu.

## 4. RTO dan RPO

RTO dan RPO merupakan dua sasaran penting dalam perencanaan pemulihan layanan.

### 4.1 RTO (Recovery Time Objective)

RTO adalah batas maksimum waktu layanan boleh tidak tersedia setelah terjadi gangguan.

Contoh: layanan akademik harus dapat dipulihkan dalam waktu maksimal dua jam.

### 4.2 RPO (Recovery Point Objective)

RPO adalah batas maksimum kehilangan data yang dapat diterima, diukur sebagai rentang waktu.

Contoh: kehilangan data maksimal 15 menit.

### 4.3 Perbedaan RTO dan RPO

| Aspek | RTO | RPO |
|---|---|---|
| Fokus | Waktu pemulihan layanan | Kehilangan data |
| Pertanyaan | Berapa lama layanan boleh berhenti? | Berapa banyak data boleh hilang? |
| Contoh | Pulih maksimal 2 jam | Kehilangan data maksimal 15 menit |

Target RTO dan RPO ditentukan berdasarkan dampak bisnis, kewajiban layanan, serta biaya pemulihan yang dapat diterima organisasi.

## 5. Failure Domain dan Single Point of Failure

### 5.1 Single Point of Failure (SPOF)

SPOF adalah satu komponen yang apabila mengalami kegagalan dapat menyebabkan layanan berhenti.

Contohnya:

- Satu server aplikasi.
- Satu database tanpa cadangan.
- Satu perangkat jaringan.
- Satu jalur koneksi internet.
- Satu sumber daya listrik.
- Satu pusat data tanpa lokasi pemulihan.

### 5.2 Failure Domain

Failure domain adalah batas area yang dapat terdampak oleh suatu kegagalan.

Contohnya meliputi:

- Host.
- Rack.
- Availability Zone.
- Region.
- Penyedia layanan.

Identifikasi failure domain diperlukan agar organisasi tidak menempatkan seluruh komponen penting pada satu area yang dapat mengalami kegagalan bersamaan.

## 6. Redundansi untuk Meningkatkan Availability

Redundansi merupakan penyediaan komponen atau jalur cadangan agar layanan tetap dapat berjalan ketika komponen utama mengalami gangguan.

Redundansi dapat diterapkan pada:

1. Komputasi.
2. Jaringan.
3. Daya listrik.
4. Storage.
5. Database.
6. DNS.
7. Jalur koneksi.

Contohnya, aplikasi menggunakan dua node server, yaitu App Node A dan App Node B, yang diakses melalui load balancer.

Jika salah satu node mengalami gangguan, node lainnya dapat tetap melayani permintaan pengguna.

Namun, dua komponen yang berbagi sumber daya atau konfigurasi identik masih dapat mengalami kegagalan secara bersamaan.

## 7. Load Balancing dan Health Check

### 7.1 Load Balancer

Load balancer merupakan komponen yang mendistribusikan permintaan pengguna ke beberapa instance aplikasi.

Tujuannya adalah membagi beban kerja dan menghindari ketergantungan pada satu instance.

### 7.2 Health Check

Health check digunakan untuk mendeteksi instance yang tidak sehat. Instance yang mengalami masalah dapat dikeluarkan sementara dari kumpulan server yang menerima permintaan.

### 7.3 Algoritma Load Balancing

Beberapa algoritma yang umum digunakan:

- **Round Robin:** permintaan dibagikan secara bergiliran ke setiap server.
- **Least Connections:** permintaan diarahkan ke server dengan jumlah koneksi aktif paling sedikit.
- **Weighted:** distribusi berdasarkan bobot atau kapasitas server.
- **Latency-Based:** memilih server berdasarkan waktu respons atau latensi.

Load balancer juga perlu dibuat redundant atau menggunakan layanan terkelola yang mendukung HA agar tidak menjadi SPOF baru.

## 8. Desain Aplikasi: Stateful dan Stateless

### 8.1 Stateful

Stateful merupakan kondisi ketika sesi pengguna atau file disimpan pada server aplikasi tertentu.

Risikonya adalah ketika server mengalami kegagalan, sesi atau data sementara yang tersimpan di server tersebut dapat ikut hilang.

Skalabilitas horizontal juga menjadi lebih sulit.

### 8.2 Stateless

Pada desain stateless, instance aplikasi tidak menyimpan state penting secara lokal.

Sesi pengguna dapat disimpan pada shared cache atau session store, sedangkan file dapat disimpan pada object storage.

Dengan pendekatan tersebut, instance aplikasi dapat ditambah, diganti, atau dipindahkan dengan lebih mudah.

**Prinsip utama: pisahkan compute dari state dan persistent data.**

## 9. Availability pada Database Management System

Ketersediaan database dapat dirancang melalui beberapa pendekatan.

### 9.1 Primary–Standby

Satu node berfungsi sebagai database utama untuk melayani operasi penulisan, sedangkan node cadangan mengambil alih ketika terjadi failover.

Hal yang perlu diperhatikan adalah replication lag dan risiko split-brain.

### 9.2 Synchronous Replication

Pada synchronous replication, konfirmasi penulisan menunggu proses replikasi sesuai mekanisme yang digunakan.

Keuntungannya adalah konsistensi data lebih kuat, tetapi dapat meningkatkan latency.

### 9.3 Asynchronous Replication

Pada asynchronous replication, proses penulisan tidak perlu menunggu seluruh replika selesai.

Keuntungannya adalah performa dapat lebih baik, tetapi terdapat risiko kehilangan transaksi terakhir apabila terjadi kegagalan.

### 9.4 Backup

Backup merupakan salinan data yang digunakan untuk pemulihan.

Backup bukan pengganti replikasi atau HA karena backup memiliki tujuan pemulihan data, bukan menjaga layanan tetap tersedia secara langsung.

### 9.5 Split-Brain

Split-brain adalah kondisi ketika beberapa bagian dalam suatu cluster terisolasi, tetapi masing-masing menganggap dirinya sebagai cluster utama yang aktif.

Akibatnya, beberapa node dapat mengambil keputusan sendiri, seperti menulis data secara bersamaan.

Pemilihan pendekatan database harus mempertimbangkan RTO, RPO, konsistensi transaksi, beban kerja, dan biaya.

## 10. Availability Zone dan Multi-Region

### 10.1 Multi-AZ

Multi-AZ merupakan desain yang menggunakan lebih dari satu Availability Zone dalam satu region.

Pendekatan ini membantu melindungi layanan dari kegagalan zona atau lokasi lokal.

### 10.2 Multi-Region

Multi-region merupakan desain yang menggunakan beberapa region berbeda.

Pendekatan ini membantu melindungi layanan dari gangguan regional, tetapi memiliki kompleksitas dan biaya lebih tinggi.

### 10.3 Perbandingan

| Aspek | Multi-AZ | Multi-Region |
|---|---|---|
| Tujuan | Melindungi dari kegagalan zona | Melindungi dari gangguan regional |
| Kompleksitas | Relatif lebih rendah | Lebih tinggi |
| Biaya | Lebih terkendali | Umumnya lebih mahal |
| Penggunaan | Baseline HA | Ketika dampak gangguan region membenarkan biaya tambahan |

Multi-AZ sering menjadi baseline HA, sedangkan multi-region dipilih berdasarkan kebutuhan bisnis dan dampak gangguan yang dapat diterima.

## 11. Failover: Otomatis atau Manual

Failover adalah proses pemindahan layanan ke komponen cadangan ketika komponen utama mengalami gangguan.

### 11.1 Automatic Failover

Kelebihan:
- Waktu pemulihan lebih cepat.
- Dapat mengurangi ketergantungan pada operator.

Risiko:
- False positive.
- Perpindahan berulang.
- Split-brain apabila fencing tidak diterapkan dengan tepat.

Automatic failover memerlukan health check dan quorum yang andal.

### 11.2 Manual atau Approved Failover

Kelebihan:
- Keputusan dapat mempertimbangkan konteks dan dampak bisnis.
- Sesuai untuk sistem kritis yang memiliki prosedur perubahan ketat.

Risiko:
- Proses pemulihan lebih lambat.
- Bergantung pada operator.

### 11.3 Tahapan Failover

Failover yang baik harus diuji melalui tahapan:

1. Deteksi gangguan.
2. Pengambilan keputusan.
3. Pengalihan trafik.
4. Verifikasi data.
5. Pemulihan kondisi normal.

Fencing adalah proses mengisolasi atau mematikan bagian sistem yang mengalami gangguan agar tidak terus melakukan operasi yang dapat membahayakan konsistensi layanan.

## 12. Disaster Recovery

Disaster Recovery (DR) merupakan strategi untuk memulihkan layanan dan data ketika terjadi gangguan besar atau bencana.

Terdapat empat pendekatan pemulihan:

| Strategi | Karakteristik | Biaya |
|---|---|---|
| Backup & Restore | Menggunakan backup untuk memulihkan layanan setelah gangguan. RTO cenderung lebih lama. | Relatif rendah |
| Pilot Light | Komponen inti dan data disiapkan, kapasitas penuh dinyalakan ketika terjadi bencana. | Menengah |
| Warm Standby | Lingkungan cadangan berjalan dengan kapasitas terbatas dan ditingkatkan ketika failover. | Lebih tinggi |
| Hot Standby | Lingkungan cadangan siap melayani dengan jeda pemulihan minimal. | Tertinggi |

Secara umum, semakin cepat target pemulihan, semakin besar biaya kapasitas cadangan dan sinkronisasi yang diperlukan.

## 13. Backup Bukan High Availability

Backup dan HA memiliki fungsi yang berbeda.

Replikasi dapat menyalin penghapusan, kerusakan data, atau ransomware ke replika. Karena itu, organisasi tetap membutuhkan backup yang terpisah.

Beberapa prinsip backup yang perlu diperhatikan:

1. Menentukan retensi backup.
2. Menggunakan enkripsi.
3. Membatasi kontrol akses.
4. Memisahkan backup dari domain kegagalan utama.
5. Melakukan pengujian restore secara berkala.
6. Mendokumentasikan pihak yang berwenang dan urutan pemulihan.

Salah satu panduan yang dikenal adalah prinsip 3-2-1:

- 3 salinan data.
- 2 jenis media berbeda.
- 1 salinan berada di lokasi berbeda atau offline.

Keberhasilan proses backup tidak otomatis membuktikan bahwa data dapat dipulihkan. Oleh karena itu, pengujian restore harus dilakukan secara berkala.

## 14. Observability dan Operasi Layanan

Observability merupakan kemampuan untuk memahami kondisi internal suatu sistem melalui data yang dihasilkan selama sistem beroperasi.

Terdapat tiga komponen utama:

| Komponen | Fungsi |
|---|---|
| Metrics | Mengukur availability, latency, error rate, throughput, CPU, memory, storage, dan replication lag. |
| Logs | Mencatat peristiwa untuk investigasi, audit, dan analisis insiden. |
| Traces | Melacak satu permintaan melalui beberapa service untuk menemukan bottleneck dan masalah dependency. |

### 14.1 SLO (Service Level Objective)

SLO merupakan target terukur yang menggambarkan tingkat layanan yang diharapkan.

### 14.2 Error Budget

Error budget merupakan batas maksimal kegagalan, downtime, atau ketidakandalan yang dapat diterima dalam periode tertentu tanpa melanggar target kualitas layanan.

Konsep ini berasal dari praktik Site Reliability Engineering (SRE) untuk menyeimbangkan kecepatan inovasi dengan stabilitas sistem.

## 15. Pengujian Ketahanan Infrastruktur

Pengujian diperlukan untuk memastikan desain HA dan DR benar-benar dapat bekerja ketika terjadi gangguan.

Beberapa jenis pengujian meliputi:

1. **Failover Test:** mematikan node atau instance secara terkontrol untuk mengukur waktu pemulihan.
2. **Restore Test:** memulihkan backup ke lingkungan terisolasi dan memvalidasi integritas data.
3. **Load Test:** menguji beban normal, beban puncak, dan lonjakan mendadak.
4. **Chaos Experiment:** memberikan gangguan secara terbatas dengan ruang lingkup dan prosedur rollback yang jelas.
5. **Game Day:** simulasi insiden lintas tim, termasuk komunikasi dan pengambilan keputusan bisnis.

## 16. Efisiensi Infrastruktur

Efisiensi berarti memenuhi kebutuhan layanan dengan total biaya dan risiko yang dapat diterima.

Terdapat tiga pendekatan utama:

### 16.1 Right-Sizing

Right-sizing merupakan penyesuaian kapasitas CPU, RAM, IOPS, dan storage berdasarkan pola penggunaan aktual.

Tujuannya menghindari kapasitas yang terlalu besar atau terlalu kecil.

### 16.2 Elasticity

Elasticity merupakan kemampuan menambah atau mengurangi kapasitas sesuai perubahan kebutuhan.

### 16.3 Utilization

Utilization menunjukkan tingkat penggunaan sumber daya infrastruktur.

Organisasi perlu menghindari resource idle dan melakukan konsolidasi workload tanpa mengorbankan target SLA.

Optimasi yang menurunkan biaya tetapi melanggar target RTO atau RPO bukanlah optimasi yang berhasil.

## 17. Scaling: Vertical, Horizontal, dan Autoscaling

### 17.1 Vertical Scaling

Vertical scaling dilakukan dengan menambah kapasitas CPU atau RAM pada satu instance.

Kelebihan:
- Mudah diterapkan.
- Tidak selalu membutuhkan perubahan besar pada aplikasi.

Kekurangan:
- Memiliki batas kapasitas maksimum.
- Dapat mempertahankan Single Point of Failure.

### 17.2 Horizontal Scaling

Horizontal scaling dilakukan dengan menambah jumlah instance atau server.

Kelebihan:
- Mendukung redundansi.
- Memungkinkan pembagian beban kerja.
- Kapasitas lebih fleksibel.

Kekurangan:
- Membutuhkan aplikasi yang mendukung distribusi beban.

### 17.3 Autoscaling

Autoscaling merupakan mekanisme penambahan atau pengurangan kapasitas berdasarkan metrik atau jadwal tertentu.

Autoscaling memerlukan:
- Threshold atau ambang batas.
- Cooldown.
- Kapasitas minimum dan maksimum.
- Proteksi scale-in.

Contoh aturan autoscaling dalam materi:

- Scale out ketika CPU lebih dari 70% selama 5 menit.
- Scale in ketika CPU kurang dari 35% selama 15 menit.

## 18. Efisiensi Storage, Jaringan, dan Data

Selain compute, efisiensi juga dapat dilakukan pada storage, jaringan, dan pengelolaan data.

Beberapa pendekatan yang digunakan:

1. **Storage Tiering:** menempatkan data pada kelas layanan storage yang sesuai dengan kebutuhan.
2. **Lifecycle Policy:** memindahkan atau menghapus objek berdasarkan masa retensi dan kebutuhan regulasi.
3. **Compression:** mengurangi ukuran data, tetapi dapat menambah penggunaan CPU.
4. **Deduplication:** mengurangi kapasitas dengan menghilangkan penyimpanan data duplikat.
5. **Cache:** mengurangi beban backend, tetapi memerlukan strategi invalidasi dan konsistensi.
6. **CDN dan Edge Caching:** mengurangi latency serta trafik menuju origin untuk konten yang sesuai.

## 19. Membaca Biaya Cloud: TCO dan Unit Economics

Efisiensi infrastruktur harus dilihat dari keseluruhan biaya layanan.

Komponen biaya meliputi:

- Compute.
- Storage.
- Database.
- Network egress.
- Load balancer.
- Backup dan Disaster Recovery.
- Observability.
- Lisensi.
- Dukungan.
- Tenaga operasional.
- Biaya migrasi dan biaya keluar.

TCO (Total Cost of Ownership) merupakan biaya langsung dan tidak langsung sepanjang siklus hidup layanan.

Biaya juga dapat diukur berdasarkan hasil layanan, misalnya:

| Metrik | Pengukuran |
|---|---|
| Biaya per transaksi | Total biaya dibandingkan jumlah transaksi. |
| Biaya per pengguna aktif | Total biaya dibandingkan pengguna aktif. |
| Biaya per GB diproses | Total biaya dibandingkan volume data yang diproses. |
| Biaya per jam layanan tersedia | Total biaya dibandingkan jam layanan yang tersedia. |

Perbandingan biaya perlu mencakup kondisi normal dan kondisi failover.

## 20. Trade-off Desain: Availability, Cost, dan Complexity

Dalam merancang infrastruktur, terdapat tiga aspek yang saling berkaitan:

1. **Availability:** tingkat ketersediaan layanan yang ingin dicapai.
2. **Cost:** biaya yang diperlukan untuk membangun dan mengoperasikan layanan.
3. **Complexity:** kompleksitas desain, pengelolaan, dan pemeliharaan infrastruktur.

Tidak ada satu desain yang paling benar untuk semua sistem.

Desain harus mengikuti target bisnis dan tingkat risiko yang dapat diterima organisasi. Infrastruktur yang terlalu kompleks dapat meningkatkan biaya operasional, sedangkan desain yang terlalu sederhana dapat menyebabkan gangguan layanan.

## 21. Studi Kasus: Portal Layanan Akademik

Materi memberikan studi kasus universitas yang menggunakan portal untuk layanan:

- Kartu Rencana Studi (KRS).
- Pembayaran.
- Nilai akademik.
- Pengunduhan dokumen.

### 21.1 Kondisi Saat Ini

Infrastruktur yang digunakan memiliki kondisi:

- Satu VM aplikasi.
- Satu database.
- Backup harian.
- Lonjakan akses ketika periode KRS.

### 21.2 Target Bisnis

Universitas menetapkan target:

| Aspek | Target |
|---|---|
| Availability | 99,9% |
| RTO | 2 jam |
| RPO | 15 menit |
| Transaksi pembayaran | Tidak boleh kehilangan transaksi yang tidak dapat diterima |

### 21.3 Kendala

- Tim TI berukuran kecil.
- Anggaran operasional terbatas.
- Terdapat lonjakan penggunaan pada periode tertentu.
- Transaksi pembayaran harus terlindungi.

### 21.4 Identifikasi Risiko

Dari kondisi awal, terdapat beberapa kemungkinan Single Point of Failure:

1. Satu VM aplikasi yang menjadi satu-satunya tempat aplikasi berjalan.
2. Satu database tanpa node cadangan.
3. Satu jalur jaringan yang dapat menghentikan akses.
4. Backup harian yang belum tentu memenuhi target RPO 15 menit.
5. Ketergantungan pada satu lokasi atau satu sumber daya infrastruktur.

### 21.5 Arah Solusi

Salah satu kemungkinan rancangan solusi adalah:

- Menggunakan dua node aplikasi, yaitu App Node A dan App Node B.
- Menggunakan DNS, WAF, dan load balancer.
- Menggunakan database primary dengan replica atau backup.
- Mempertimbangkan multi-AZ jika tersedia.
- Menguji database failover.
- Menggunakan backup terisolasi.
- Menyimpan dokumen pada object storage.
- Menggunakan autoscaling yang terukur.
- Menerapkan monitoring berdasarkan SLO.
- Menyediakan prosedur penanganan insiden.

### 21.6 Strategi Scaling

Pada periode normal, kapasitas dapat disesuaikan dengan kebutuhan penggunaan.

Pada periode KRS, kapasitas aplikasi dapat ditingkatkan berdasarkan metrik penggunaan atau jadwal yang telah diperkirakan.

### 21.7 Validasi

Rancangan harus diuji untuk memastikan:

- Availability dapat memenuhi target 99,9%.
- Layanan dapat dipulihkan maksimal dua jam.
- Kehilangan data tidak melampaui target 15 menit.
- Transaksi pembayaran tetap terlindungi.
- Kapasitas mampu menghadapi lonjakan akses.

Desain tidak cukup hanya terlihat redundant di atas diagram. Kemampuan pemulihan harus dibuktikan melalui simulasi dan pengujian.

## 22. Kesimpulan

Desain High Availability dan efisiensi infrastruktur merupakan dua aspek penting dalam Business Cloud Design.

High Availability membantu menjaga layanan tetap dapat diakses ketika terjadi gangguan melalui redundansi, load balancing, failover, backup, dan disaster recovery. Sementara itu, efisiensi infrastruktur dilakukan melalui right-sizing, elasticity, utilization, autoscaling, serta pengelolaan storage dan jaringan.

Keputusan desain harus mempertimbangkan availability, biaya, dan kompleksitas secara bersamaan. Infrastruktur yang baik bukanlah infrastruktur yang paling mahal atau paling kompleks, melainkan infrastruktur yang sesuai dengan kebutuhan dan tujuan bisnis.

## 23. Penggunaan AI

Dalam penyusunan rangkuman materi minggu keenam ini, saya menggunakan bantuan AI (ChatGPT) untuk membantu memahami, menyusun, dan merangkum materi dari file PDF perkuliahan.

### Prompt yang Digunakan

> Saya sedang mengerjakan tugas rangkuman mingguan mata kuliah Business Cloud Design. Bantu saya membuat rangkuman materi Minggu 06 berdasarkan file PDF yang saya berikan dengan judul Desain High Availability dan Efisiensi Infrastruktur. Susun rangkuman dalam format Markdown untuk README.md GitHub. Bahas capaian pembelajaran, High Availability, availability dan downtime, MTBF, MTTR, RTO, RPO, Single Point of Failure, failure domain, redundansi, load balancing, stateful dan stateless, availability database, Multi-AZ, multi-region, failover, disaster recovery, backup, observability, SLO, error budget, pengujian ketahanan, efisiensi infrastruktur, scaling, TCO, trade-off desain, dan studi kasus portal layanan akademik. Gunakan bahasa Indonesia yang jelas dan mudah dipahami. Pertahankan istilah, angka, target, dan contoh sesuai PDF dosen. Jangan menambahkan angka atau asumsi yang tidak terdapat dalam materi. Sertakan tabel jika membantu pemahaman.

### Bagian yang Dibantu AI

- Menyusun struktur rangkuman agar lebih sistematis.
- Menjelaskan kembali istilah teknis menggunakan bahasa yang lebih mudah dipahami.
- Menyusun tabel perbandingan dan merapikan poin-poin materi.
- Menjelaskan konsep HA, DR, RTO, RPO, dan efisiensi infrastruktur.
- Menyusun kesimpulan dan dokumentasi penggunaan AI.

### Bagian yang Diperiksa dan Disesuaikan

- Memeriksa kesesuaian isi rangkuman dengan PDF perkuliahan.
- Memeriksa kembali angka target availability, RTO, dan RPO.
- Menyesuaikan istilah teknis agar tetap sesuai dengan materi dosen.
- Membaca kembali hasil rangkuman sebelum dipublikasikan ke GitHub.

## 24. Sumber Materi

- File perkuliahan: **06--business-cloud-design.pdf**
- Judul materi: Desain High Availability dan Efisiensi Infrastruktur.
- Mata Kuliah: Business Cloud Design.
- Program Studi: Sistem Informasi.
- Universitas Teknologi Digital Indonesia (UTDI).
