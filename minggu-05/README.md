# Minggu 05 – Metode Kuantitatif Ekonomi Infrastruktur untuk Deployment Cloud

## 1. Pendahuluan

Materi minggu kelima mata kuliah Business Cloud Design membahas metode kuantitatif untuk menganalisis ekonomi infrastruktur dalam penerapan cloud. Pembahasan berfokus pada bagaimana organisasi menghitung biaya, mengukur manfaat investasi, serta membandingkan pilihan deployment private cloud dan public cloud.

Keputusan infrastruktur tidak hanya didasarkan pada biaya pembelian perangkat atau harga layanan cloud. Organisasi perlu mempertimbangkan biaya langsung, biaya tidak langsung, biaya transisi, risiko, serta manfaat finansial yang dihasilkan.

Tujuan akhirnya bukan sekadar memilih alternatif dengan biaya paling rendah, tetapi menentukan pilihan yang memberikan nilai bisnis terbaik sesuai kebutuhan organisasi.

## 2. Capaian Pembelajaran

Setelah mempelajari materi ini, mahasiswa diharapkan mampu:

1. Menjelaskan pentingnya analisis kuantitatif ekonomi infrastruktur untuk deployment cloud.
2. Mengidentifikasi biaya langsung, tidak langsung, transisi, dan risiko.
3. Menghitung TCO, ROI sederhana, dan Payback Period serta memahami batasannya.
4. Membandingkan private cloud dan public cloud berdasarkan asumsi yang setara.
5. Menyusun rekomendasi dengan mempertimbangkan sensitivitas dan faktor nonfinansial.

## 3. Mengapa Analisis Ekonomi Infrastruktur Penting?

Infrastruktur TI merupakan keputusan investasi sekaligus keputusan operasional. Organisasi harus mengetahui berapa biaya yang dibutuhkan, manfaat apa yang diperoleh, dan kapan manfaat tersebut dapat menutup investasi.

Terdapat dua jenis biaya yang perlu diperhatikan:

- **Biaya terlihat:** server, storage, jaringan, lisensi, listrik, dan layanan cloud.
- **Biaya tersembunyi:** tenaga ahli, downtime, migrasi, keamanan, pelatihan, serta biaya yang muncul ketika berpindah dari satu vendor ke vendor lain.

Dengan analisis ekonomi, organisasi dapat membuat keputusan berdasarkan perhitungan dan asumsi yang lebih terukur.

## 4. Metode Kuantitatif yang Digunakan

### 4.1 Analisis Biaya Manfaat (Cost Benefit Analysis)

Cost Benefit Analysis merupakan metode untuk membandingkan biaya yang dikeluarkan dengan manfaat yang diperoleh dari suatu investasi.

Dalam konteks cloud, analisis ini mempertimbangkan CAPEX, OPEX, total biaya, dan manfaat yang dihasilkan selama periode tertentu.

### 4.2 TCO (Total Cost of Ownership)

TCO adalah keseluruhan biaya untuk memperoleh, mengoperasikan, dan mengakhiri penggunaan suatu solusi atau infrastruktur.

Rumus:

**TCO = Biaya Awal + Biaya Operasional + Biaya Transisi + Biaya Risiko/Keluar**

TCO digunakan untuk mengetahui keseluruhan biaya selama periode analisis, bukan hanya biaya pembelian awal.

### 4.3 ROI (Return on Investment)

ROI merupakan metrik keuangan untuk mengukur tingkat pengembalian atau keuntungan suatu investasi dibandingkan dengan biaya yang telah dikeluarkan.

Rumus ROI sederhana:

**ROI (%) = ((Manfaat Finansial Total − Biaya Total) ÷ Biaya Total) × 100%**

ROI membantu organisasi melihat seberapa besar manfaat finansial dibandingkan dengan biaya investasi.

### 4.4 Payback Period

Payback Period merupakan metode untuk mengukur waktu yang dibutuhkan agar investasi awal dapat kembali melalui arus kas bersih atau manfaat yang dihasilkan.

Rumus sederhana:

**Payback Period = Investasi Awal ÷ Manfaat Bersih per Tahun**

Semakin pendek periode pengembalian, semakin cepat investasi awal tertutup berdasarkan asumsi perhitungan tersebut.

### 4.5 NPV (Net Present Value)

NPV merupakan metode analisis keuangan untuk mengukur kelayakan suatu proyek dengan memperhitungkan nilai waktu uang (*time value of money*).

Uang yang diterima saat ini memiliki nilai lebih tinggi dibandingkan jumlah uang yang sama di masa depan.

Secara umum:

**NPV = Nilai Sekarang Arus Kas Masuk − Nilai Sekarang Arus Kas Keluar**

NPV membantu membandingkan arus kas yang terjadi pada waktu berbeda.

### 4.6 Analisis Sensitivitas

Analisis sensitivitas digunakan untuk menguji bagaimana perubahan asumsi tertentu memengaruhi hasil perhitungan ekonomi.

Contohnya perubahan biaya operasi, pertumbuhan data, utilisasi, biaya transfer data, dan harga layanan cloud.

ROI mudah dikomunikasikan, tetapi tidak menunjukkan kapan arus kas terjadi. NPV lebih tepat untuk membandingkan arus kas pada waktu berbeda.

## 5. Komponen Biaya Infrastruktur

Dalam membuat model ekonomi infrastruktur, terdapat enam kelompok biaya yang perlu diperhatikan.

| Komponen | Contoh |
|---|---|
| CAPEX | Server, storage, jaringan, rak, UPS, fasilitas, dan implementasi. |
| OPEX | Listrik, pendinginan, konektivitas, penggunaan cloud, dukungan, lisensi, backup, dan monitoring. |
| People Cost | Administrasi sistem, keamanan, database, platform engineering, pelatihan, dan staf operasional. |
| Transition Cost | Assessment, migrasi, pengujian, parallel run, dan perubahan proses. |
| Risk Cost | Downtime, kehilangan data, insiden keamanan, over-provisioning, dan ketidakpastian harga. |
| Exit Cost | Pemindahan data, penghapusan data secara aman, terminasi kontrak, dan biaya egress. |

Egress merupakan proses keluarnya data dari sistem cloud ke luar, misalnya mengunduh file, menampilkan gambar, memberikan respons API, atau melakukan sinkronisasi data ke server lokal. Biaya egress dapat dikenakan berdasarkan jumlah data yang ditransfer.

## 6. Langkah Membuat Model Ekonomi

Untuk membuat model ekonomi infrastruktur, organisasi dapat mengikuti beberapa langkah berikut:

1. **Menetapkan ruang lingkup:** menentukan workload, SLA, lokasi, kapasitas, keamanan, dan periode analisis.
2. **Menetapkan baseline:** menyamakan kapasitas, performa, ketersediaan, backup, dan pertumbuhan.
3. **Memisahkan biaya:** membedakan biaya satu kali dan biaya berulang serta menetapkan pemilik setiap asumsi.
4. **Memproyeksikan biaya:** menghitung biaya per tahun, bukan hanya menggunakan satu angka bulanan.
5. **Menghitung TCO dan manfaat:** menghindari perhitungan manfaat yang sama lebih dari satu kali.
6. **Menguji skenario:** menggunakan skenario rendah, dasar, dan tinggi serta mendokumentasikan sumber asumsi.

Dalam perbandingan, kedua alternatif harus memiliki horizon waktu dan cakupan layanan yang sama. Asumsi pertumbuhan dan utilisasi juga harus dinyatakan secara jelas.

## 7. Studi Kasus: Layanan Bisnis Selama Tiga Tahun

Materi memberikan simulasi organisasi yang menjalankan tiga jenis layanan, yaitu:

- ERP (Enterprise Resource Planning).
- Portal pelanggan.
- Analitik internal.

Periode analisis adalah tiga tahun dengan kapasitas yang setara. Manfaat finansial yang digunakan dalam simulasi sebesar Rp1,2 miliar per tahun.

Manfaat tersebut berasal dari pengurangan downtime, otomatisasi pekerjaan, dan percepatan proses. Angka ini merupakan asumsi ilustratif dan harus divalidasi oleh pemilik proses bisnis. Penghematan waktu tidak otomatis sama dengan penghematan kas.

### 7.1 Input Biaya

Seluruh angka berikut menggunakan satuan Rp juta.

| Komponen | Private Cloud | Public Cloud |
|---|---:|---:|
| Investasi awal | 1.200 | 100 |
| Operasi infrastruktur per tahun | 300 | 480 |
| Tenaga ahli per tahun | 250 | 150 |
| Migrasi dan transisi (sekali) | 150 | 200 |
| Biaya keluar/egress di akhir periode | 0 | 80 |

Biaya tahunan diasumsikan konstan selama tiga tahun.

### 7.2 Perhitungan TCO Tiga Tahun

**A. Private Cloud**

Rumus:

Investasi awal + (Operasi infrastruktur × 3) + (Tenaga ahli × 3) + Migrasi

Perhitungan:

1.200 + (300 × 3) + (250 × 3) + 150

= 1.200 + 900 + 750 + 150

= **Rp3.000 juta atau Rp3 miliar**

**B. Public Cloud**

Rumus:

Investasi awal + (Operasi infrastruktur × 3) + (Tenaga ahli × 3) + Migrasi + Egress

Perhitungan:

100 + (480 × 3) + (150 × 3) + 200 + 80

= 100 + 1.440 + 450 + 200 + 80

= **Rp2.270 juta atau Rp2,27 miliar**

### 7.3 Analisis Hasil TCO

| Alternatif | TCO 3 Tahun |
|---|---:|
| Private Cloud | Rp3.000 juta |
| Public Cloud | Rp2.270 juta |

Selisih biaya:

Rp3.000 juta − Rp2.270 juta = **Rp730 juta**

Persentase selisih terhadap biaya private cloud:

(Rp730 juta ÷ Rp3.000 juta) × 100% = **24,3%**

Berdasarkan asumsi dasar dalam simulasi, public cloud memiliki biaya total tiga tahun lebih rendah sebesar Rp730 juta atau sekitar 24,3% dibandingkan private cloud.

## 8. Perhitungan ROI Sederhana

Manfaat finansial kumulatif selama tiga tahun:

Rp1.200 juta × 3 = **Rp3.600 juta**

### 8.1 ROI Private Cloud

Rumus:

ROI = ((Manfaat − Biaya Total) ÷ Biaya Total) × 100%

Perhitungan:

((3.600 − 3.000) ÷ 3.000) × 100%

= **20,0%**

### 8.2 ROI Public Cloud

Perhitungan:

((3.600 − 2.270) ÷ 2.270) × 100%

= **58,6%**

### 8.3 Analisis Hasil ROI

| Alternatif | Manfaat Finansial | TCO | ROI |
|---|---:|---:|---:|
| Private Cloud | Rp3.600 juta | Rp3.000 juta | 20,0% |
| Public Cloud | Rp3.600 juta | Rp2.270 juta | 58,6% |

Berdasarkan perhitungan tersebut, public cloud menghasilkan ROI lebih tinggi dibandingkan private cloud.

Namun, hasil ini bergantung pada validitas manfaat finansial, utilisasi, biaya tenaga ahli, dan biaya transfer data.

Catatan: perhitungan tersebut menggunakan ROI sederhana tanpa diskonto. Hasilnya bukan pengganti NPV atau analisis risiko.

## 9. Perhitungan Payback Period

Payback Period digunakan untuk mengetahui waktu yang dibutuhkan agar investasi awal kembali.

### 9.1 Private Cloud

Investasi awal dan biaya transisi:

Rp1.200 juta + Rp150 juta = Rp1.350 juta

Manfaat bersih tahunan:

Rp1.200 juta − (Rp300 juta + Rp250 juta)

= Rp650 juta

Payback:

Rp1.350 juta ÷ Rp650 juta

= **2,08 tahun**

### 9.2 Public Cloud

Investasi awal dan biaya transisi:

Rp100 juta + Rp200 juta = Rp300 juta

Manfaat bersih tahunan:

Rp1.200 juta − (Rp480 juta + Rp150 juta)

= Rp570 juta

Payback:

Rp300 juta ÷ Rp570 juta

= **0,53 tahun**

### 9.3 Analisis Hasil Payback

| Alternatif | Investasi Awal dan Transisi | Manfaat Bersih per Tahun | Payback |
|---|---:|---:|---:|
| Private Cloud | Rp1.350 juta | Rp650 juta | 2,08 tahun |
| Public Cloud | Rp300 juta | Rp570 juta | 0,53 tahun |

Berdasarkan simulasi, public cloud memiliki periode pengembalian investasi yang lebih singkat.

Perhitungan ini masih sederhana karena belum memodelkan biaya akhir, perubahan kapasitas, pajak, diskonto, dan manfaat yang diterima secara bertahap.

## 10. Analisis Sensitivitas

Analisis sensitivitas dilakukan untuk menguji apakah perubahan asumsi dapat memengaruhi hasil keputusan.

Dalam materi, diberikan contoh jika biaya operasi public cloud meningkat sebesar 30%.

Biaya operasi awal:

Rp480 juta per tahun.

Setelah kenaikan 30%:

Rp480 juta × 130% = Rp624 juta per tahun.

Tambahan biaya selama tiga tahun:

(Rp624 juta − Rp480 juta) × 3

= Rp144 juta × 3

= Rp432 juta.

TCO public cloud setelah kenaikan:

Rp2.270 juta + Rp432 juta

= **Rp2.702 juta**

Perbandingan baru:

- Private cloud: Rp3.000 juta.
- Public cloud: Rp2.702 juta.
- Selisih: Rp298 juta.

Meskipun biaya operasi public cloud meningkat 30%, berdasarkan simulasi public cloud masih memiliki TCO lebih rendah daripada private cloud. Namun, selisih biayanya menjadi lebih kecil.

Faktor lain yang perlu diuji meliputi:

- Pertumbuhan data.
- Biaya egress.
- Penggunaan GPU.
- Lisensi.
- Nilai tukar mata uang.
- Biaya tenaga ahli.
- Utilisasi private cloud.

Analisis sebaiknya menggunakan skenario rendah, dasar, dan tinggi serta menghindari presisi semu.

## 11. Deployment: Private Cloud vs Public Cloud

### 11.1 Private Cloud

Private cloud merupakan lingkungan cloud yang didedikasikan untuk satu organisasi dan dapat dikelola oleh tim internal maupun penyedia layanan.

Karakteristiknya:

- Kontrol infrastruktur lebih langsung.
- Biaya awal cenderung tinggi.
- Biaya rutin relatif tetap.
- Kapasitas perlu direncanakan.
- Organisasi memiliki tanggung jawab operasional lebih besar.

### 11.2 Public Cloud

Public cloud merupakan layanan infrastruktur atau platform dari penyedia yang melayani banyak pelanggan dengan isolasi logis.

Karakteristiknya:

- Biaya awal cenderung lebih rendah.
- Biaya rutin mengikuti penggunaan.
- Kapasitas dapat ditambah atau dikurangi secara relatif cepat.
- Provisioning umumnya lebih cepat.
- Sebagian tanggung jawab infrastruktur dibagi dengan provider.

### 11.3 Perbandingan Karakteristik Deployment

| Dimensi | Private Cloud | Public Cloud |
|---|---|---|
| Biaya awal | Cenderung tinggi | Cenderung rendah |
| Biaya rutin | Lebih tetap | Variabel sesuai penggunaan |
| Skalabilitas | Dibatasi kapasitas yang disediakan | Elastis dan relatif cepat |
| Kontrol teknis | Lebih langsung | Melalui kontrol dan layanan provider |
| Provisioning | Bergantung otomatisasi dan proses | Umumnya cepat |
| Operasi | Lebih banyak pada organisasi | Berbagi dengan provider |
| Risiko utama | Overcapacity, refresh, dan skill | Cost sprawl, lock-in, dan egress |
| Cocok ketika | Kebutuhan stabil atau kontrol khusus | Beban berubah dan membutuhkan time-to-market cepat |

Perbandingan private dan public cloud bukan sekadar membandingkan server lokal dengan layanan internet. Private cloud juga dapat di-host oleh pihak ketiga.

Kedua model tetap membutuhkan desain identitas, jaringan, backup, observability, keamanan, dan tata kelola biaya.

## 12. Kerangka Keputusan Deployment

Dalam menentukan pilihan deployment, terdapat lima aspek utama yang perlu dipertimbangkan:

1. **Regulasi dan Data:** apakah terdapat batasan lokasi, isolasi, atau kontrol khusus terhadap data?
2. **Pola Beban:** apakah workload stabil dan dapat diprediksi atau sangat fluktuatif?
3. **Kapabilitas:** apakah tim organisasi mampu mengoperasikan platform selama 24 jam sehari dan 7 hari seminggu?
4. **Ekonomi:** bagaimana TCO selama tiga sampai lima tahun dan biaya ketika terjadi beban puncak?
5. **Strategi:** seberapa penting portabilitas dan upaya menghindari vendor lock-in?

Hasil analisis tidak harus selalu memilih private atau public cloud. Organisasi juga dapat menggunakan hybrid cloud atau membuat keputusan berbeda untuk setiap workload.

## 13. Kesimpulan

Metode kuantitatif ekonomi infrastruktur membantu organisasi menentukan pilihan deployment cloud berdasarkan perhitungan biaya dan manfaat yang lebih terukur.

Beberapa metode penting yang digunakan adalah TCO, ROI, Payback Period, NPV, dan analisis sensitivitas. Setiap metode memiliki fungsi berbeda dalam mengevaluasi investasi.

Berdasarkan studi kasus dalam materi, public cloud menghasilkan TCO sebesar Rp2.270 juta, ROI sebesar 58,6%, dan Payback Period sekitar 0,53 tahun. Sementara itu, private cloud menghasilkan TCO sebesar Rp3.000 juta, ROI sebesar 20%, dan Payback Period sekitar 2,08 tahun.

Hasil tersebut berlaku berdasarkan asumsi simulasi yang digunakan. Keputusan nyata tetap harus mempertimbangkan keamanan, regulasi, kemampuan tim, performa, pola penggunaan, dan kebutuhan bisnis. Tujuan utama analisis bukan sekadar memilih biaya terendah, melainkan memperoleh nilai bisnis terbaik.

## 14. Penggunaan AI

Dalam penyusunan rangkuman materi minggu kelima ini, saya menggunakan bantuan AI (ChatGPT) untuk membantu memahami, menyusun, dan merangkum materi dari file PDF perkuliahan.

### Prompt yang Digunakan

> Saya sedang mengerjakan tugas rangkuman mingguan mata kuliah Business Cloud Design. Bantu saya membuat rangkuman materi Minggu 05 berdasarkan file PDF yang saya berikan dengan judul Metode Kuantitatif Ekonomi Infrastruktur untuk Deployment Cloud. Susun rangkuman dalam format Markdown untuk README.md GitHub. Bahas capaian pembelajaran, analisis biaya manfaat, TCO, ROI, Payback Period, NPV, komponen biaya infrastruktur, langkah membuat model ekonomi, studi kasus private cloud dan public cloud, perhitungan TCO tiga tahun, ROI, Payback Period, analisis sensitivitas, perbandingan deployment, dan kerangka keputusan. Gunakan bahasa Indonesia yang jelas dan mudah dipahami. Pertahankan angka, rumus, dan hasil perhitungan sesuai PDF dosen. Jangan menambahkan asumsi angka yang tidak terdapat dalam materi. Sertakan tabel agar perbandingan lebih mudah dipahami.

### Bagian yang Dibantu AI

- Menyusun struktur rangkuman agar lebih sistematis.
- Menjelaskan kembali istilah ekonomi infrastruktur cloud.
- Menyusun tabel komponen biaya dan perbandingan deployment.
- Membantu menuliskan rumus serta tahapan perhitungan TCO, ROI, dan Payback Period.
- Menyusun kesimpulan dan dokumentasi penggunaan AI.

### Bagian yang Diperiksa dan Disesuaikan

- Memeriksa kembali angka dan hasil perhitungan berdasarkan PDF perkuliahan.
- Memastikan rumus yang digunakan sesuai dengan materi.
- Menyesuaikan istilah teknis agar mudah dipahami.
- Membaca kembali hasil rangkuman sebelum dipublikasikan ke GitHub.

## 15. Sumber Materi

- File perkuliahan: **05--business-cloud-design.pdf**
- Judul materi: Metode Kuantitatif Ekonomi Infrastruktur untuk Deployment Cloud.
- Mata Kuliah: Business Cloud Design.
- Dosen: Dr. Bambang Purnomosidi D. P.
- Program Studi: Sistem Informasi.
- Universitas Teknologi Digital Indonesia (UTDI).

### Referensi Lanjutan dalam Materi

- NIST SP 800-145 – *The NIST Definition of Cloud Computing*.
- FinOps Foundation – https://www.finops.org/
- AWS Cloud Financial Management – https://aws.amazon.com/aws-cost-management/
- Microsoft Cost Management – https://azure.microsoft.com/en-us/products/cost-management
- Google Cloud FinOps – https://cloud.google.com/learn/what-is-finops
- J. R. Storment dan Mike Fuller – *Cloud FinOps: Collaborative, Real-Time Cloud Value Decision Making*.
