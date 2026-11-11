# Minggu 04 – Ekonomi Private Cloud dan Capital Expenditure (CAPEX)

## 1. Pendahuluan

Materi minggu keempat mata kuliah Business Cloud Design membahas aspek ekonomi dalam penerapan private cloud, khususnya biaya investasi dan biaya operasional. Materi ini menjelaskan bagaimana organisasi menentukan pilihan infrastruktur berdasarkan kebutuhan bisnis, biaya, risiko, serta manfaat yang diperoleh.

Pemilihan antara private cloud dan public cloud tidak cukup hanya berdasarkan harga awal. Organisasi perlu menghitung keseluruhan biaya selama periode penggunaan dan memastikan bahwa layanan yang dibandingkan memiliki kapasitas serta tingkat layanan yang sebanding.

## 2. Tujuan Pembelajaran

Setelah mempelajari materi ini, mahasiswa diharapkan mampu:

1. Menjelaskan karakteristik private cloud dan model biayanya.
2. Membedakan CAPEX, OPEX, biaya langsung, dan biaya tidak langsung.
3. Mengidentifikasi komponen Total Cost of Ownership (TCO) private cloud.
4. Membandingkan skenario private cloud dan public cloud secara terstruktur.
5. Menyusun rekomendasi awal berdasarkan biaya, risiko, dan kebutuhan bisnis.

## 3. Konsep Dasar Private Cloud dan Model Biaya

### 3.1 Pengertian Private Cloud

Private cloud merupakan lingkungan cloud yang digunakan secara eksklusif oleh satu organisasi. Sumber daya dapat berada di pusat data sendiri, fasilitas colocation, atau fasilitas milik provider.

Private cloud dapat dikelola sendiri (*self-managed*), dikelola oleh pihak ketiga (*managed private cloud*), atau menggunakan kombinasi keduanya.

Karakteristik cloud seperti self-service, resource pooling, elasticity, dan layanan terukur tetap menjadi bagian penting dari private cloud.

### 3.2 Perbedaan Istilah Penting

| Istilah | Pengertian |
|---|---|
| Private Cloud | Lingkungan cloud khusus untuk satu organisasi. |
| On-Premises | Infrastruktur yang berada di lokasi organisasi. |
| Virtualisasi | Teknologi untuk mengabstraksi server agar dapat menjalankan beberapa lingkungan virtual. |
| CAPEX | Pengeluaran untuk memperoleh atau meningkatkan aset jangka panjang. |
| OPEX | Biaya operasional yang muncul ketika layanan dijalankan. |

On-premises tidak otomatis berarti private cloud. Begitu juga virtualisasi saja belum cukup untuk menjadikan sebuah infrastruktur sebagai layanan cloud.

## 4. Ekonomi Cloud dan Total Cost of Ownership (TCO)

### 4.1 Pengertian TCO

TCO (Total Cost of Ownership) merupakan seluruh biaya yang diperlukan untuk memperoleh, menjalankan, melindungi, dan menghentikan suatu layanan atau infrastruktur.

TCO tidak hanya memperhitungkan harga pembelian perangkat, tetapi juga biaya selama masa penggunaan.

Secara sederhana:

**TCO = Biaya Akuisisi + Biaya Operasi + Biaya Risiko dan Akhir Masa Pakai**

Komponen TCO meliputi:

- **Akuisisi:** hardware, software, dan biaya setup.
- **Operasi:** sumber daya manusia, listrik, dukungan, serta pemeliharaan.
- **Risiko dan akhir masa pakai:** downtime, pembaruan perangkat, dan biaya penghentian atau pembuangan aset.

Dalam membandingkan beberapa alternatif, organisasi perlu menggunakan periode analisis yang sama, misalnya tiga atau lima tahun, kapasitas yang sama, dan tingkat layanan yang sama.

### 4.2 Unit Economics

Biaya total dapat diubah menjadi biaya per unit agar lebih mudah digunakan untuk membandingkan layanan.

Contohnya:

| Metrik | Perhitungan |
|---|---|
| Biaya per VM-bulan | TCO periode dibagi total VM-bulan yang disediakan. |
| Biaya per pengguna | TCO periode dibagi jumlah pengguna aktif yang relevan. |
| Biaya per transaksi | TCO periode dibagi volume transaksi. |

Metrik unit membantu organisasi mengetahui biaya layanan secara lebih terperinci. Namun, hasilnya tetap perlu disertai konteks performa, availability, keamanan, dan pola penggunaan.

### 4.3 Utilisasi Sumber Daya

Utilisasi menunjukkan seberapa banyak kapasitas infrastruktur yang benar-benar digunakan.

Terdapat dua kondisi yang perlu diperhatikan:

- **Utilisasi rendah:** biaya tetap dibebankan kepada sedikit workload sehingga biaya per unit meningkat. Kapasitas yang tidak digunakan menyebabkan pemborosan.
- **Utilisasi sehat:** konsolidasi workload dapat meningkatkan penggunaan sumber daya sehingga biaya per unit menjadi lebih efisien.

Namun, utilisasi tidak boleh dipaksakan hingga 100%. Organisasi tetap perlu menyediakan kapasitas cadangan (*headroom*) untuk menghadapi lonjakan penggunaan dan kegagalan sistem.

## 5. CAPEX dan OPEX

### 5.1 CAPEX (Capital Expenditure)

CAPEX adalah pengeluaran untuk memperoleh atau meningkatkan aset yang memberikan manfaat lebih dari satu periode.

Contoh CAPEX:

- Server.
- Storage.
- Perangkat jaringan.
- Perangkat fasilitas.
- Implementasi infrastruktur yang memenuhi kebijakan kapitalisasi.

CAPEX biasanya membutuhkan pengeluaran dana yang cukup besar pada awal investasi. Aset tersebut dapat disusutkan sepanjang umur manfaat sesuai kebijakan akuntansi yang berlaku.

Pertanyaan penting sebelum melakukan investasi adalah apakah kapasitas yang dibeli akan digunakan cukup lama dan cukup tinggi sehingga investasi tersebut layak dilakukan.

### 5.2 OPEX (Operational Expenditure)

OPEX merupakan biaya operasional yang muncul ketika infrastruktur atau layanan digunakan dan dikelola.

Contohnya:

- Listrik dan pendinginan.
- Kontrak dukungan.
- Lisensi berulang.
- Staf operasional.
- Biaya penggunaan layanan cloud.

Pada layanan cloud, biaya dapat mengikuti jumlah penggunaan, reservasi, kapasitas, atau kombinasi beberapa model tersebut.

OPEX tidak selalu berarti lebih murah. Konsumsi cloud yang tidak dikendalikan dapat menyebabkan biaya meningkat dengan cepat.

### 5.3 Perbandingan CAPEX dan OPEX

| Dimensi | Private Cloud dengan Investasi Aset | Public Cloud / Layanan Konsumsi |
|---|---|---|
| Arus kas | Umumnya besar di awal. | Tersebar atau mengikuti konsumsi. |
| Kapasitas | Dibeli sebelum digunakan. | Dapat ditambah atau dikurangi. |
| Risiko utilisasi | Lebih banyak ditanggung organisasi. | Sebagian dapat dialihkan kepada provider. |
| Kontrol | Kontrol fisik dan konfigurasi lebih besar. | Bergantung pada layanan dan kontrak. |
| Tantangan | Overprovisioning, refresh, dan aset menganggur. | Bill shock, vendor lock-in, dan biaya berulang. |

Perbandingan tidak cukup hanya melihat label CAPEX dan OPEX. Organisasi juga harus mempertimbangkan pola arus kas, fleksibilitas, perubahan biaya, dan tanggung jawab operasional.

### 5.4 Depresiasi dan Arus Kas

Depresiasi merupakan proses alokasi biaya aset selama masa manfaatnya dalam laporan keuangan.

Contoh:

- Harga server dan storage: Rp600 juta.
- Umur manfaat: 5 tahun.
- Nilai residu: diabaikan.
- Metode: depresiasi garis lurus.

Perhitungannya:

**Depresiasi per tahun = Harga aset ÷ Umur manfaat**

**Rp600 juta ÷ 5 = Rp120 juta per tahun.**

Depresiasi bukan pembayaran kas tahunan yang baru. Arus kas pembelian umumnya terjadi ketika aset dibayar. Perlakuan aktual mengikuti kebijakan akuntansi dan pajak yang berlaku.

## 6. Kerangka Keputusan Investasi

Sebelum memilih model infrastruktur, organisasi perlu mempertimbangkan enam aspek berikut:

1. **Kebutuhan:** mengidentifikasi workload, SLA, keamanan, dan regulasi.
2. **Kapasitas:** memperhatikan baseline penggunaan, kebutuhan puncak, pertumbuhan, dan headroom.
3. **Biaya:** menghitung TCO, arus kas, dan unit economics.
4. **Risiko:** mempertimbangkan availability, kemampuan SDM, vendor, dan vendor lock-in.
5. **Opsi:** membandingkan alternatif build, buy, host, dan hybrid.
6. **Ukur ulang:** melakukan evaluasi menggunakan FinOps, utilisasi, dan biaya aktual.

FinOps (Financial Operations) merupakan kerangka kerja operasional dan praktik budaya yang menyatukan tim teknik, keuangan, dan bisnis untuk mengelola pengeluaran cloud secara bersama-sama.

## 7. Studi Kasus: Private Cloud untuk Kampus

Materi memberikan studi kasus universitas yang ingin mengonsolidasikan sistem akademik, Learning Management System (LMS), dan aplikasi internal.

### 7.1 Data Kebutuhan

| Komponen | Keterangan |
|---|---|
| Kebutuhan infrastruktur | 120 VM ekuivalen |
| Storage | 80 TB |
| Target ketersediaan | 99,9% |
| Periode analisis | 5 tahun |

Terdapat dua alternatif yang dibandingkan:

| Komponen | Private Cloud | Public Cloud |
|---|---:|---:|
| Investasi awal (CAPEX) | Rp1,2 miliar | Migrasi Rp100 juta |
| Biaya tahunan | Rp300 juta | Rp520 juta |
| Periode analisis | 5 tahun | 5 tahun |

### 7.2 Perhitungan Biaya Lima Tahun

**A. Private Cloud**

Rumus:

CAPEX + (OPEX tahunan × 5 tahun)

Perhitungan:

Rp1,2 miliar + (Rp300 juta × 5)

= Rp1,2 miliar + Rp1,5 miliar

= **Rp2,7 miliar**

**B. Public Cloud**

Rumus:

Biaya migrasi + (Biaya tahunan × 5 tahun)

Perhitungan:

Rp100 juta + (Rp520 juta × 5)

= Rp100 juta + Rp2,6 miliar

= **Rp2,7 miliar**

### 7.3 Analisis Hasil

Berdasarkan perhitungan nominal selama lima tahun, kedua alternatif menghasilkan biaya yang sama, yaitu Rp2,7 miliar.

Artinya, keputusan tidak dapat berhenti pada jumlah biaya saja. Organisasi perlu mempertimbangkan faktor lain, seperti performa, kapasitas, SLA, backup, keamanan, dan risiko.

Perhitungan tersebut juga belum memasukkan beberapa komponen, seperti:

- Diskonto.
- Pajak.
- Refresh hardware.
- Nilai residu.
- Biaya sumber daya manusia.
- Risiko operasional.

Selain itu, perlu diperiksa apakah kapasitas, performa, keamanan, dan tingkat layanan kedua alternatif benar-benar setara.

## 8. Analisis Sensitivitas

Analisis sensitivitas dilakukan untuk mengetahui bagaimana perubahan asumsi dapat memengaruhi hasil perhitungan biaya.

Beberapa faktor yang perlu diuji adalah:

1. **Utilisasi turun:** kapasitas private cloud yang menganggur meningkat sehingga biaya per workload menjadi lebih tinggi.
2. **Kebutuhan tumbuh:** private cloud mungkin membutuhkan investasi tambahan, sedangkan public cloud dapat memberikan fleksibilitas kapasitas.
3. **Harga cloud berubah:** diskon, nilai tukar, biaya egress atau aliran data keluar dari cloud, dan pola konsumsi dapat mengubah total biaya.

Analisis sebaiknya menggunakan minimal tiga skenario, yaitu rendah, dasar, dan tinggi untuk volume penggunaan, utilisasi, serta biaya operasi.

## 9. Risiko Ekonomi yang Sering Terlewat

Terdapat beberapa risiko yang perlu diperhatikan dalam keputusan ekonomi cloud:

- **Technical Debt:** perangkat lama, arsitektur yang sulit diubah, dan integrasi khusus dapat menambah biaya pemeliharaan.
- **Skill & Staffing:** ketergantungan pada personel tertentu dan kebutuhan pelatihan dapat memengaruhi biaya operasional.
- **Resilience:** redundansi, backup, disaster recovery, dan pengujian pemulihan membutuhkan biaya.
- **Vendor Lock-in:** biaya perpindahan, format data, layanan proprietary, dan kontrak dapat membatasi pilihan organisasi.
- **Governance:** kapasitas yang tidak terpakai, shadow IT, dan tagihan tanpa pemilik dapat menyebabkan pemborosan.

## 10. Kesimpulan

Ekonomi private cloud tidak hanya membahas biaya pembelian server, tetapi juga seluruh biaya yang muncul selama layanan digunakan hingga dihentikan. TCO perlu memperhitungkan biaya langsung, tidak langsung, risiko, serta akhir masa pakai.

CAPEX dan OPEX menjelaskan pola pengeluaran, tetapi tidak secara otomatis menunjukkan bahwa suatu model lebih murah. Perbandingan private cloud dan public cloud harus menggunakan workload, periode analisis, kapasitas, dan tingkat layanan yang sebanding.

Oleh karena itu, organisasi perlu melakukan perhitungan biaya secara menyeluruh, mengevaluasi risiko, dan mengukur biaya aktual setelah implementasi dengan metrik serta tata kelola yang jelas.

## 11. Penggunaan AI

Dalam penyusunan rangkuman materi minggu keempat ini, saya menggunakan bantuan AI (ChatGPT) untuk membantu memahami, menyusun, dan merangkum materi dari file PDF perkuliahan.

### Prompt yang Digunakan

> Saya sedang mengerjakan tugas rangkuman mingguan mata kuliah Business Cloud Design. Bantu saya membuat rangkuman materi Minggu 04 berdasarkan file PDF yang saya berikan dengan topik Ekonomi Private Cloud dan Capital Expenditure (CAPEX). Susun rangkuman dalam format Markdown untuk README.md GitHub. Bahas tujuan pembelajaran, konsep private cloud, TCO, unit economics, utilisasi, CAPEX, OPEX, depresiasi, kerangka keputusan investasi, studi kasus kampus, perhitungan biaya private cloud dan public cloud selama lima tahun, analisis sensitivitas, risiko ekonomi, dan kesimpulan. Gunakan bahasa Indonesia yang jelas dan mudah dipahami. Pertahankan istilah dan angka sesuai materi dosen, jangan mengubah hasil perhitungan, dan sertakan tabel jika membantu pemahaman.

### Bagian yang Dibantu AI

- Menyusun struktur rangkuman materi agar lebih sistematis.
- Menjelaskan kembali istilah ekonomi cloud dengan bahasa yang lebih mudah dipahami.
- Menyusun tabel perbandingan CAPEX dan OPEX.
- Menuliskan kembali contoh perhitungan biaya selama lima tahun.
- Menyusun kesimpulan dan dokumentasi penggunaan AI.

### Bagian yang Diperiksa dan Disesuaikan

- Memeriksa kesesuaian rangkuman dengan PDF perkuliahan.
- Memeriksa kembali angka dan hasil perhitungan studi kasus.
- Menyesuaikan istilah teknis agar tetap sesuai dengan materi dosen.
- Membaca kembali hasil rangkuman sebelum dipublikasikan ke GitHub.

## 12. Sumber Materi

- File perkuliahan: **04--business-cloud-design.pdf**
- Mata Kuliah: Business Cloud Design
- Dosen: Dr. Bambang Purnomosidi D. P.
- Program Studi: Sistem Informasi
- Universitas Teknologi Digital Indonesia (UTDI)

### Referensi Lanjutan dalam Materi

- National Institute of Standards and Technology (NIST). *The NIST Definition of Cloud Computing*, SP 800-145 (2011).
- FinOps Foundation. *FinOps Framework – Principles, Capabilities, and Unit Economics*.
- Amazon Web Services. *Cloud Financial Management / AWS Well-Architected Framework – Cost Optimization Pillar*.
- Microsoft Azure. *Cloud Adoption Framework – Cloud Economics and Cost Management*.
