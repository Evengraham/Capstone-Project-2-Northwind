# Capstone-Project-2-Northwind
Capstone Project 2 Northwind

Pada Pengerjaan capastone project 2 ini, saya mendapatkan Northwind dengan Tabel Products.
langkah pertama yang saya lakukan :

# Instalasi Database Northwind
Download file sql yang telah disediakan.
Buka terminal/command prompt di directory lokasi dari file yang telah di download. Bisa dengan menggunakan cd lokasi directory (ex : cd C:/Users/achma/Desktop) atau bisa dengan langsung membuka command prompt/terminal di lokasi directory nya.
Masuk pada mysql command dengan cara mengetikan mysql -u root -p lalu masukan password masing-masing.
Setelah masuk di mysql command, silahkan buat sebuah database dengan menggunakan perintah create database namadatabase (ex : create database human_resource).
Gunakan database yang barusan dibuat tersebut dengan perintah use namadatabase (ex : use human_resource).
Setelah masuk di database, ketikan SOURCE HR Database.sql.
Biarkan prosesnya berjalan hingga selesai. 

# Kemudian setelah sudah connect
Saya memasukan nya di jupyternotebook.

Setelah itu saya melihat data dari setiap tabel yang ada di northwind untuk dapat digabungkan dengan data product yang saya dapat.
Pada penggabungan tabel tersebut saya sudah menggabungkan dari tiap tabel berbeda dan kolom yang berbeda.
Jadinya terdapat penambahan kolom dari kolom products.
berikut kolom yang bertambah :
1. CategoryName
2. OrderID	
3. Quantity	
4. UnitPrice	
5. ShipCountry

Saya mengambil data tersebut untuk hasil Pembelian terbanyak dari tiap product dan tiap shipcountry mana yang terbanyak.

# Missing Value
Dari data Tabel1 yang sudah saya buat tidak terdapat Missing Value. Hanya ada Dtype yang salah

# Mengubah tipe data yang salah
Dari kolom UnitPrice awal DType nya adalah Object, Kemudian saya mengubah menjadi Float.
Kemudian saya mengecek kembali dari data tipe yang salah / tabel1.info() , hasilnya sudah berubah menjadi float64.


# Groupby
## Produk yang di beli paling banyak
1. Disini saya akan menggabungkan / Groupby pada ProductName dan ProductID untuk mengetahui Jumlah produk apa yang pembeliannya paling banyak di beli oleh customer.

## ShipCountry Terbanyak

Pada ShipCountry saya ingin mengetahui Negara mana yang paling banyak mengangkut barang terbanyak pada Produk tersebut.
Yang dimana saya menggabungkan ShipCountry dan ProductID untuk mentotalkan keseluruhan data tersebut agar dapat terlihat negara mana yang mengirim paling banyak.

# DATA VISUALIZATION & STATISTICS
Dari ke 2 hasil tersebut, langsung saya buatkan visualisasi statistiknya dengan barplot.

Setelah melihat hasil, Ternyata produk yang paling banyak di beli adalah produk :
1. Raclette Courdavault
2. Gorgonzola Telino
3. Guaran Fantstica
4. Camembert Pierrot
5. Gnocchi di nonna Alice

Ternyata dari hasil tersebut Keju dan Pasta lah yang lebih banyak di minati oleh pembeli, wajar saja karena budaya Barat lebih terbiasa atau lebih suka memakan keju dan pasta karena sudah menjadi makanan sehari hari.


Dari hasil pengiriman produk, ShipCountry terbanyak masuk di negara :
USA : Dari segi warga USA banyak pembeli di karenakan penduduk USA memiliki penduduk lebih banyak dari negara yang ada di list tersebut.
German : Warga German itu makanan tradisionalnya adalah Keju dan Pasta, maka lebih banyak peminat yang membeli.
Brazil : Penduduk Brazil rata rata penduduknya dalam sehari hari memakan keju.
France : Di France rata rata penduduknya dalam sehari hari memakan keju.
UK : di UK juga sama, selera masyarakat nya suka dengan Keju.

Kesimpulannya dari 5 negara tersebut :
Keberadaan Keju dan Pasta ada kewajiban untuk masyarakat mereka untuk di makan.
Seperti halnya di Indonesia Nasi.
