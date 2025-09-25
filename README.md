# CRUD dengan Java Form dan Java Dialog
Pada praktikum ke 6 ini dapat mengimplementasikan operasi CRUD (Create, Read, Update, Delete) dengan memanfaatkan Java Swing sebagai antarmuka grafis dan JDBC untuk terhubung ke database PostgreSQL. Desain aplikasi dipisahkan antara JFrame sebagai form utama untuk menampilkan data sekaligus navigasi, serta JDialog yang digunakan untuk proses input, pembaruan, dan konfirmasi penghapusan data.

# 1. CRUD menggunakan Java Form
   
CRUD  (Create, Read, Update, Delete) adalah operasi dasar pada basis data. Dalam Java, implementasinya dilakukan dengan Java Swing sebagai GUI dan JDBC untuk koneksi database (misalnya PostgreSQL), dengan pemisahan peran antara JFrame Form sebagai tampilan utama dan JDialog untuk input atau konfirmasi

# Implementasi CRUD :
- Create (Tambah Data) : 
Menekan tombol Insert pada Form utama akan memunculkan JDialog untuk memasukkan data baru. Setelah disimpan, data dikirim ke database menggunakan perintah INSERT.
- Read (Lihat Data) : 
Form utama menampilkan isi tabel database melalui JTable. Data diambil dengan query SELECT yang diproses menggunakan ResultSet dan DefaultTableModel.
- Update (Perbarui Data) : 
Ketika tombol Update ditekan, JDialog terbuka dengan field yang sudah berisi data lama. Setelah dilakukan perubahan dan disimpan, sistem menjalankan query UPDATE.
- Delete (Hapus Data) : 
Menekan tombol Delete akan menampilkan dialog konfirmasi. Jika pengguna menyetujui, data diproses dengan query DELETE dan dihapus dari database.

# Alur Penggunaan CRUD :
- Insert :<br>
Klik tombol Insert → dialog input muncul → data disimpan → data baru masuk ke tabel + database.
- Update (tanpa memilih data) : 
Klik tombol Update → tidak ada baris dipilih → muncul pesan peringatan.
- Update (dengan memilih data) : 
Klik tombol Update → baris data dipilih → dialog edit terbuka dengan data lama → data disimpan → pesan “Data berhasil diperbarui!” tampil.
- Delete (tanpa memilih data) : 
Klik tombol Delete → tidak ada baris dipilih → muncul pesan peringatan.
- Delete (dengan memilih data) : 
Klik tombol Delete → baris data dipilih → dialog konfirmasi tampil → pilih Yes → data terhapus dari tabel + database.
