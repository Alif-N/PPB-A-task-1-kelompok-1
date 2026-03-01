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
