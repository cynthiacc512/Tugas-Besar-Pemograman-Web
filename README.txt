username dan password:

Sebagai user (bisa register sendiri):
	email: user@gmail.com
	pass: 123

Sebagai admin:
	email: admin@toko.com
	pass: 123


Penjelasan sesuai job desc dari Cynthia Caroline:
1. Home: select data dari database menggunakan order by. Ada 2x select, select by rating(buku yang sedang trend) dan by harga (buku termurah). Jika kita ingin add buku to cart, ada 2 kemungkinan, jika belum login, maka akan diarahkan ke page login, jika sudah login, maka buku langung masuk ke cart.
2. AJAX XML (yang menggunakan xhttprequest): berguna untuk fitur searching buku. ini hanya mengambil dari database. code AJAX nya ada di index.php sedangkan code get seisi tabel database ada di autocomplete_search.php
3. Cart (bisa hapus buku): menampung buku yang ceritanya ingin dibeli. Untuk menampungnya menggunakan array, yang isinya adalah array lagi tentang data data bukunya, lalu dia akan dimerge pada buku yang akan dimasukan dicart. fungsinya agar data yg sudah ada di array sebelumnya bisa bergabung dg buku yang baru dimasukkan. Ada juga fitur jumlah buku yang akan dibeli, harga 1 buku dan total harga.

Perbaikan setelah presentasi dari Cynthia Caroline:
1. Home: Tulisan judul bukunya menjadi lebih besar.
2. Cart: Ada validasi jumlah, tetapi bukan mengurangi jumlah buku dari database (karena cart belum tentu jadi membeli, jadi jumlah buku di database tidak berkurang), hanya saja memvalidasi jumlah bukunya apakah cukup atau tidak jika dibeli dengan jumlah tertentu, jadi yang tampil di websitenya (page cart.php)  hanya jumlah buku yang bisa dibeli. Misalnya jumlah buku hanya ada 3, sedangkan menu option button di cart bisa sampai 5, tapi kan bukunya tidak cukup, jadi option button yang tampil hanya sampai 3.



Penjelasan sesuai job desc dari Yoel:
1. List Buku Sesuai Kategori(pakai sql WHERE) + Show Book(detail/deskripsi buku tersebut yang di click gambarnya). Diambil berdasarkan ID
2. Admin - bisa addBuku dan editBuku(DELETE atau UPDATE). Jika sudah addBuku automatis parsing data Buku ke XML. 

Perbaikan setelah presentasi dari Yoel:
1. Logout session admin sudah diperbaikin
2. saat di formAddBook, sudah diberi required. Jadi harus ada data yang diinput dulu
3. Image dari cover sudah di atur ukurannya



Penjelasan sesuai job desc dari William:
1. Login
login menggunakan email dan password yang sudah di register ke database, menggunakan required agar tidak dapat login jika data kosong, jika login sebagai member atau user biasa maka akan kembali ke halaman index.php, tetapi jika login sebagai admin makan akan masuk ke formadd buku (dapat mengedit/hapus buku) bisa jg menambah buku
2. Register
Terdapat validasi, email yang sudah digunakan tidak dapat digunakan kembali (email sama hanya sekali), dan jika password dengan confirm password tidak sesuai makan tidak dapat melakukan registrasi, terdapat required agar tidak dapat submit data masih kosong.
3. Membuat session admin, kategori dirubah manual melalui database, "0" jika member, "1" jika admin, admin = edit, hapus, tambah buku, member untuk melihat dan memasukan buku ke cart 
4. Mencari data buku (cover,judul, penulis,jumlah halaman, penerbit dan sinopsis)

Perbaikan setelah presentasi dari William:
1. menambahkan echo alert berhasil register dan welcome jika telah berhasil register dan login
2. merubah kategori yang tadinya member = null menjadi angka "0", admin tetap = "1"




Penjelasan sesuai job desc dari Femi:
1. Database buku yang berisi 2 table:
   - table list buku yang memiliki 9 kolom yaitu: nama buku, penulis, penerbit, rating, jumlah halaman, harga, sinopsis, cover dan kategori, data telah di       insert terlebih dahulu. 
   - table user yang memiliki 5 kolom yaitu: id, nama, email, password dan kategori. Data masuk ke table user setelah registrasi dilakukan.  

Perbaikan setelah presentasi dari Femi:
1. menambah kolom jumlah di dalam table list buku. 


Penjelasan sesuai job desc dari Cintya Kristianto:
1. View Profile = menampilkan nama dan email
2. Edit profile = hanya dapat mengedit nama

Perbaikan setelah presentasi dari Cintya Kristianto:
1. User dapat melakukan update terhadap profile yang mereka buat tetapi hanya dapat edit nama saja untuk password dan email tidak bisa
2. user dapat melihat data diri mereka melalui menu profil
3. ada tombol batal saat user memutuskan tidak jadi untuk mengedit profile mereka