# Catatan referensi — landing page antarkitaindonesia.com

Riset 15 Sep 2026 (WebFetch; halaman Shopee Food dan gojek.com/gopartner tidak dapat diambil — SPA/404, dilewati).

1. **gojek.com** — hero tagline + mockup ponsel, produk dikelompokkan (Transport & Logistics / Food & Groceries), tiga kartu "bergabung" (karyawan/driver/merchant), CTA unduh di bawah, footer legal. *Diadopsi:* hero dengan mockup ponsel, blok CTA unduh terpisah menjelang footer, footer 4 kolom (Aplikasi/Legal/Kontak).
2. **grab.com/id** — CTA ganda di hero ("Tentang Kami" / "Unduh Aplikasi"), grid layanan per kategori, tab audiens (Konsumen/Driver/Merchant/Enterprise), tombol unduh Play/App Store di footer. *Diadopsi:* dua CTA di hero (Pelanggan / Mitra), strip nama layanan di bawah hero.
3. **grab.com/id/driver** — manfaat mitra (pendaftaran cepat, pencairan, asuransi), langkah pendaftaran, syarat dokumen (KTP, SIM, rekening, STNK), FAQ khusus mitra. *Diadopsi:* bagian "Untuk Mitra" dengan daftar manfaat bercentang, kalimat syarat (usia ≥18, KTP, dokumen), FAQ syarat mitra.
4. **indrive.com/id-id** — headline nilai utama ("tarif adil"), kartu layanan masing-masing dengan CTA penumpang *dan* driver, bagian keamanan khusus, daftar kota, footer memuat tautan **hapus akun**. *Diadopsi:* bagian "Aman & transparan" berdiri sendiri, tautan Permintaan hapus akun di footer, cakupan wilayah disebut jujur (Pekanbaru, Riau).
5. **bolt.eu** — grid 6 layanan bergambar/berikon, bagian "cara menghasilkan" 4 jalur (driver/kurir/merchant/fleet) masing-masing dengan CTA, blok unduh dengan mockup ponsel, footer multi-kolom. *Diadopsi:* grid layanan berikon (9 kartu SVG inline), 4 kartu peran mitra (driver, merchant, pedagang pasar, travel).
6. **taximaxim.com/id** — hero "Order perjalanan" dengan tombol toko aplikasi berjajar, menu "Untuk pengemudi / Menjadi mitra", tautan "Setiap perjalanan Anda terlindungi", footer legal + privasi. *Diadopsi:* tiga opsi unduh berjajar (Web app / APK / Google Play), item menu "Mitra" di navbar, pesan perlindungan perjalanan di bagian keamanan.
7. **Pola umum yang diadopsi dari semuanya:** hero → layanan → cara kerja 3 langkah (gaya Grab/Bolt) → mitra → keamanan → dompet → FAQ → CTA unduh → footer legal; navbar lengket dengan satu CTA utama; tombol toko yang belum tersedia ditandai "Segera" tanpa tautan palsu.
8. **Yang sengaja tidak ditiru:** angka pengguna/mitra/kota (Gojek/Grab), klaim "terbaik/#1", carousel berita, pinjaman (inDrive) — tidak sesuai kebijakan konten AntarKita dan belum ada datanya.
9. **Konten & nada bahasa** diambil dari `docs/rilis/PLAY-STORE-LISTING.md` (deskripsi Pelanggan & Mitra, fitur keamanan, AntarPay/Midtrans, syarat mitra); nama layanan resmi dipakai apa adanya.
10. **Aset:** logo `apps/pelanggan/assets/logo.svg`, ikon 1024px → favicon/apple-touch-icon, screenshot mentah `docs/rilis/aset/screenshot/mentah/*.png` (412×892@3x) → WebP lebar 560 px (18–46 KB per gambar), OG image 1200×630 dipotong dari `feature-graphic-pelanggan.png`.

## Asumsi yang ditandai di HTML (`[ASUMSI]`)
- Cakupan wilayah: "Mulai dari Pekanbaru, Riau · hadir bertahap di kota-kota Sumatra" (pill hero dan jawaban FAQ pertama). Perbarui saat kota baru resmi dibuka.
- Google Play: dinyatakan "sedang disiapkan", tombol nonaktif (`aria-disabled`), tanpa tautan.
- Alamat usaha ditampilkan persis "Kahuripan Terrace VII-21" (footer + JSON-LD `address.streetAddress`) — kota/kode pos belum dikonfirmasi pemilik, sengaja tidak ditambahkan.
- Jam layanan CS "Setiap hari 07.00–22.00 WIB" (footer + FAQ "Bagaimana menghubungi CS?") — belum dikonfirmasi; ganti bila berbeda. Nomor WA/CS resmi 0811-7805-600 (wa.me/628117805600) sudah terkonfirmasi.
- Screenshot yang dipakai adalah tangkapan build web dengan data tiruan (lihat catatan di PLAY-STORE-LISTING.md §7); ganti dengan tangkapan HP asli sebelum rilis produksi bila diinginkan.

## Catatan deploy
- Halaman + aset ≈ 400 KB (index.html 54 KB, 8 WebP + ikon + OG ≈ 345 KB). `landing-desktop.png` dan `landing-mobile.png` hanya preview — tidak perlu ikut di-push.
- Font Inter dimuat dari Google Fonts; fallback system-ui/Arial disediakan bila diblokir.
- `CNAME` = `antarkitaindonesia.com`; aktifkan *Enforce HTTPS* di GitHub Pages setelah DNS (A/ALIAS apex) mengarah ke GitHub.
