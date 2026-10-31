# Riset Konsep Website Toko Perhiasan — Toko Mas Berkah

Tanggal riset: 31 Oktober 2026.

## Rekomendasi konsep

Untuk kebutuhan Toko Mas Berkah saat ini, konsep yang paling tepat adalah **premium jewelry brand + multi-branch store locator**. Website tidak perlu langsung menjadi toko online penuh karena fokus saat ini adalah memperkenalkan jaringan, menampilkan kategori produk, membangun kepercayaan, dan membantu pelanggan menemukan cabang yang tepat.

## Dasar riset UX industri perhiasan

Baymard Institute melakukan riset UX khusus Jewelry & Watches dan melaporkan 470+ panduan UX, 4.400+ skor kinerja UX, serta 3.900+ contoh praktik terbaik. Ruang lingkup penelitiannya meliputi bagaimana produk divisualkan, interaksi gambar, variasi produk, ukuran/fit, navigasi kategori, pencarian, daftar produk, halaman produk, dan proses purna-jual. Benchmark 2025 yang diumumkan 2 September 2025 membandingkan tujuh situs perhiasan/jam tangan melalui lebih dari 470 parameter riset. Sumber: https://baymard.com/research/jewelry-and-watches dan https://baymard.com/research-articles/jewelry-and-watches-2025-benchmark

## Prinsip desain yang direkomendasikan

1. **Brand-led homepage.** Perkenalkan logo, nama, positioning, dan karakter jaringan terlebih dahulu. Store locator menjadi fitur utama berikutnya, bukan headline pembuka yang menenggelamkan identitas merek.
2. **Fotografi produk sebagai pusat katalog.** Gunakan gambar produk yang tajam, konsisten, cukup besar, dan memiliki crop seragam. Bila stok foto sendiri tersedia, prioritaskan foto asli perhiasan di toko. Foto ilustrasi harus diberi keterangan bahwa gambar bersifat ilustrasi.
3. **Kategori jelas.** Pisahkan Cincin, Gelang, Kalung, Liontin, Anting, Giwang, Logam Mulia, serta layanan Jual Beli dan Konsultasi. Jangan membuat halaman detail produk atau harga sampai katalog, berat, kadar, variasi, dan stok dapat dipastikan.
4. **Detail dan kepercayaan.** Ketika katalog produk asli sudah siap, tampilkan detail yang relevan seperti kadar/finishing, berat atau rentang berat bila tersedia, ukuran, foto dari beberapa sudut, dan keterangan stok per cabang. Jangan mengarang spesifikasi.
5. **Navigasi lokal yang mudah.** Jaga pencarian cabang, filter wilayah, alamat, WhatsApp, dan tautan Maps tetap dekat dengan kebutuhan pelanggan. Informasi tiap cabang harus mudah diverifikasi.
6. **Ulasan per cabang.** Tampilkan rating dan jumlah ulasan bersama tautan profil cabang. Hindari menggabungkan rating menjadi satu angka jaringan kecuali metode agregasinya jelas dan listing yang dihitung terverifikasi.
7. **Mobile-first.** Pastikan foto, filter, kartu cabang, dan tombol dapat digunakan dengan jempol; teks utama nyaman dibaca; tombol interaktif memiliki area sentuh memadai.
8. **Tipografi berhierarki.** Gunakan Cormorant Garamond untuk heading editorial yang elegan dan Plus Jakarta Sans untuk teks isi, navigasi, data cabang, tombol, serta filter. Skala teks memakai CSS `clamp()` agar beradaptasi dengan lebar layar.

## Sistem visual yang dipakai dalam proyek

- **Heading:** Cormorant Garamond, untuk kesan editorial, elegan, dan berkarakter.
- **Body/UI:** Plus Jakarta Sans, untuk keterbacaan paragraf, label, navigasi, filter, dan informasi cabang.
- **Palet:** merah identitas sebagai aksen utama, putih/krem untuk ruang, hitam/arang untuk kontras, dan emas sebagai aksen perhiasan. Jangan gunakan emas pada teks kecil dengan kontras rendah.
- **Tata letak:** grid foto di desktop, grid dua kolom di tablet, dan satu kolom untuk kartu rating/daftar panjang pada ponsel sempit.
- **Animasi:** hover/reveal yang lembut saja; hormati `prefers-reduced-motion` dan jangan mengandalkan animasi untuk menyampaikan informasi.

## Rating Google Maps dalam versi ini

Bagian `Ulasan pelanggan` menampilkan rating dan jumlah ulasan dari 14 listing publik yang berhasil dicocokkan berdasarkan nama, area, dan/atau nomor telepon cabang. Snapshot diperiksa pada 31 Oktober 2026 dan berjumlah 1.975 ulasan jika seluruh 14 listing dijumlahkan. Angka dapat berubah. Satu profil publik di Lembang menyatukan nama Berkah Baru 1/2, sehingga tidak diperlakukan sebagai dua rating terpisah.

Website menampilkan rating, bintang, jumlah ulasan, wilayah, dan tautan untuk membuka foto serta ulasan aktual di Google Maps. Isi review dan foto profil pelanggan tidak disalin ke website karena hasil listing yang tersedia tidak memberikan data author attribution, foto profil, dan tautan review per-item yang lengkap.

## Ketentuan Google Places API untuk fase berikutnya

Dokumentasi Google Places API (New) menyebut Place Details dapat mengembalikan maksimum lima review dan sepuluh foto untuk satu place. Data review memiliki author attribution dan tautan Google Maps; foto juga memiliki author attribution. Google meminta atribusi penulis untuk review/foto yang ditampilkan, serta akses/tautan menuju sumber Google Maps. Terdapat juga batasan penggunaan, caching, dan penyimpanan data Places. Sumber: https://developers.google.com/maps/documentation/places/web-service/reference/rest/v1/places dan https://developers.google.com/maps/documentation/places/web-service/policies

Karena website ini belum memiliki integrasi Places API dan API key yang dikelola pemilik domain, versi ini tidak mengunduh atau menyimpan foto/kutipan review pelanggan. Bila ingin menampilkan review dan foto langsung di website, fase berikutnya harus mengimplementasikan Places API, pengamanan API key, billing, atribusi, dan pemenuhan kebijakan Google.

## Pemetaan data rating (snapshot)

| Cabang | Wilayah | Rating | Jumlah ulasan | Ref pencocokan |
|---|---|---:|---:|---|
| Berkah A | Ujungberung | 4.4/5 | 66 | turn802965business11 |
| Berkah C | Ujungberung | 5.0/5 | 966 | turn802965business0 |
| Berkah D | Ujungberung | 4.5/5 | 178 | turn802965business5 |
| Berkah Baru · Lembang | Lembang | 4.8/5 | 71 | turn802965business8 |
| Berkah Umat | Soreang | 4.8/5 | 333 | turn802965business3 |
| Berkah Umat 2 | Soreang | 4.8/5 | 28 | turn482016business3 |
| Berkah Muda 2 | Soreang | 4.9/5 | 28 | turn802965business2 |
| Berkah Muda 1 | Banjaran | 4.7/5 | 66 | turn802965business7 |
| Duta 1 Sumedang | Sumedang | 4.5/5 | 87 | turn348835business11 |
| Zahra 1 | Tasikmalaya | 4.8/5 | 42 | turn348835business1 |
| Zahra 2 | Tasikmalaya | 4.9/5 | 19 | turn348835business4 |
| Berkah Muda | Buah Batu | 4.6/5 | 30 | turn348835business0 |
| Berkah Baru | Padalarang | 4.6/5 | 10 | turn482016business0 |
| Berkah Baru | Ciwidey | 5.0/5 | 51 | turn482016business1 |

17 dari 31 entri toko belum memiliki listing rating publik yang dapat dicocokkan dengan keyakinan yang memadai. Angka rating bukan verifikasi kualitas produk/layanan dan bukan jaminan pengalaman yang sama di setiap cabang.
