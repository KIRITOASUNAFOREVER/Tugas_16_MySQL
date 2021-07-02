# Tugas_16_MySQL

### 1. Buat database dengan nama matkul dan insert 5 buah data yang jika ditampilkan akan seperti gambar dibawah ini!
![HasilNomor1](HasilNomor1.png)


```mongodb
use matkul;
```
![DBMatkul](DBMatkul.PNG)


```mongodb
db.matkul.insertMany( [
      { matkul:"Algoritma & Pemrograman", kode_matkul:"1234567", nama_dosen:"Jamal Kosasih" },
      { matkul:"Rekayasa Perangkat Lunak", kode_matkul:"1234568", nama_dosen:"Ivan Bagus" },
      { matkul:"Sistem Basis Data",  kode_matkul:"1234569", nama_dosen:"Anida Nur Afika"},
      { matkul:"Pengantar Ilmu Komputer",  kode_matkul:"1234561", nama_dosen:"Nico Ariesto"},
      { matkul:"Bahasa Indonesia",  kode_matkul:"1234562", nama_dosen:"Fifi Meilani"}
   ] );
```
![DBInsert](DBInsert.PNG)

![Nomor1](Nomor1.PNG)


### 2. Ubah nama_dosen menjadi Sekar Wandansari untuk kode_matkul = 1234562.
```mongodb
db.matkul.update(
   { kode_matkul: "1234562" },
   {
     $set: { nama_dosen:"Sekar Wandansari" },
   }
);
```

![Nomor2](Nomor2.PNG)

### 3. Hapus data nama dosen a/n Jamal Kosasih dan Ivan Bagus dari tabel matkul!
```mongodb
db.matkul.remove(
       { "nama_dosen":"Jamal Kosasih" }
);
```

```mongodb
db.matkul.remove(
       { "nama_dosen":"Ivan Bagus" }
);
```

![Nomor3](Nomor3.PNG)

### 4. Hapus database matkul!
```mongodb
db.dropDatabase()
```

![Nomor4](Nomor4.PNG)
