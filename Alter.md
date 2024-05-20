# ALTER 
## Menambahkan Kolom
### Struktur Query

```mysql
ALTER TABLE nama_table ADD nama_kolom_baru varchar(10) AFTER nama_kolom_lama;
```

### Contoh

```mysql
ALTER TABLE daftar_mobil ADD batas_peminjaman VARCHAR(10) AFTER peminjam;
```

### Penjelasan
- ALTER TABLE mobil: Perintah untuk mengubah struktur tabel mobil.
- ADD batas_peminjaman varchar(10): Menambahkan kolom baru dengan nama batas_peminjaman yang memiliki tipe data varchar(10).
- AFTER peminjam: Menentukan bahwa kolom baru akan ditambahkan setelah kolom peminjam dalam struktur tabel.
### Kesimpulan
ALTER TABLE mobil ADD batas_peminjaman VARCHAR(10) AFTER peminjam; digunakan untuk menambahkan kolom baru bernama batas_peminjaman dengan tipe data VARCHAR(10) ke tabel mobil, diletakkan setelah kolom peminjam.
### Hasil
![gambar](Aset/Alter/IMG1.png)

## Query Tambahan

```mysql
UPDATE daftar_mobil SET batas_peminjaman='2024-04-24' WHERE peminjaman IS NOT NULL ;
```

### Penjelasan
- UPDATE mobil: adalah perintah untuk memperbarui data dalam tabel mobil.
- SET batas_peminjaman='2024-04-24': menetapkan nilai '2024-04-24' ke kolom batas_peminjaman untuk baris yang sesuai dengan kondisi yang diberikan.
- WHERE peminjaman IS NOT NULL: adalah klausa WHERE yang menentukan kondisi untuk baris yang akan diperbarui. Dalam hal ini, hanya baris di mana nilai kolom peminjaman tidak NULL yang akan diperbarui.
### Kesimpulan
UPDATE mobil SET batas_peminjaman='2024-04-24' WHERE peminjaman IS NOT NULL; digunakan untuk memperbarui nilai kolom batas_peminjaman menjadi '2024-04-24' untuk semua baris di tabel mobil di mana nilai kolom peminjaman tidak NULL. 
### Hasil
![gambar](Aset/Alter/IMG2.png)

## Mengubah Nama kolom
### Struktur Query

```mysql
ALTER TABLE nama_tabel RENAME COLUMN nama_kolom TO nama_kolom_Baru
```

### Contoh 

```mysql
ALTER TABLE daftar_mobil RENAME COLUMN batas_peminjaman TO Deadline;
```

### Penjelasan
-  ALTER TABLE mobil:  adalah perintah untuk mengubah struktur tabel yang ada di mobil.
- RENAME COLUMN batas_peminjaman TO Deadline: adalah bagian dari perintah `ALTER TABLE`yang menentukan perubahan yang diinginkan. Contoh menggunakan klausa RENAME COLUMN untuk mengubah nama kolom `batas_peminjaman`menjadi Deadline.
### Kesimpulan
ALTER TABLE mobil RENAME COLUMN batas_peminjaman TO Deadline; digunakan untuk mengubah nama kolom dari batas_peminjaman menjadi Deadline dalam tabel mobil. 
### Hasil 
![gambar](Aset/ALter/IMG3.png)

## Mengubah Tipe data kolom
### Struktur query

```mysql
ALTER TABLE (nama_tabel) MODIFY h(nama_kolom) (nama_tipedata);
```

### Contoh 

```mysql
Alter Table daftar_mobil MODIFY deadline DATE;
```

### Penjelasan
- ALTER TABLE mobil:  adalah perintah untuk mengubah struktur tabel yang ada, dalam hal ini, tabel mobil.
- MODIFY deadline DATE:  adalah bagian dari perintah ALTER TABLE yang menentukan perubahan yang diinginkan. Contoh menggunakan klausa `MODIFY`untuk mengubah tipe data kolom deadline menjadi DATE.
### Kesimpulan
ALTER TABLE mobil MODIFY deadline DATE; digunakan untuk mengubah tipe data kolom `deadline`dalam tabel mobil menjadi tipe data DATE.berguna untuk memastikan bahwa kolom deadline dapat menyimpan tanggal dengan format yang benar
### Hasil 
![gambar](Aset/Alter/IMG4.png)


## Menambah Constraints
### Struktur Query

```mysql
ALTER TABLE (nama_tabel)
ALTER (nama_kolom) SET DEFAULT (nilai_default );
```

### Contoh

```mysql
ALTER TABLE mobil
ALTER deadline SET DEFAULT Ready;
```

### Penjelasan 
- ALTER TABLE mobil: adalah perintah untuk mengubah struktur tabel yang ada, dalam hal ini, tabel mobil.
- ALTER deadline SET DEFAULT 'Ready': adalah bagian dari perintah ALTER TABLE yang menentukan perubahan yang diinginkan. Contoh menggunakan klausa ALTER untuk mengubah kolom deadline, dan SET DEFAULT 'Ready' digunakan untuk menetapkan nilai default 'Ready' untuk kolom tersebut.
### Kesimpulan
ALTER TABLE mobil ALTER deadline SET DEFAULT 'Ready'; digunakan untuk menetapkan nilai default 'Ready' pada kolom deadline dalam tabel mobil. 
### Hasil 
![Gambar](Aset/Alter/IMG5.png)

## Menghapus Constraints
### Struktur Query

```mysql
ALTER TABLE (nama_tabel)
ALTER (nama_kolom) DROP DEFAULT;
```

### Contoh

```mysql
ALTER TABLE mobil
ALTER deadline DROP DEFAULT ;
```

### Penjelasan
- ALTER TABLE mobil: adalah perintah untuk mengubah struktur tabel yang ada, dalam hal ini, tabel mobil.
- ALTER deadline DROP DEFAULT: adalah bagian dari perintah ALTER TABLE yang menentukan perubahan yang diinginkan. Contoh menggunakan klausa ALTER untuk mengubah kolom deadline, dan `DROP DEFAULT`digunakan untuk menandai bahwa nilai default dari kolom tersebut akan dihapus.
### Kesimpulan
ALTER TABLE mobil ALTER deadline DROP DEFAULT; digunakan untuk menghapus nilai default dari kolom `deadline`dalam tabel mobil. 
### Hasil 
![Gambar](Aset/Alter/IMG6.png)

## Menghapus Kolom
### Struktur Query

```mysql
ALTER TABLE nama_tabel DROP COLUMN nama_kolom;
```

### Contoh 

```mysql
ALTER TABLE mobil DROP COLUMN batas_peminjaman;
```

### Penjelasan 
- ALTER TABLE mobil: adalah perintah untuk mengubah struktur tabel yang ada, dalam hal ini, tabel mobil.
- DROP COLUMN deadline: adalah bagian dari perintah ALTER TABLE yang menentukan perubahan yang diinginkan. Contoh menggunakan klausa DROP COLUMN untuk menandai bahwa kolom deadline harus dihapus dari tabel mobil.
### Kesimpulan
ALTER TABLE mobil DROP COLUMN deadline; digunakan untuk menghapus kolom deadline dari tabel mobil. 
### Hasil 
![gambar](Aset/Alter/IMG7.png)
## Mengganti nama tabel 
### Struktur Query

```mysql
ALTER TABLE nama_tabel RENAME TO nama_baru_tabel
```

### Contoh

```mysql
ALTER TABLE mobil RENAME TO data_mobil
```

### Penjelasan
- ALTER TABLE mobil: adalah perintah untuk mengubah struktur tabel yang ada, dalam hal ini, tabel mobil.
- RENAME TO data_mobil: adalah bagian dari perintah `ALTER TABLE`yang menentukan perubahan yang diinginkan. Contoh menggunakan klausa `RENAME TO`untuk mengubah nama tabel mobil menjadi data_mobil.
### Kesimpulan
ALTER TABLE mobil RENAME TO data_mobil; digunakan untuk mengubah nama tabel mobil menjadi data_mobil.
### Hasil 
![gambar](Aset/Alter/IMG8.png)