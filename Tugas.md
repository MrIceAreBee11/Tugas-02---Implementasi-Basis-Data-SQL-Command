   Tugas SQL ini merupakan salah satu tahap dalam pengembangan program sistem informasi perpustakaan yang lebih besar. Dalam tahap ini, kami merancang dan membuat struktur database yang akan digunakan untuk menyimpan informasi yang diperlukan dalam pengoperasian sistem informasi perpustakaan. Database yang dibuat adalah contoh sampel yang merepresentasikan bagian dari sistem yang sedang kami kembangkan.

   Database ini mencakup tabel-tabel yang relevan dengan operasi perpustakaan, seperti informasi buku, data anggota, data pustakawan, genre buku, dan catatan peminjaman. Setiap tabel memiliki kolom-kolom yang sesuai dengan jenis data yang harus disimpan, dan kami juga telah memasukkan beberapa data contoh ke dalam tabel-tabel ini.

   Data sampel ini digunakan untuk menguji fungsionalitas sistem dan membantu kami memahami bagaimana data akan dikelola dalam sistem informasi perpustakaan yang lebih besar. Kami akan terus mengembangkan dan memperluas sistem ini, dan database ini adalah langkah awal untuk membangun fondasi yang kuat bagi sistem informasi perpustakaan kami.

   Dalam tugas ini, kami belajar cara membuat tabel, mendefinisikan tipe data kolom, dan memasukkan data contoh ke dalam tabel. Ini adalah langkah penting dalam memahami bagaimana database akan berfungsi dalam sistem informasi perpustakaan kami yang sedang kami kembangkan."



** BUATLAH PERINTAH SQL**

===================================================================CREATE TABLE===================================================================


    CREATE TABLE Buku (
        KodeISBN INT PRIMARY KEY,
        Judul VARCHAR(255) NOT NULL,
        Penulis VARCHAR(100),
        Penerbit VARCHAR(100),
        Tahun_Terbit INT
    );

    CREATE TABLE Kategori (
        ID_Genre INT PRIMARY KEY,
        Nama VARCHAR(100)
    );

CREATE TABLE Pustakawan (
    NIK INT PRIMARY KEY,
    Nama VARCHAR(100) NOT NULL,
    Jenis_Kelamin VARCHAR(20),
    Alamat VARCHAR(255),
    Email VARCHAR(100),
    Username VARCHAR(50),
    Password VARCHAR(50)
);

CREATE TABLE Anggota (
    NIK INT PRIMARY KEY,
    Nama VARCHAR(100) NOT NULL,
    Jenis_Kelamin VARCHAR(20),
    Alamat VARCHAR(255),
    Email VARCHAR(100),
    Username VARCHAR(50),
    Password VARCHAR(50)
);

CREATE TABLE Peminjaman_Buku (
    NIK INT,
    Nama_Peminjam VARCHAR(100),
    Judul_Buku VARCHAR(255),
    Tanggal_Pinjam DATE,
    Tanggal_Kembali DATE,
    Status_Keterlambatan BOOLEAN,
    Denda INT
);

===================================================================DESCRIBE TABLE===================================================================



*Buku*


![image](https://github.com/MrIceAreBee11/Tugas-02---Implementasi-Basis-Data-SQL-Command-/assets/121444978/a34f9841-dd30-46a8-b3b7-c5eba39579db)




*Kategori*


![image](https://github.com/MrIceAreBee11/Tugas-02---Implementasi-Basis-Data-SQL-Command-/assets/121444978/251837f4-b945-4eba-ade2-6b6b09fc0108)



*Anggota*


![image](https://github.com/MrIceAreBee11/Tugas-02---Implementasi-Basis-Data-SQL-Command-/assets/121444978/5376113b-dd18-4080-8546-39cfd8b942fe)



*Pustakawan*


![image](https://github.com/MrIceAreBee11/Tugas-02---Implementasi-Basis-Data-SQL-Command-/assets/121444978/5a8c540b-cbee-49bd-84fe-3087f0b990d6)



*Peminjaman Buku*


![image](https://github.com/MrIceAreBee11/Tugas-02---Implementasi-Basis-Data-SQL-Command-/assets/121444978/e571f79a-a8d9-4b69-ba60-f84cdcda6bdd)



=================================================INSERT INTO TABLE (masing-masing table 1 value)====================================================


*Buku*


INSERT INTO Buku (KodeISBN, Judul, Penulis, Penerbit, Tahun_Terbit)
VALUES (12345678, 'Buku Panduan Guru Cerdas Cergas Berbahasa dan Bersastra Indonesia untuk SMA/SMK Kelas XI', 'Heny Marwati & K. Waskitaningtyas', 'Pusat Kurikulum dan Perbukuan', 2021);




*Kategori*


INSERT INTO Genre (ID_Genre, Nama)
VALUES (4, 'Bahasa');




*Anggota*


INSERT INTO Anggota (NIK, Nama, Jenis_Kelamin, Alamat, Email, Username, Password)
VALUES (1301212244, 'Megawati Hangestri Pertiwi', 'Perempuan', 'Kabupaten Jember', 'megatron08@email.com', 'megatron08', 'soultry08');




*Pustakawan*


INSERT INTO Pustakawan (NIK, Nama, Jenis_Kelamin, Alamat, Email, Username, Password)
VALUES (1301212251, 'Muhammad Ramadhan Sananta', 'Laki-laki', 'Kepulauan Riau', 'sananta09@email.com', 'snanta09', 'soul09');




*Peminjaman Buku*


INSERT INTO Peminjaman_Buku (NIK, Nama_Peminjam, Judul_Buku, Tanggal_Pinjam, Tanggal_Kembali, Status_Keterlambatan, Denda)
VALUES (1301212244, 'Megawati Hangestri Pertiwi', 'Buku Panduan Guru Cerdas Cergas Berbahasa dan Bersastra Indonesia untuk SMA/SMK Kelas XI', '2023-10-29', '2023-11-01', false, 0);




===================================================================SELECT * FROM===================================================================


*Buku*


![image](https://github.com/MrIceAreBee11/Tugas-02---Implementasi-Basis-Data-SQL-Command-/assets/121444978/8c92869a-f783-4736-8c67-fc209dddf352)




*Kategori*


![image](https://github.com/MrIceAreBee11/Tugas-02---Implementasi-Basis-Data-SQL-Command-/assets/121444978/17db5512-5504-4ba0-94b6-e8471ea8c815)



*Anggota*


![image](https://github.com/MrIceAreBee11/Tugas-02---Implementasi-Basis-Data-SQL-Command-/assets/121444978/d126318e-0e04-4035-8804-e32533edb1ee)




*Pustakawan*


![image](https://github.com/MrIceAreBee11/Tugas-02---Implementasi-Basis-Data-SQL-Command-/assets/121444978/b931a8d5-c713-4537-8a81-89e2df7598ad)




*Peminjaman Buku*


![image](https://github.com/MrIceAreBee11/Tugas-02---Implementasi-Basis-Data-SQL-Command-/assets/121444978/b3dfe33a-7d63-455b-b0d1-f84d9e5fdf6a)



