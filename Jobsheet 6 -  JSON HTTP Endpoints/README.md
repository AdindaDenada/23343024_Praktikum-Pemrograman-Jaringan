# Jobsheet 6 – Implementasi JSON HTTP Endpoints & Integrasi API

Melalui praktikum ini, saya telah mendalami teknik **pembangunan dan pengelolaan JSON HTTP Endpoints menggunakan Express.js**. Fokus utama pembelajaran ini meliputi pembuatan *endpoint* dinamis untuk pertukaran data berformat **JSON**, pemrosesan parameter melalui **query string (`req.query`)**, serta orkestrasi API eksternal (Mapbox dan Weatherstack) untuk menyajikan data cuaca secara *real-time*.

## Tahapan Latihan & Implementasi

Secara sistematis, saya telah menyelesaikan rangkaian instruksi berikut:

1. **Eksplorasi JSON HTTP Endpoints** — Memahami peran URL sebagai titik akses (*endpoint*) yang memfasilitasi pengiriman dan penerimaan data dalam format JSON melalui protokol HTTP.
2. **Ekstraksi Parameter URL (`req.query`)** — Mengimplementasikan pengambilan data dinamis dari URL (contoh: `?address=padang`) pada sisi Express.js untuk menghasilkan respons yang personal.
3. **Pengembangan Endpoint `/infoCuaca**` — Membangun logika *backend* yang mampu memberikan respons kondisional berdasarkan keberadaan atau validitas parameter alamat yang dikirimkan pengguna.
4. **Konektivitas API Eksternal** — Memanfaatkan modul `postman-request` sebagai *HTTP client* untuk menghubungkan server Node.js dengan layanan penyedia data pihak ketiga.
5. **Modularisasi Logika (Utilitas)** — Memisahkan fungsi-fungsi spesifik ke dalam modul terpisah guna menjaga keteraturan kode:
* `geocode.js`: Berinteraksi dengan **Mapbox API** untuk mentransformasi lokasi menjadi koordinat geografis.
* `prediksiCuaca.js`: Mengakses **Weatherstack API** untuk mengekstraksi informasi detail cuaca (suhu, visibilitas, indeks UV).


6. **Sinergi Modul pada `app.js**` — Mengintegrasikan seluruh modul utilitas agar aplikasi dapat menyajikan *payload* JSON yang komprehensif, mencakup narasi prediksi cuaca, nama lokasi resmi, dan input alamat asal.
7. **Integrasi Frontend dengan Fetch API** — Mengimplementasikan komunikasi asinkron pada file `index.hbs`. Dengan fitur ini, pengguna dapat melakukan pencarian tanpa perlu memuat ulang halaman (*refresh*).
8. **Estetika Antarmuka (CSS)** — Melakukan kustomisasi tampilan pada formulir input dan tombol pencarian, serta memastikan pesan status ditampilkan secara interaktif dan informatif.
9. **Validasi Input Sisi Klien** — Menerapkan logika pengecekan untuk memastikan pengguna tidak mengirimkan permintaan kosong, dengan memberikan peringatan: *"Kamu harus memasukkan lokasi yang ingin dicari"*.
10. **Optimalisasi Halaman Penunjang** — Melakukan pembaruan pada halaman *Help* dan *About* agar lebih relevan dan selaras dengan fungsi utama aplikasi.

---

## Kesimpulan

Praktikum ini memberikan pemahaman krusial bahwa **JSON HTTP Endpoints** adalah tulang punggung aplikasi web modern berbasis API. Saya telah berhasil menguasai alur kerja *full-stack* yang mencakup:

* Pemrosesan input pengguna melalui `req.query`.
* Interkoneksi *backend* dengan layanan API luar.
* Penyajian data dinamis ke *frontend* menggunakan **Fetch API**.
* Validasi data dan peningkatan pengalaman pengguna melalui desain UI yang responsif.

Hasil akhirnya adalah sebuah aplikasi pencarian cuaca yang fungsional, interaktif, dan memiliki struktur kode yang modular serta profesional.