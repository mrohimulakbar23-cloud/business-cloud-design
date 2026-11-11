# Minggu 07 – Skalabilitas Berbasis Kontainer dan Virtualisasi

## 1. Pendahuluan

Materi minggu ketujuh mata kuliah Business Cloud Design membahas skalabilitas infrastruktur cloud dengan memanfaatkan teknologi virtualisasi dan kontainer.

Dalam lingkungan cloud, kebutuhan sumber daya dapat berubah sesuai jumlah pengguna, transaksi, dan aktivitas aplikasi. Oleh karena itu, organisasi membutuhkan infrastruktur yang mampu menyesuaikan kapasitas dengan kebutuhan beban kerja.

Virtual Machine (VM) dan kontainer merupakan dua teknologi yang dapat digunakan untuk menyediakan lingkungan aplikasi secara terisolasi. Keduanya memiliki karakteristik, keunggulan, dan kebutuhan sumber daya yang berbeda.

Materi ini juga membahas Kubernetes sebagai platform orkestrasi kontainer serta FinOps untuk membantu mengoptimalkan penggunaan sumber daya dan biaya infrastruktur.

## 2. Agenda Pembelajaran

Materi minggu ketujuh terdiri dari empat pembahasan utama:

1. **Landasan Skalabilitas:** vertical scaling, horizontal scaling, dan dampaknya terhadap efisiensi bisnis.
2. **VM vs Kontainer:** perbandingan hypervisor, container engine, dan isolasi sistem.
3. **Orkestrasi Kubernetes:** auto-scaling, load balancing, dan self-healing cluster.
4. **Analisis FinOps:** perhitungan TCO, optimasi biaya, dan strategi multi-cloud.

## 3. Konsep Skalabilitas Cloud

Skalabilitas merupakan kemampuan sistem untuk menyesuaikan kapasitas sumber daya ketika kebutuhan beban kerja berubah.

Dalam cloud computing, terdapat dua pendekatan utama untuk meningkatkan kapasitas sistem.

### 3.1 Vertical Scaling (Scale-Up)

Vertical scaling merupakan metode meningkatkan kapasitas satu server dengan menambahkan atau meningkatkan spesifikasi perangkat keras.

Contohnya:
- Menambah kapasitas CPU.
- Menambah RAM.
- Meningkatkan kapasitas disk.

**Karakteristik:**
- Peningkatan kapasitas dilakukan pada satu server.
- Bergantung pada batas maksimum spesifikasi perangkat keras.
- Perubahan spesifikasi dapat membutuhkan restart atau downtime.
- Tidak otomatis menghilangkan ketergantungan pada satu server.

### 3.2 Horizontal Scaling (Scale-Out)

Horizontal scaling merupakan metode meningkatkan kapasitas dengan menambahkan node atau replika baru ke dalam sistem.

Contohnya:
- Menambah instance aplikasi.
- Menambah jumlah server.
- Menambah replika kontainer.

**Karakteristik:**
- Kapasitas ditingkatkan dengan menambah jumlah instance.
- Mendukung distribusi beban kerja.
- Dapat meningkatkan High Availability.
- Cocok untuk aplikasi yang membutuhkan elastisitas berdasarkan perubahan traffic.

### 3.3 Perbandingan Vertical dan Horizontal Scaling

| Aspek | Vertical Scaling | Horizontal Scaling |
|---|---|---|
| Metode | Menambah kapasitas satu server | Menambah jumlah node |
| Perubahan | CPU, RAM, dan disk | Instance atau replika |
| Batasan | Spesifikasi maksimum hardware | Bergantung pada kapasitas platform dan arsitektur |
| Downtime | Perubahan dapat membutuhkan restart | Dapat dilakukan dengan menambah node tanpa menghentikan seluruh layanan jika didesain dengan benar |
| Skalabilitas | Terbatas pada kapasitas satu server | Lebih fleksibel untuk beban terdistribusi |

## 4. Arsitektur Virtual Machine (VM)

### 4.1 Pengertian Virtual Machine

Virtual Machine merupakan teknologi virtualisasi yang memungkinkan satu perangkat keras fisik menjalankan beberapa mesin virtual secara independen melalui lapisan yang disebut Hypervisor.

Setiap VM dapat memiliki sistem operasi atau Guest OS sendiri beserta aplikasi yang dijalankan di dalamnya.

Dengan virtualisasi, sumber daya fisik seperti CPU, RAM, dan storage dapat dibagi untuk beberapa lingkungan komputasi.

### 4.2 Hypervisor

Hypervisor merupakan lapisan perangkat lunak yang mengelola dan menyediakan sumber daya perangkat keras untuk mesin virtual.

Terdapat dua jenis hypervisor:

**1. Hypervisor Type 1 (Bare-Metal)**

Hypervisor berjalan langsung di atas perangkat keras fisik tanpa membutuhkan sistem operasi host sebagai lapisan utama.

Contoh:
- VMware ESXi.
- KVM.

**2. Hypervisor Type 2 (Hosted)**

Hypervisor berjalan di atas sistem operasi host.

Contoh:
- VirtualBox.
- VMware Workstation.

### 4.3 Kelebihan Virtual Machine

- Menyediakan isolasi lingkungan virtual.
- Setiap VM dapat menjalankan Guest OS sendiri.
- Mendukung berbagai sistem operasi dalam satu perangkat fisik.
- Cocok untuk workload yang membutuhkan isolasi tingkat mesin virtual.
- Dapat digunakan sebagai fondasi infrastruktur cloud.

## 5. PVM dan HVM

Dalam materi juga dibahas dua pendekatan virtualisasi, yaitu PVM dan HVM.

### 5.1 PVM (Paravirtualization)

Paravirtualization merupakan pendekatan virtualisasi yang melibatkan kesadaran sistem operasi Guest terhadap lingkungan virtualisasi dan penggunaan mekanisme khusus untuk berkomunikasi dengan hypervisor.

### 5.2 HVM (Hardware-Assisted Virtualization)

Hardware-Assisted Virtualization merupakan pendekatan virtualisasi yang memanfaatkan dukungan fitur virtualisasi dari perangkat keras prosesor.

Contoh teknologi pendukung:
- Intel VT-x.
- AMD-V.

Dukungan hardware membantu hypervisor menjalankan mesin virtual dengan mekanisme virtualisasi yang disediakan oleh prosesor.

## 6. Arsitektur Kontainer Modern

### 6.1 Pengertian Kontainer

Kontainer merupakan teknologi yang mengemas aplikasi bersama dependensi dan lingkungan yang dibutuhkan agar aplikasi dapat dijalankan secara konsisten.

Berbeda dengan VM, kontainer tidak memerlukan Guest OS terpisah untuk setiap aplikasi. Kontainer berbagi kernel dari sistem operasi host melalui container engine.

Contoh teknologi:
- Docker.
- containerd.

### 6.2 Karakteristik Kontainer

Kontainer memiliki beberapa karakteristik utama:

1. **Ringan:** tidak membutuhkan Guest OS terpisah untuk setiap kontainer.
2. **Cepat:** proses startup dapat berlangsung dalam hitungan detik atau lebih cepat.
3. **Portabel:** aplikasi beserta dependensinya dapat dikemas dan dijalankan pada lingkungan yang mendukung kontainer.
4. **Efisien:** penggunaan sumber daya dapat lebih rendah dibandingkan VM pada workload yang sesuai.
5. **Konsisten:** membantu menjaga kesamaan lingkungan pengembangan dan produksi.

### 6.3 Struktur Arsitektur Kontainer

Secara sederhana, arsitektur kontainer terdiri dari:

1. Application A dan dependensinya.
2. Application B dan dependensinya.
3. Container Engine seperti Docker atau containerd.
4. Host Operating System yang menyediakan kernel.
5. Infrastruktur perangkat keras.

Dengan pendekatan ini, beberapa kontainer dapat berjalan pada satu host dengan berbagi kernel sistem operasi.

## 7. Perbandingan Virtual Machine dan Kontainer

VM dan kontainer memiliki pendekatan isolasi serta penggunaan sumber daya yang berbeda.

| Metrik Evaluasi | Virtual Machine (VM) | Kontainer (Docker) |
|---|---|---|
| Tingkat abstraksi | Hardware level melalui hypervisor | OS level melalui kernel sharing |
| Waktu boot | 2–5 menit | Hitungan detik atau milidetik |
| Ukuran image | Besar, beberapa GB | Lebih ringan, MB |
| Isolasi dan keamanan | Isolasi tingkat mesin virtual | Isolasi tingkat proses |
| Kecepatan skalabilitas | Relatif lebih lambat dan berat | Lebih cepat dan dinamis |

### 7.1 Analisis Perbandingan

VM cocok ketika organisasi membutuhkan isolasi lingkungan Guest OS dan kontrol sistem operasi yang lebih terpisah.

Sementara itu, kontainer cocok untuk aplikasi yang membutuhkan proses deployment cepat, portabilitas, serta skalabilitas yang lebih dinamis.

Kontainer tidak selalu menggantikan VM. Pemilihan teknologi perlu disesuaikan dengan kebutuhan keamanan, kompatibilitas aplikasi, performa, dan pengelolaan infrastruktur.

## 8. Dampak Kinerja Bisnis

Skalabilitas tidak hanya berhubungan dengan kemampuan teknis, tetapi juga memberikan dampak terhadap proses bisnis.

Salah satu indikator yang dibahas dalam materi adalah respons elastisitas real-time.

Materi mencantumkan rata-rata auto-scaling kontainer dalam menghadapi lonjakan traffic sebesar:

**Kurang dari 3 detik.**

Respons yang cepat membantu sistem menyesuaikan kapasitas ketika terjadi lonjakan permintaan.

Dampak bisnis yang diharapkan:
- Mengurangi risiko gangguan layanan.
- Menjaga ketersediaan aplikasi.
- Mengurangi potensi kerugian akibat system outage.
- Mendukung transaksi dan pengajuan data dalam jumlah tinggi.
- Memberikan pengalaman layanan yang lebih konsisten.

Angka tersebut merupakan angka ilustratif dalam materi, bukan jaminan bahwa setiap implementasi kontainer selalu dapat melakukan scaling dalam waktu kurang dari tiga detik.

## 9. Orkestrasi dengan Kubernetes

### 9.1 Pengertian Kubernetes

Kubernetes atau K8s merupakan platform orkestrasi kontainer yang digunakan untuk mengelola aplikasi berbasis kontainer.

Kubernetes membantu mengatur deployment, jumlah replika, distribusi beban, dan pemulihan kontainer ketika terjadi kegagalan.

### 9.2 Fungsi Utama Kubernetes

**1. Auto-Scaling (HPA – Horizontal Pod Autoscaler)**

HPA merupakan mekanisme Kubernetes untuk menyesuaikan jumlah replika Pod secara otomatis berdasarkan metrik seperti penggunaan CPU dan RAM.

Ketika kebutuhan meningkat, jumlah replika dapat ditambah. Ketika kebutuhan menurun, jumlah replika dapat dikurangi sesuai kebijakan.

**2. Self-Healing System**

Self-healing merupakan kemampuan sistem untuk melakukan pemulihan secara otomatis.

Contohnya:
- Restart kontainer yang gagal.
- Mengganti Pod yang tidak berjalan dengan baik.
- Menjaga jumlah replika sesuai konfigurasi yang ditentukan.

**3. Load Balancing**

Load balancing membantu mendistribusikan traffic ke beberapa kontainer atau Pod yang aktif.

Tujuannya adalah menghindari penumpukan permintaan pada satu instance dan menjaga distribusi beban kerja.

### 9.3 Manfaat Kubernetes

- Mempermudah pengelolaan banyak kontainer.
- Mendukung horizontal scaling.
- Membantu pemulihan otomatis.
- Mendukung distribusi traffic.
- Mempermudah deployment aplikasi.
- Mendukung pengelolaan aplikasi dalam lingkungan produksi.

## 10. Arsitektur Hibrida: VM dan Kontainer

Arsitektur hybrid VM + kontainer merupakan pendekatan yang menggabungkan virtualisasi mesin dengan teknologi kontainer.

Keduanya memiliki fungsi yang saling melengkapi.

### 10.1 Infrastructure Base

Pada lapisan infrastruktur, Virtual Machine digunakan sebagai host untuk menjalankan lingkungan aplikasi.

Fungsinya:
- Isolasi tingkat penyewa atau multi-tenancy.
- Pengamanan lingkungan.
- Pengaturan batas alokasi sumber daya.
- Pengelolaan infrastruktur cloud.

Contoh platform:
- AWS EC2.
- Google Cloud Compute Engine.

### 10.2 Application Layer

Pada lapisan aplikasi, kontainer dijalankan di dalam instance VM.

Kontainer digunakan untuk menjalankan layanan mikro atau microservices.

Manfaatnya:
- Deployment lebih fleksibel.
- Portabilitas aplikasi.
- Scaling lebih granular.
- Pengelolaan layanan aplikasi lebih mudah.

### 10.3 Alur Arsitektur

Secara sederhana:

**Infrastruktur Fisik → Virtual Machine → Container Engine → Kontainer Aplikasi → Microservices**

Pendekatan ini menggabungkan isolasi VM dengan fleksibilitas dan kecepatan deployment kontainer.

## 11. FinOps dan Efisiensi Biaya (TCO)

### 11.1 Pengertian FinOps

FinOps merupakan pendekatan pengelolaan keuangan cloud yang menghubungkan tim teknologi, keuangan, dan bisnis untuk mengoptimalkan penggunaan sumber daya serta biaya cloud.

FinOps membantu organisasi memahami hubungan antara penggunaan infrastruktur dan biaya yang dikeluarkan.

### 11.2 TCO (Total Cost of Ownership)

TCO merupakan keseluruhan biaya yang dikeluarkan untuk memperoleh, menjalankan, dan mengelola infrastruktur selama periode tertentu.

Dalam penerapan VM dan kontainer, TCO dapat dipengaruhi oleh:

- Kebutuhan server fisik.
- Lisensi hypervisor.
- Lisensi Guest OS.
- CPU dan RAM.
- Daya listrik.
- Pendinginan data center.
- Pemeliharaan infrastruktur.
- Penggunaan sumber daya yang menganggur.

### 11.3 Optimasi Densitas

Optimasi densitas merupakan upaya meningkatkan pemanfaatan CPU dan RAM pada infrastruktur fisik.

Materi mencantumkan target utilisasi CPU/RAM hingga 80% pada server fisik.

Tujuannya:
- Memaksimalkan penggunaan perangkat keras.
- Mengurangi kapasitas yang menganggur.
- Mengurangi kebutuhan server tambahan.
- Meningkatkan efisiensi biaya infrastruktur.

Target utilisasi tetap perlu disesuaikan dengan karakteristik workload dan kapasitas cadangan yang dibutuhkan.

### 11.4 Penghematan CAPEX

Dalam ilustrasi materi:

- Infrastruktur berbasis VM membutuhkan sekitar 10 server fisik.
- Kontainer bare-metal membutuhkan sekitar 4 server fisik.
- Potensi penghematan CAPEX mencapai 60%.

Perhitungan persentase:

((10 − 4) ÷ 10) × 100% = 60%.

### 11.5 Penghematan Lisensi

Kontainer dapat mengurangi kebutuhan Guest OS terpisah untuk setiap aplikasi.

Materi mencantumkan potensi pengurangan lisensi Guest OS dan CPU-core hypervisor hingga 80%.

Besarnya penghematan aktual bergantung pada model lisensi, platform, dan arsitektur yang digunakan.

### 11.6 Penghematan OPEX

Konsolidasi server dapat mengurangi kebutuhan daya listrik dan pendinginan data center.

Materi mencantumkan potensi penghematan OPEX sebesar 60% untuk biaya listrik dan HVAC.

HVAC merupakan singkatan dari Heating, Ventilation, and Air Conditioning, yaitu sistem pemanas, ventilasi, dan pendingin udara.

### 11.7 Pay-per-Use Precision

Pay-per-use merupakan pendekatan pembayaran berdasarkan sumber daya yang benar-benar digunakan.

Dalam lingkungan kontainer, organisasi dapat mengoptimalkan alokasi sumber daya agar tidak membayar kapasitas komputasi yang tidak diperlukan.

### 11.8 Ringkasan Efisiensi Biaya

| Komponen | Dampak yang Dibahas dalam Materi |
|---|---|
| Kebutuhan hardware | Ilustrasi penghematan CAPEX 60% |
| Lisensi hypervisor dan OS | Potensi pengurangan lisensi hingga 80% |
| Listrik dan HVAC | Ilustrasi penghematan OPEX 60% |
| Utilisasi | Target utilisasi CPU/RAM hingga 80% |
| Pay-per-use | Penggunaan sumber daya sesuai kebutuhan |

Angka penghematan tersebut merupakan ilustrasi dari materi perkuliahan dan bukan hasil yang pasti untuk semua organisasi.

## 12. Studi Kasus Implementasi Skalabilitas Modern

Materi memberikan dua contoh penerapan skalabilitas berbasis kontainer dan virtualisasi.

### 12.1 E-Commerce Flash Sale

Pada sistem e-commerce, flash sale dapat menyebabkan lonjakan traffic yang sangat tinggi dalam waktu singkat.

Contoh kondisi:
- Jumlah pengunjung meningkat secara drastis.
- Permintaan transaksi meningkat.
- Layanan pembayaran harus tetap berjalan.
- Kapasitas aplikasi harus dapat menyesuaikan kebutuhan.

Materi memberikan ilustrasi lonjakan traffic hingga 10 kali lipat yang diatasi dengan otomatisasi scaling ribuan Pod kontainer dalam waktu 30 detik tanpa mengganggu modul pembayaran.

Pendekatan yang digunakan:
- Kubernetes untuk mengelola kontainer.
- Auto-scaling untuk menambah replika.
- Load balancing untuk membagi traffic.
- Self-healing untuk mengganti kontainer yang gagal.

Manfaat bisnis:
- Menjaga layanan ketika traffic meningkat.
- Mengurangi risiko gangguan transaksi.
- Menyesuaikan kapasitas dengan kebutuhan.
- Mendukung pengalaman pengguna.

### 12.2 Sistem Perbankan Digital

Pada sistem perbankan digital, keamanan dan isolasi data menjadi aspek penting.

Materi memberikan contoh penggunaan kombinasi VM dan kontainer.

Pendekatan yang digunakan:

- VM digunakan untuk isolasi yang lebih ketat pada database finansial.
- Kontainer digunakan untuk menjalankan aplikasi mobile banking.
- Kontainer membantu mempercepat proses deployment dan perilisan fitur baru.

Dengan pendekatan hybrid, organisasi dapat menyesuaikan teknologi berdasarkan karakteristik setiap workload.

## 13. Kesimpulan

Skalabilitas berbasis kontainer dan virtualisasi merupakan pendekatan penting dalam desain infrastruktur cloud modern.

Virtual Machine memberikan isolasi lingkungan melalui hypervisor dan memungkinkan setiap mesin virtual menjalankan Guest OS sendiri. Sementara itu, kontainer menggunakan kernel host sehingga lebih ringan, cepat, dan mendukung deployment aplikasi secara fleksibel.

Kubernetes membantu mengelola kontainer melalui auto-scaling, self-healing, dan load balancing. Kombinasi VM dan kontainer juga dapat digunakan untuk membangun arsitektur hybrid yang memanfaatkan keunggulan masing-masing teknologi.

Dari sisi bisnis, penggunaan kontainer dan optimasi infrastruktur dapat membantu meningkatkan utilisasi sumber daya serta mengurangi biaya CAPEX dan OPEX. Namun, keputusan implementasi tetap harus mempertimbangkan kebutuhan aplikasi, keamanan, biaya, dan kemampuan operasional organisasi.

## 14. Penggunaan AI

Dalam penyusunan rangkuman materi minggu ketujuh ini, saya menggunakan bantuan AI (ChatGPT) untuk membantu memahami, menyusun, dan merangkum materi dari file PDF perkuliahan.

### Prompt yang Digunakan

> Saya sedang mengerjakan tugas rangkuman mingguan mata kuliah Business Cloud Design. Bantu saya membuat rangkuman materi Minggu 07 berdasarkan file PDF yang saya berikan dengan judul Skalabilitas Berbasis Kontainer dan Virtualisasi. Susun rangkuman dalam format Markdown untuk README.md GitHub. Bahas landasan skalabilitas cloud, vertical scaling, horizontal scaling, arsitektur Virtual Machine, hypervisor Type 1 dan Type 2, PVM, HVM, arsitektur kontainer, perbandingan VM dan kontainer, dampak kinerja bisnis, Kubernetes, HPA, self-healing, load balancing, arsitektur hybrid VM dan kontainer, FinOps, TCO, efisiensi CAPEX dan OPEX, optimasi densitas, pay-per-use, serta studi kasus e-commerce flash sale dan perbankan digital. Gunakan bahasa Indonesia yang jelas dan mudah dipahami. Pertahankan istilah teknis, angka, dan ilustrasi sesuai PDF dosen. Jangan mengubah angka penghematan yang tercantum dalam materi. Berikan penjelasan tambahan hanya jika diperlukan untuk memperjelas konsep dan jangan menyajikannya sebagai kutipan langsung dari PDF.

### Bagian yang Dibantu AI

- Menyusun struktur rangkuman agar lebih sistematis.
- Menjelaskan kembali konsep virtualisasi dan kontainer dengan bahasa yang lebih mudah dipahami.
- Menyusun tabel perbandingan VM dan kontainer.
- Menjelaskan fungsi Kubernetes, HPA, self-healing, dan load balancing.
- Merapikan pembahasan FinOps dan efisiensi biaya.
- Menyusun kesimpulan dan dokumentasi penggunaan AI.

### Bagian yang Diperiksa dan Disesuaikan

- Memeriksa kesesuaian isi rangkuman dengan PDF perkuliahan.
- Memeriksa kembali istilah teknis dan angka ilustrasi penghematan.
- Menyesuaikan penjelasan agar mudah dipahami.
- Membaca kembali hasil rangkuman sebelum dipublikasikan ke GitHub.

## 15. Sumber Materi

- File perkuliahan: **07--business-cloud-design.pdf**
- Judul materi: Skalabilitas Berbasis Kontainer dan Virtualisasi.
- Mata Kuliah: Business Cloud Design.
- Dosen: Dr. Bambang Purnomosidi D. P.
- Program Studi: Sistem Informasi.
- Universitas Teknologi Digital Indonesia (UTDI).
