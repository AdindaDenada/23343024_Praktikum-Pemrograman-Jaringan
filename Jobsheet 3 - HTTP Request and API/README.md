# Jobsheet 3 – Integrasi HTTP Request & API

Melalui modul praktikum ini, saya telah mendalami mekanisme **HTTP Request** serta implementasi **API (Application Programming Interface)** sebagai jembatan komunikasi antara aplikasi dan layanan pihak ketiga. Fokus utama pembelajaran ini adalah memahami siklus permintaan (*request*) dan jawaban (*response*) dalam protokol HTTP, serta teknik konsumsi data eksternal menggunakan ekosistem Node.js.

## Rincian Aktivitas Latihan

Secara bertahap, saya telah menyelesaikan tahapan berikut:

1. **Pendalaman Protokol HTTP:** Mempelajari ragam metode komunikasi seperti `GET`, `POST`, `PUT`, dan `DELETE`, serta membedah struktur anatomi *header* dan *body* pada pesan HTTP.
2. **Eksplorasi Arsitektur API:** Memahami pola interaksi *request-response*, pengolahan struktur data **JSON**, serta prosedur keamanan menggunakan kunci akses (*API/Access Key*).
3. **Pemanfaatan Weatherstack API:** Mengintegrasikan layanan cuaca untuk mengekstraksi data meteorologi terkini berdasarkan koordinat geografis (*latitude* dan *longitude*).
4. **Implementasi Geocoding dengan Mapbox API:** Menerapkan fitur *forward geocoding* guna mentransformasi nama lokasi atau alamat menjadi data koordinat yang presisi.
5. **Otomasi dengan Library `postman-request`:** Menggunakan modul Node.js ini untuk memicu permintaan HTTP secara programatik dan menangkap *payload* data hasil respons server.
6. **Formatting Output Terminal:** Menyajikan data mentah dari API (seperti temperatur, deskripsi cuaca, dan peluang presipitasi) menjadi informasi yang mudah dipahami melalui konsol terminal.
7. **Integrasi Multi-API (Chaining):** Menggabungkan layanan Mapbox dan Weatherstack dalam satu alur logika aplikasi agar sistem dapat menyajikan data cuaca yang relevan berdasarkan input lokasi pengguna.

## Kesimpulan

Praktikum ini memberikan pemahaman komprehensif mengenai efisiensi komunikasi **client-server** pada Node.js melalui **HTTP Request**. Saya telah berhasil menguasai teknik pemrosesan data **JSON**, manajemen autentikasi API, dan penyajian data dinamis. Hasil akhir dari latihan ini adalah sebuah aplikasi fungsional yang mampu melakukan automasi pencarian **informasi cuaca berdasarkan lokasi** secara *real-time*.