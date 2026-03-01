# 2. Context Assumption

Dalam studi kasus aplikasi ini, saya mengasumsikan bahwa aplikasi WhatsApp
dikembangkan oleh sebuah perusahaan teknologi global berskala enterprise.

## Why Context Matters

Jika konteksnya startup kecil,
maka pilihan teknologinya mungkin berbeda.
Namun dalam konteks enterprise global,
prioritas utama adalah:

- Stability
- Efficiency
- Control
- Long-term sustainability

## Strategic Objective

Tujuan utama perusahaan dalam konteks ini adalah:
1. Reliability over speed of development
2. Performance over cost efficiency
3. Long-term maintainability
4. Security and privacy first
5. Scalability to hundreds of millions of users

Perusahaan ini memiliki:
- Jutaan hingga miliaran pengguna aktif
- Infrastruktur server terdistribusi secara global
- Tim engineering besar dan terstruktur
- Pengembangan jangka panjang

Dalam konteks bisnis, aplikasi ini bersifat mission-critical yang artinya:
- Digunakan untuk komunikasi pribadi dan bisnis
- Menangani data sensitif
- Harus selalu tersedia (ketersediaan tinggi / high availability)
- Tidak boleh sering crash
- Tidak boleh kehilangan data pesan
- Downtime sekecil apapun dapat berdampak besar terhadap reputasi dan kepercayaan pengguna.

Karakteristik produk aplikasi ini:
- Real-time messaging
- End-to-end encryption
- Background synchronization
- Media transfer (image, video, document)
- Voice & video call
- Push notification
- Offline message queue
- Memaksimalkan aplikasi dapat berjalan optimal pada segala spesifikasi perangkat

Lingkungan pengembangan dalam aplikasi ini:
- Tersedia pengembangan Android team tersendiri
- Tersedia pengembangan iOS team tersendiri
- DevOps dan Security team terpisah
- QA automation team, DLL

Karena resource tersedia, perusahaan dapat memilih solusi
yang memaksimalkan performa dan stabilitas,
meskipun biaya pengembangan lebih tinggi.

# 3. Penjelasan Constraints

## Budget
Salah satu keunggulan terbesar Flutter dalam konteks budget adalah kemampuannya untuk membangun aplikasi di dua platform sekaligus dari satu codebase. Dengan pendekatan ini, biaya development bisa dihemat sekitar 60 hingga 70 persen dibandingkan pendekatan native yang membutuhkan dua codebase terpisah untuk Android dan iOS. Estimasi biaya MVP dengan Flutter berkisar antara $150K hingga $600K, jauh lebih rendah dibandingkan pendekatan native terpisah yang bisa mencapai $500K hingga $2M atau lebih.

## Team Size
Dengan Flutter, ukuran tim yang dibutuhkan untuk membangun aplikasi sekelas WhatsApp bisa jauh lebih kecil dibandingkan pendekatan native. Secara minimum, dibutuhkan sekitar 7 hingga 10 orang, yang terdiri dari 4 sampai 5 Flutter developer untuk UI dan logika bisnis, 1 hingga 2 native specialist untuk menulis platform channel pada fitur yang memerlukan akses langsung ke OS seperti VoIP dan background service, serta 2 sampai 3 backend engineer. Sebagai perbandingan, pendekatan native terpisah membutuhkan 12 hingga 15 orang karena harus membagi tim menjadi tim iOS dan tim Android.

## Performance Needs
 Flutter menjawab tantangan ini dengan pendekatan AOT (Ahead-of-Time) compilation yang mengkompilasi Dart langsung ke kode native ARM, sehingga performa UI sangat mendekati native dengan konsistensi 60fps melalui engine rendering sendiri bernama Skia yang kini digantikan oleh Impeller.
<br>
Untuk fitur-fitur berat yang menjadi inti WhatsApp, Flutter menyediakan mekanisme yang memadai. Enkripsi end-to-end menggunakan Signal Protocol bisa diimplementasikan melalui dart:ffi yang memanggil library C/C++ secara langsung, sehingga berjalan pada kecepatan native tanpa melalui Dart murni.

## Long-Term Maintenance
Flutter memiliki keunggulan fundamental yaitu satu codebase. Ini berarti setiap bug fix hanya perlu ditulis sekali dan langsung berlaku untuk kedua platform. Tidak ada risiko bug yang muncul di Android tapi tidak di iOS, atau sebaliknya. Feature parity juga otomatis terjaga karena setiap fitur baru langsung tersedia di kedua platform secara bersamaan, tanpa ada lag rilis antar platform seperti yang sering terjadi pada pendekatan native. Hot reload mempercepat iterasi development secara signifikan, sementara Dart yang strongly-typed mampu menangkap bug sejak compile time, mengurangi runtime error dalam jangka panjang. Framework testing bawaan yang mencakup widget test, integration test, dan golden test juga memperkuat kualitas kode dari waktu ke waktu.

# 4. Chosen Approach
Menggunakan Flutter sebagai pendekatan dalam pengembangan aplikasi pesan instan seperti WhatsApp merupakan keputusan yang tepat, terutama jika tujuan utamanya adalah membangun sistem yang:
- Cepat dikembangkan
- Efisien secara biaya
- Mudah dipelihara
- Siap berkembang di masa depan

Berikut adalah keuntungan dari menggunakan flutter:
- Mempercepat Time-to-Market
- Konsistensi Antar Platform
- Cocok untuk Sistem Realtime
- Efisiensi Biaya Pengembangan
- Mendukung Arsitektur yang Bersih dan Skalabel
- Dukungan Multimedia yang Matang
- Cocok untuk MVP hingga Scaling
- Siap untuk Ekspansi Masa Depan
