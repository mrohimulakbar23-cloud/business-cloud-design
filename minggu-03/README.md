# Minggu 03 – Private Cloud dan IT Alignment

## 1. Pendahuluan

Materi minggu ketiga mata kuliah Business Cloud Design membahas konsep **Private Cloud** dan **IT Alignment**. Pembahasan berfokus pada bagaimana infrastruktur cloud dirancang agar sesuai dengan kebutuhan organisasi dan mendukung pencapaian tujuan bisnis.

Keberhasilan penerapan teknologi tidak hanya dinilai dari kecanggihan perangkat atau sistem yang digunakan, tetapi juga dari manfaat yang diberikan kepada organisasi, seperti efisiensi, keamanan, keandalan, dan kualitas layanan.

## 2. Tujuan Pembelajaran

Setelah mempelajari materi ini, mahasiswa diharapkan mampu:

1. Memahami konsep private cloud dan perbedaannya dengan virtualisasi serta public cloud.
2. Menganalisis hubungan antara sasaran bisnis, strategi TI, dan keputusan desain private cloud.
3. Merancang prinsip arsitektur, tata kelola, KPI, dan roadmap implementasi private cloud.

## 3. Konsep Private Cloud

### 3.1 Pengertian Private Cloud

Private Cloud merupakan model cloud yang menyediakan lingkungan komputasi untuk satu organisasi dengan kontrol dan kebijakan yang ditentukan oleh organisasi tersebut.

Private cloud dapat ditempatkan di pusat data milik organisasi sendiri atau dikelola oleh pihak ketiga. Dengan demikian, lokasi fisik bukan satu-satunya faktor yang menentukan private cloud.

Private cloud menggabungkan beberapa kemampuan, yaitu:

- Resource pooling atau pengumpulan sumber daya.
- Otomatisasi layanan.
- Self-service yang tetap terkontrol.
- Pengukuran penggunaan sumber daya.
- Pengelolaan layanan secara konsisten.

Private cloud bukan sekadar satu server, satu hypervisor, atau kumpulan mesin virtual. Private cloud merupakan layanan infrastruktur yang dapat diminta, disediakan, diamankan, dan dipantau melalui mekanisme standar.

### 3.2 Perbedaan Virtualisasi dan Private Cloud

Virtualisasi merupakan teknologi abstraksi perangkat keras yang memungkinkan beberapa Virtual Machine (VM) berjalan pada satu host. Fokus utamanya adalah efisiensi dan isolasi workload.

Sementara itu, private cloud memiliki cakupan lebih luas karena mencakup katalog layanan, otomatisasi, kontrol akses, kebijakan, monitoring, dan tata kelola.

Dalam private cloud juga dikenal:

- **Showback:** biaya penggunaan sumber daya ditampilkan kepada unit bisnis, tetapi tidak benar-benar ditagihkan.
- **Chargeback:** biaya penggunaan sumber daya ditampilkan dan benar-benar dibebankan kepada unit bisnis.

Virtualisasi dapat menjadi fondasi private cloud, tetapi belum cukup untuk disebut sebagai private cloud tanpa adanya pengelolaan layanan dan tata kelola.

### 3.3 Perbandingan Private, Public, dan Hybrid Cloud

| Model | Karakteristik |
|---|---|
| Private Cloud | Kontrol dan penyesuaian tinggi. Organisasi bertanggung jawab terhadap kapasitas, operasi, dan keamanan. |
| Public Cloud | Menyediakan kapasitas elastis dan layanan yang luas. Memerlukan pengelolaan biaya, identitas, jaringan, dan vendor. |
| Hybrid Cloud | Menggabungkan beberapa lingkungan cloud. Membutuhkan pengelolaan identitas, konektivitas, klasifikasi data, dan tata kelola lintas lingkungan. |

### 3.4 Kapan Private Cloud Layak Dipertimbangkan?

Private cloud dapat dipertimbangkan apabila:

1. Organisasi membutuhkan kontrol terhadap data, konfigurasi, lokasi, atau persyaratan regulasi.
2. Workload relatif stabil atau dapat diperkirakan sehingga kapasitas dapat direncanakan.
3. Terdapat kebutuhan platform bersama untuk banyak tim atau unit bisnis.
4. Organisasi memiliki atau bersedia membangun kemampuan operasi, keamanan, otomatisasi, dan dukungan.
5. Terdapat business case yang mempertimbangkan TCO, risiko, dan nilai layanan.

## 4. IT Alignment

### 4.1 Pengertian IT Alignment

IT Alignment adalah keselarasan antara strategi dan sasaran bisnis dengan strategi, portofolio, proses, arsitektur, serta investasi teknologi informasi.

IT Alignment bukan sekadar meminta pengguna menyetujui proyek TI. Proses ini berlangsung dua arah:

- Pihak bisnis menjelaskan hasil yang dibutuhkan dan batasan risiko.
- Pihak TI menjelaskan pilihan teknologi, konsekuensi, serta kapabilitas yang diperlukan.

Keselarasan tersebut perlu dijaga mulai dari perencanaan, desain, implementasi, operasi, evaluasi, hingga perbaikan.

### 4.2 Hubungan Strategi Bisnis dengan TI

Hubungan antara strategi bisnis dan TI dapat digambarkan melalui empat tahapan:

1. **Strategi bisnis:** menentukan tujuan organisasi, misalnya mempercepat peluncuran produk digital.
2. **Kapabilitas:** menentukan kemampuan yang diperlukan, seperti lingkungan pengembangan yang cepat dan layanan yang tersedia.
3. **Arsitektur:** merancang katalog VM/container, jaringan, backup, otomatisasi provisioning, dan monitoring.
4. **Ukuran hasil:** mengukur waktu provisioning, availability, lead time rilis, biaya layanan, dan insiden keamanan.

Dengan hubungan tersebut, keputusan teknologi dapat dijelaskan berdasarkan manfaatnya terhadap organisasi.

### 4.3 Sasaran Bisnis dan Keputusan Cloud

Terdapat empat sasaran yang dapat menjadi pertimbangan dalam desain cloud:

- **Cepat:** menggunakan otomatisasi provisioning dan self-service dengan persetujuan sesuai risiko.
- **Andal:** menerapkan Service Level Objective (SLO), redundansi, backup, pemantauan, dan prosedur pemulihan.
- **Aman:** menerapkan klasifikasi data, prinsip least privilege, segmentasi, patching, logging, dan audit.
- **Efisien:** memperhatikan utilisasi sumber daya, biaya layanan, lifecycle VM, capacity planning, dan right-sizing.

### 4.4 Peran dan Tanggung Jawab

| Pihak | Tanggung Jawab |
|---|---|
| Pimpinan bisnis | Menetapkan sasaran, prioritas, toleransi risiko, dan hasil yang diharapkan. |
| CIO / IT Leadership | Menyelaraskan strategi TI, investasi, arsitektur, dan kapabilitas organisasi. |
| Platform Team | Membangun platform, otomatisasi layanan, kapasitas, keandalan, dan dokumentasi. |
| Security / Finance | Menetapkan kontrol, menguji kepatuhan, serta mengevaluasi biaya dan risiko. |

### 4.5 Governance atau Tata Kelola

Governance merupakan pengaturan keputusan, tanggung jawab, kebijakan, dan proses dalam pengelolaan private cloud.

Beberapa hal yang perlu ditentukan dalam tata kelola adalah:

1. Siapa yang boleh meminta layanan dan siapa yang menyetujui permintaan berisiko tinggi.
2. Workload dan data apa yang boleh ditempatkan di private cloud.
3. Standar yang wajib dipenuhi, seperti image, patch, backup, logging, jaringan, dan identitas.
4. Bagaimana kapasitas, biaya, dan pengecualian kebijakan ditinjau.
5. Bagaimana perubahan, insiden, pemulihan, dan penghentian layanan dikelola.

Tata kelola yang baik memberikan batasan dan aturan yang jelas tanpa membuat setiap permintaan menjadi proses birokrasi yang berlebihan.

## 5. Menerjemahkan IT Alignment ke Desain Private Cloud

### 5.1 Arsitektur Logis

Arsitektur private cloud yang selaras dengan bisnis terdiri dari empat bagian utama:

| Komponen | Fungsi |
|---|---|
| Layanan | Katalog, portal permintaan, image VM, API, dan alur persetujuan. |
| Kontrol | Identitas, RBAC, kebijakan, otomatisasi, inventory, kuota, dan audit trail. |
| Sumber daya | Compute, storage, jaringan, hypervisor, backup, dan kapasitas cadangan. |
| Operasi | Monitoring, logging, patching, incident/change management, dan pengujian restore. |

RBAC (Role Based Access Control) merupakan metode keamanan yang memberikan hak akses kepada pengguna berdasarkan peran pekerjaan mereka.

### 5.2 Prinsip Desain yang Mendukung Alignment

Terdapat lima prinsip desain yang perlu diperhatikan:

1. **Product Thinking:** platform diperlakukan sebagai produk internal yang memiliki pengguna, katalog, roadmap, dan dukungan.
2. **Standardisasi:** menyediakan jalur standar yang aman. Pengecualian harus memiliki alasan, pemilik, dan masa berlaku.
3. **Automation First:** mengotomatisasi pekerjaan berulang yang rawan kesalahan setelah prosesnya jelas.
4. **Security and Resilience by Design:** membangun keamanan, backup, pemulihan, dan observability sejak awal.
5. **Measure Outcomes:** mengukur hasil layanan, bukan hanya jumlah host, VM, atau kapasitas yang terpasang.

### 5.3 KPI dalam Private Cloud

KPI (Key Performance Indicator) digunakan untuk mengukur keberhasilan layanan private cloud.

Beberapa kelompok pengukuran yang dapat digunakan adalah:

| Aspek | Contoh Pengukuran |
|---|---|
| Kecepatan | Waktu permintaan sampai VM siap, lead time perubahan, dan provisioning otomatis. |
| Keandalan | Availability, jumlah insiden, MTTR, keberhasilan backup, dan hasil uji restore. |
| Efisiensi | Utilisasi compute/storage, biaya per workload, kapasitas menganggur, dan biaya operasi. |
| Pengalaman dan kontrol | Kepuasan pengguna, baseline compliance, patch compliance, dan temuan audit. |

Setiap KPI perlu memiliki definisi, baseline, target, sumber data, pemilik, dan frekuensi evaluasi.

MTTR (Mean Time to Repair) merupakan waktu yang diperlukan untuk memperbaiki sistem yang mengalami masalah.

### 5.4 TCO dan Business Case

TCO (Total Cost of Ownership) merupakan keseluruhan biaya yang perlu dipertimbangkan dalam kepemilikan dan pengelolaan teknologi.

Komponen biaya yang perlu dianalisis meliputi:

- **Biaya investasi:** server, storage, jaringan, lisensi, ruang, daya, pendinginan, dan fasilitas.
- **Biaya operasi:** staf, dukungan vendor, patching, monitoring, backup, keamanan, dan pembaruan infrastruktur.
- **Biaya risiko:** downtime, kehilangan data, ketergantungan pada personel kunci, dan kapasitas yang tidak memadai.
- **Manfaat potensial:** provisioning lebih cepat, standardisasi, kontrol lebih baik, utilisasi lebih tinggi, dan layanan konsisten.

Perbandingan biaya perlu dilakukan secara setara antara private cloud, public cloud, managed service, atau hybrid cloud. Perbandingan tidak cukup hanya menggunakan harga server dengan tagihan cloud, tetapi harus mempertimbangkan periode dan asumsi yang sama.

## 6. Roadmap Implementasi Private Cloud

Implementasi private cloud berbasis alignment dapat dilakukan melalui empat tahapan:

1. **Discover:** memetakan strategi, stakeholder, aplikasi, data, risiko, baseline KPI, dan biaya saat ini.
2. **Design:** memilih workload awal, target layanan, arsitektur, guardrail, SLO, dan operating model.
3. **Pilot:** menguji workload yang mewakili kebutuhan organisasi, provisioning, keamanan, backup-restore, dan pengalaman pengguna.
4. **Scale:** memperluas katalog, otomatisasi, showback, capacity planning, evaluasi KPI, dan perbaikan.

Guardrail merupakan seperangkat kebijakan, aturan, dan batasan yang diterapkan untuk mencegah tindakan yang berbahaya, melanggar kepatuhan, atau keluar dari standar keamanan yang ditetapkan.

## 7. Studi Kasus: Universitas dengan Layanan Digital

Materi memberikan contoh universitas yang ingin mempercepat penyediaan lingkungan praktikum, menjaga data akademik, dan mengendalikan biaya.

Kondisi awal yang dihadapi:

- Server terpisah pada setiap laboratorium.
- Permintaan VM masih dilakukan secara manual.
- Backup belum pernah diuji proses restore-nya.
- Tim TI terbatas dan anggaran terbatas.
- Terdapat lonjakan kebutuhan pada awal semester.
- Aplikasi menyimpan data sensitif.

Contoh analisis penyelesaian:

- **Sasaran:** lingkungan praktikum tersedia dalam waktu maksimal 15 menit dan 95% permintaan standar dapat diproses tanpa intervensi manual.
- **Kapabilitas:** katalog VM/container, kuota per mata kuliah, provisioning otomatis, segmentasi, dan expiry policy.
- **Kendali:** akses berbasis peran, image yang terpelihara, pemisahan data akademik, serta pengujian backup secara berkala.
- **KPI:** waktu provisioning, kegagalan permintaan, utilisasi host, keberhasilan restore test, dan biaya per image VM/container.
- **Risiko:** lonjakan kebutuhan pada awal semester dan VM yang tidak lagi digunakan. Mitigasinya melalui capacity planning, kuota, expiry policy, dan alert.

Angka target pada contoh tersebut merupakan ilustrasi. Target sebenarnya perlu ditetapkan berdasarkan baseline organisasi.

## 8. Risiko IT Alignment

Terdapat beberapa risiko yang sering terjadi dalam penerapan IT Alignment:

1. **Technology-first:** platform dibeli sebelum kebutuhan dan hasil bisnis disepakati.
2. **Ownership kabur:** tidak jelas siapa pemilik layanan, data, biaya, dan risiko.
3. **Cloud-washing:** virtualisasi dianggap sebagai cloud meskipun belum memiliki self-service, otomatisasi, dan governance.
4. **Metrics theater:** uptime dan kapasitas dilaporkan tanpa menunjukkan dampaknya terhadap layanan.

## 9. Kesimpulan

Private cloud merupakan kapabilitas layanan infrastruktur yang dikelola secara terstruktur, bukan hanya perangkat keras atau hypervisor. Sementara itu, IT Alignment memastikan strategi bisnis, investasi, arsitektur, dan operasi TI tetap saling terhubung.

Keberhasilan penerapan private cloud perlu dilihat dari manfaat layanan yang dihasilkan, seperti keamanan, keandalan, efisiensi, dan kemampuan untuk terus melakukan perbaikan. Oleh karena itu, organisasi perlu memulai perencanaan dari masalah dan hasil bisnis yang ingin dicapai, kemudian memilih teknologi sebagai sarana untuk mencapainya.

## 10. Penggunaan AI

Dalam penyusunan rangkuman materi minggu ketiga ini, saya menggunakan bantuan AI (ChatGPT) untuk membantu memahami, menyusun, dan merangkum materi dari file PDF perkuliahan.

### Prompt yang Digunakan

> Saya sedang mengerjakan tugas rangkuman mingguan mata kuliah Business Cloud Design. Bantu saya membuat rangkuman materi Minggu 03 berdasarkan file PDF yang saya berikan dengan judul Private Cloud dan IT Alignment. Susun rangkuman dalam format Markdown untuk README.md GitHub. Bahas pengertian private cloud, perbedaan virtualisasi dengan private cloud, perbandingan private, public, dan hybrid cloud, IT Alignment, governance, arsitektur private cloud, prinsip desain, KPI, TCO, roadmap implementasi, studi kasus, risiko alignment, dan kesimpulan. Gunakan bahasa Indonesia yang jelas dan mudah dipahami. Pertahankan istilah penting sesuai materi dosen, jangan menambahkan informasi yang tidak terdapat dalam PDF, dan sertakan tabel jika dapat membantu pemahaman.

### Bagian yang Dibantu AI

- Menyusun struktur rangkuman agar lebih sistematis.
- Menjelaskan kembali istilah teknis menggunakan bahasa yang lebih mudah dipahami.
- Membuat tabel perbandingan dan merapikan poin-poin materi.
- Menyusun kesimpulan dan dokumentasi penggunaan AI.

### Bagian yang Diperiksa dan Disesuaikan

- Memeriksa kesesuaian isi rangkuman dengan materi PDF perkuliahan.
- Menyesuaikan istilah teknis agar tetap sesuai dengan penjelasan dosen.
- Membaca kembali hasil rangkuman sebelum dipublikasikan ke GitHub.

## 11. Sumber Materi

- File perkuliahan: **03--private-cloud--IT-alignment.pdf**
- Mata Kuliah: Business Cloud Design
- Dosen: Dr. Bambang Purnomosidi D. P.
- Universitas Teknologi Digital Indonesia (UTDI)

