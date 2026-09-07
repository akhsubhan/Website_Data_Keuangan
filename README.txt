WEBSITE DATA KEUANGAN V3

Versi ini menambahkan:
- Halaman awal wajib login / buat akun.
- Akun email + password menggunakan Supabase Auth.
- Data transaksi, catatan, kategori, pengaturan, dan kebutuhan bulanan tersimpan per akun di Supabase.
- Pengingat kebutuhan inti bulanan tanpa kategori: pengguna bisa menambah, mencentang selesai per bulan, dan menghapus.
- Footer bantuan: DM Instagram, YouTube, email, dan link pusat bantuan opsional.
- Tetap bisa di-host gratis di GitHub Pages.
- Backup JSON dan CSV.

SETUP SUPABASE
1. Buat project di Supabase.
2. Buka SQL Editor.
3. Jalankan seluruh isi file schema.sql.
4. Buka Project Settings > API.
5. Salin Project URL dan Publishable/Anon Key ke supabase-config.js.
6. Untuk akun email, buka Authentication > Providers > Email dan atur verifikasi email sesuai kebutuhanmu.
7. Jika memakai verifikasi email, masukkan URL GitHub Pages kamu ke Authentication > URL Configuration sebagai Site URL / Redirect URL yang sesuai.

PENTING
- Jangan pernah memasukkan service_role key ke website.
- Publishable/anon key memang digunakan oleh aplikasi browser; keamanan data bergantung pada Row Level Security (RLS).
- Jalankan schema.sql agar RLS aktif.
- GitHub Pages hanya menjadi hosting file HTML/CSS/JS. Database dan login ditangani Supabase.

GITHUB PAGES
- Upload isi folder Data-Keuangan ke repository.
- Aktifkan Settings > Pages > Deploy from a branch.
- Pilih branch utama dan folder root.
- Website akan mendapat alamat github.io.

MIGRASI V2
Saat pertama kali login pada browser yang masih memiliki data V2 lokal, V3 akan mencoba mengunggah data lokal tersebut jika akun cloud belum mempunyai data.


V5 PERUBAHAN
- Catatan sekarang punya halaman khusus "Catatan" dan semua catatan tersimpan ditampilkan di sana.
- Catatan singkat dari Beranda ikut masuk ke arsip Catatan setelah disimpan.
- Kebutuhan bulanan dipisahkan menjadi halaman sendiri.
- Kontak Pribadi memakai kolom tetap: Nama, No. HP, WhatsApp, Email pribadi, Instagram. Kolom tidak dapat ditambah, tetapi isinya dapat diedit.
- Kontak bantuan resmi website tetap dan tidak dapat diedit pengguna.
- Mukafaah 💰 tetap menjadi kategori pemasukan saja.
- Tidak perlu membuat project Supabase baru; payload JSONB lama tetap kompatibel.
