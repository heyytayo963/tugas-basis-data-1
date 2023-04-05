##Tugas-Basis-Data

1. Membuat sebuah database dengan nama latihan001!
``` 
CREATE DATABASE latihan001;
```
![r1](https://user-images.githubusercontent.com/115687740/229983492-954e0920-5ffc-4041-950c-f50d6cf33d03.png)



2. Buat sebuah tabel dengan nama biodata (nama, alamat) didalam
database latihan1!
```
CREATE TABLE siswa (nama VARCHAR(100), alamat TEXT);
```
![r2](https://user-images.githubusercontent.com/115687740/229983608-87c3eeb8-9896-430a-aed3-dcad37c3fb8d.png)

3. Tambahkan sebuah kolom keterangan (varchar 15), sebagai kolom
terakhir!
```
ALTER TABLE siswa ADD COLUMN keterangan varchar(15) AFTER alamat;
```
![r3](https://user-images.githubusercontent.com/115687740/229983674-048ff7dd-7962-4298-bd06-051be388c3af.png)


4. Tambahkan kolom id (int 11) di awal (sebagai kolom pertama)!
```
ALTER TABLE siswa ADD COLUMN id int(11) First;
```
![r4](https://user-images.githubusercontent.com/115687740/229983711-9a9f5349-7b88-4b08-b0cc-3405ce23fbc9.png)


5. Sisipkan sebuah kolom dengan nama phone (varchar 15) setelah
kolom alamat!
```
ALTER TABLE siswa ADD COLUMN phone varchar(15) after alamat;
```
![r5](https://user-images.githubusercontent.com/115687740/229983749-a028c6cd-b90a-4d1c-af62-2201cb22c4fb.png)


6. Ubah tipe data kolom id menjadi char(11)!
```
ALTER TABLE siswa MODIFY COLUMN id VARCHAR(11);
```
![r6](https://user-images.githubusercontent.com/115687740/229983774-7a2ded1e-521e-4710-8ea2-8d4a1aa27c81.png)


7. Ubah nama kolom phone menjadi hp (varchar 20)!
```
ALTER TABLE siswa CHANGE COLUMN phone hp varchar(20);
```
![r7](https://user-images.githubusercontent.com/115687740/229983800-27dd237b-a0cf-45cf-95fa-b2f2c9181f66.png)


8. Tambahkan kolom email setelah kolom hp
```
ALTER TABLE siswa ADD COLUMN email text after hp;
```
![r8](https://user-images.githubusercontent.com/115687740/229983843-013eea1a-f779-43c3-9e7c-6e608a1708c4.png)


9. Hapus kolom keterangan dari tabel!
```
alter table siswa drop keterangan;
```
![r9](https://user-images.githubusercontent.com/115687740/229983886-418a33d5-6623-491c-8c52-b9c58b8a0cfd.png)

10. Ganti nama tabel menjadi data_mahasiswa!
```
alter table siswa rename data_mahasiswa;
```
![r10](https://user-images.githubusercontent.com/115687740/229983931-62cb1234-b765-4442-94e4-9e7a61ed6778.png)


11. Ganti nama field id menjadi nim!
```
ALTER TABLE data_mahasiswa CHANGE COLUMN id nim varchar(11);
```
![r11](https://user-images.githubusercontent.com/115687740/229983972-3b3023cd-2645-4f7f-b0df-d0e282bf2db3.png)


12. Jadikan nim sebagai PRIMARY KEY!
```
ALTER TABLE data_mahasiswa ADD PRIMARY KEY(nim);
```
![r12](https://user-images.githubusercontent.com/115687740/229984001-d872c3d2-a4f0-44bf-b63b-511d24a8c59f.png)


13. Jadikan kolom email sebagai UNIQUE KEY
```
ALTER TABLE data_mahasiswa ADD CONSTRAINT email unique KEY(email);
```
![r13](https://user-images.githubusercontent.com/115687740/229984046-e8e1a7d8-aa6f-40cc-bc1b-9a833f08fa61.png))



# Evaluasi dan pertanyaan
1. Apa maksud dari int (11)?
```
int (11) nunjukkan bahwa kolom memiliki tipe data bilangan bulat (integer) dengan ukuran 11 digit 
```

2. Ketika kita melihat struktur tabel dengan perintah desc, ada kolom Null yang
berisi Yes dan No. Apa maksudnya ?
```
Jika kolom "Null" adalah "YES", itu berarti kolom tersebut diizinkan untuk memiliki nilai NULL.

Jika kolom "Null" adalah "NO", maka kolom tersebut tidak diizinkan untuk memiliki nilai NULL
```
