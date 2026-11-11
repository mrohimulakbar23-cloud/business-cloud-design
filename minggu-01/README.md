# Minggu 01 — Paradigma Cloud Computing dan Gerakan Open Source

## 1. Pendahuluan

Cloud Computing merupakan salah satu perkembangan teknologi informasi yang memungkinkan pengguna mengakses sumber daya komputasi melalui jaringan internet sesuai kebutuhan. Sumber daya tersebut meliputi server, jaringan, penyimpanan, aplikasi, dan berbagai layanan lainnya.

Dalam materi ini dibahas pengertian Cloud Computing, sejarah perkembangannya, karakteristik, kelebihan dan kekurangan, model layanan, model deployment, serta hubungan Cloud Computing dengan gerakan Open Source dalam menciptakan nilai tambah bagi bisnis.

## 2. Pengertian Cloud Computing

Menurut National Institute of Standards and Technology (NIST), Cloud Computing adalah model yang memungkinkan akses jaringan secara luas, mudah, dan sesuai permintaan terhadap kumpulan sumber daya komputasi yang dapat dikonfigurasi.

Sumber daya tersebut dapat berupa:
- Jaringan (network).
- Server.
- Penyimpanan (storage).
- Aplikasi.
- Layanan komputasi lainnya.

Sumber daya tersebut dapat disediakan dan dilepaskan dengan cepat tanpa membutuhkan banyak interaksi dengan penyedia layanan.

Dengan demikian, pengguna tidak harus memiliki seluruh perangkat keras dan infrastruktur sendiri untuk memanfaatkan layanan komputasi.

## 3. Sejarah Cloud Computing

Perkembangan Cloud Computing melalui beberapa tahapan penting, antara lain:

| Tahun | Perkembangan |
|---|---|
| 1950-an | Era mainframe dan teori time-sharing system oleh John McCarthy. |
| 1961 | John McCarthy memprediksi komputer suatu saat dapat digunakan seperti air dan listrik, berkaitan dengan konsep Grid Computing. |
| 1969 | ARPANET mulai berkembang. |
| 1990 | World Wide Web (WWW) oleh Tim Berners-Lee dan perkembangan Client-Server Computing. |
| 1997 | Prof. Ramnath Chellappa menggunakan istilah Cloud Computing. |
| 1999 | Salesforce.com mulai hadir. |
| 2002 | Amazon Web Services (AWS) mulai berkembang. |
| 2006 | Amazon EC2 diperkenalkan. |
| 2009 | Google Cloud mulai berkembang. |

Perkembangan tersebut menunjukkan perubahan dari penggunaan komputer secara terpusat menuju layanan komputasi yang dapat diakses melalui jaringan sesuai kebutuhan.

## 4. Karakteristik Cloud Computing

Cloud Computing memiliki beberapa karakteristik utama:

### 4.1 On-Demand Self-Service

Pengguna dapat memperoleh sumber daya komputasi, seperti penyimpanan atau waktu penggunaan server, secara otomatis sesuai kebutuhan tanpa harus berinteraksi langsung dengan penyedia layanan.

### 4.2 Broad Network Access

Layanan Cloud Computing dapat diakses melalui jaringan menggunakan berbagai perangkat, seperti komputer, laptop, tablet, dan smartphone dari berbagai lokasi.

### 4.3 Resource Pooling

Penyedia layanan mengelompokkan sumber daya komputasi fisik maupun virtual, seperti server, penyimpanan, dan jaringan, untuk melayani banyak pelanggan secara bersamaan.

### 4.4 Rapid Elasticity

Sumber daya komputasi dapat ditambah atau dikurangi secara cepat dan otomatis mengikuti perubahan kebutuhan pengguna.

### 4.5 Measured Service

Penggunaan sumber daya dipantau dan diukur oleh penyedia layanan. Pengukuran tersebut dapat digunakan untuk memberikan transparansi penggunaan serta sistem pembayaran berdasarkan konsumsi.

### 4.6 Multitenancy

Satu sumber daya perangkat lunak atau perangkat keras dapat melayani banyak pelanggan (tenant), dengan data dan aktivitas setiap pelanggan tetap terisolasi.

## 5. Kelebihan dan Kekurangan Cloud Computing

### 5.1 Kelebihan

Beberapa kelebihan Cloud Computing berdasarkan materi perkuliahan adalah:

1. **Ekonomis:** biaya dapat disesuaikan dengan kebutuhan dan model pembayaran penyedia layanan.
2. **Kapasitas penyimpanan:** menyediakan kapasitas penyimpanan yang dapat diperluas sesuai layanan.
3. **Universal Access:** layanan dapat diakses dari berbagai lokasi dan perangkat.
4. **Scaling:** sumber daya dapat disesuaikan dengan kebutuhan.
5. **Backup and Recovery:** mendukung pencadangan dan pemulihan data.
6. **Security and Reliability:** menyediakan fitur keamanan dan keandalan layanan.

Model penentuan harga dapat berupa subscription, bulanan, per jam atau detik, serta transient/spot.

### 5.2 Kekurangan

Beberapa kekurangan Cloud Computing meliputi:

1. Ketergantungan pada koneksi internet.
2. Permasalahan privasi (privacy issues).
3. Downtime atau layanan tidak tersedia sementara.
4. Biaya penggunaan yang dalam kondisi tertentu dapat lebih tinggi dibandingkan infrastruktur on-premises.

## 6. Model Layanan Cloud Computing

Secara umum, terdapat tiga kelompok besar model layanan Cloud Computing:

### 6.1 Software as a Service (SaaS)

SaaS merupakan model layanan yang memungkinkan pengguna menggunakan fungsionalitas suatu perangkat lunak tanpa harus melakukan instalasi dan pemeliharaan aplikasi di komputer sendiri.

Aplikasi disediakan oleh penyedia layanan dan umumnya dapat diakses melalui web.

Contoh:
- Microsoft 365.
- Google Docs.

### 6.2 Platform as a Service (PaaS)

PaaS merupakan layanan yang menyediakan platform lengkap berupa perangkat keras, perangkat lunak, dan infrastruktur untuk membangun, menjalankan, serta mengelola aplikasi.

PaaS dapat digunakan untuk:
- Development framework.
- Analytics dan Business Intelligence.
- Workflow, keamanan, dan scheduling.
- Pengembangan serta pengelolaan API.
- Internet of Things (IoT).
- AI Services.

Materi juga menjelaskan bahwa teknologi container menjadi salah satu pendukung kemudahan penggunaan PaaS.

Docker berfungsi sebagai container engine untuk mengelola image, seperti menjalankan, mengaktifkan, menonaktifkan, dan menghapus container.

Teknologi yang berkaitan dengan container antara lain Docker, Docker Compose, Docker Swarm, dan Kubernetes.

### 6.3 Infrastructure as a Service (IaaS)

IaaS merupakan model layanan yang menyediakan sumber daya infrastruktur komputasi sesuai permintaan (on-demand) dengan sistem pembayaran pay-as-you-go.

Sumber daya yang disediakan meliputi:
- Data center fisik.
- Sumber daya komputasi.
- Jaringan.
- Storage.

IaaS menggunakan teknologi seperti hypervisor untuk menjalankan virtual machine. Contohnya Xen, KVM, VMware, VirtualBox, dan Hyper-V.

Perangkat lunak orkestrasi cloud yang disebutkan dalam materi antara lain Apache CloudStack, OpenNebula, dan OpenStack.

Materi juga membahas Bare Metal as a Service (BMaaS), yaitu layanan yang memberikan akses langsung ke perangkat keras. BMaaS dapat digunakan untuk kebutuhan seperti High Performance Computing, Big Data Analytics, dan GPU Computing.

### 6.4 XaaS (Everything as a Service)

XaaS merupakan istilah untuk berbagai kemampuan komputasi yang disediakan sebagai layanan. Contohnya meliputi SaaS, PaaS, IaaS, Backend as a Service, dan Data as a Service.

## 7. Model Deployment Cloud Computing

Materi memperkenalkan empat model deployment Cloud Computing:

1. **Public Cloud:** layanan cloud yang disediakan untuk digunakan oleh publik.
2. **Private Cloud:** lingkungan cloud yang diperuntukkan secara khusus bagi satu organisasi.
3. **Hybrid Cloud:** kombinasi dari beberapa model cloud.
4. **Community Cloud:** lingkungan cloud yang digunakan bersama oleh kelompok organisasi dengan kebutuhan tertentu.

## 8. Perusahaan Penyedia Cloud Computing

Materi menyebutkan beberapa perusahaan penyedia layanan Cloud Computing.

**Penyedia dari luar Indonesia:**
- Amazon Web Services (AWS).
- Google.
- Alibaba.
- Heroku.
- Microsoft.
- Oracle.
- IBM.

**Penyedia di Indonesia:**
- Biznet Gio.
- Telkom Telstra.
- Lintas Arta.

## 9. Hubungan Cloud Computing dan Open Source

Open Source memiliki peran penting dalam perkembangan infrastruktur Cloud Computing. Materi menjelaskan bahwa banyak infrastruktur cloud modern, baik Public Cloud maupun Private Cloud, dibangun menggunakan teknologi Open Source.

Contoh teknologi yang disebutkan adalah Linux, KVM, dan Kubernetes.

Hubungan antara keduanya dapat dijelaskan melalui beberapa hal:

### 9.1 Open Source sebagai Pondasi Teknologi

Teknologi Open Source menyediakan dasar untuk membangun infrastruktur cloud yang fleksibel dan membantu mengurangi ketergantungan terhadap vendor tertentu (vendor lock-in).

### 9.2 Cloud Computing sebagai Pendukung Inovasi

Cloud Computing memungkinkan perusahaan menggunakan infrastruktur komputasi tanpa harus selalu membeli perangkat keras yang mahal terlebih dahulu. Sumber daya dapat disediakan sesuai kebutuhan dan anggaran operasional (OPEX).

### 9.3 Mempercepat Siklus Inovasi

Perusahaan dapat menggunakan kode Open Source, menjalankannya pada lingkungan cloud, melakukan eksperimen, dan mengembangkan produk baru dalam waktu yang lebih singkat.

## 10. Business Value Added dari Cloud Computing dan Open Source

Kombinasi Cloud Computing dan Open Source dapat memberikan nilai tambah bagi bisnis melalui beberapa aspek:

1. **Kolaborasi:** komunitas Open Source dan fleksibilitas infrastruktur cloud mendukung kolaborasi serta business agility dengan biaya yang lebih terkendali.
2. **Kedaulatan Data dan Efisiensi Biaya:** penggunaan Open Source pada Private Cloud dapat membantu organisasi menjaga kerahasiaan data sekaligus mengurangi biaya lisensi.
3. **Standarisasi Global:** teknologi Open Source mendukung integrasi sistem, migrasi, dan kolaborasi tanpa terikat pada satu ekosistem tertentu.
4. **Inovasi Bisnis:** komunitas Open Source menghasilkan inovasi, Cloud Computing menyediakan teknologi tersebut sebagai layanan, dan bisnis memanfaatkannya untuk menciptakan nilai baru.

## 11. Kesimpulan

Cloud Computing merupakan model penyediaan sumber daya komputasi melalui jaringan yang dapat digunakan sesuai kebutuhan. Teknologi ini memiliki karakteristik seperti On-Demand Self-Service, Broad Network Access, Resource Pooling, Rapid Elasticity, Measured Service, dan Multitenancy.

Cloud Computing memiliki tiga model layanan utama, yaitu SaaS, PaaS, dan IaaS, serta empat model deployment, yaitu Public, Private, Hybrid, dan Community Cloud.

Selain itu, Open Source menjadi salah satu pondasi penting dalam pembangunan infrastruktur cloud. Kombinasi keduanya dapat mendukung efisiensi biaya, kolaborasi, kedaulatan data, dan percepatan inovasi sehingga menghasilkan nilai tambah bagi bisnis.

## 12. Penggunaan AI

Dalam penyusunan rangkuman ini, digunakan bantuan AI (ChatGPT GPT-6).

**Prompt yang digunakan:**

"Buat rangkuman materi perkuliahan berdasarkan file PDF yang diberikan. Susun secara sistematis menggunakan bahasa Indonesia yang mudah dipahami, pertahankan istilah penting dari materi, dan jangan menghilangkan pokok pembahasan."

**Bagian yang diadaptasi:**
- Materi PDF diringkas dan disusun ulang menjadi beberapa subbab.
- Penjelasan disederhanakan agar lebih mudah dipahami.
- Istilah teknis dan contoh utama tetap mengikuti materi perkuliahan.
- Kesimpulan disusun berdasarkan pembahasan dalam materi.

**Sumber materi utama:**

PDF perkuliahan Business Cloud Design — *01: Paradigma Cloud Computing dan Gerakan Open Source*, Dr. Bambang Purnomosidi D. P., Fakultas Teknologi Informasi, Universitas Teknologi Digital Indonesia.

**Referensi tambahan:**

Mell, P., & Grance, T. (2011). *The NIST Definition of Cloud Computing*. NIST Special Publication 800-145. https://doi.org/10.6028/NIST.SP.800-145
