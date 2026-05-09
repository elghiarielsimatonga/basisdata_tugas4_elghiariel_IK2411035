# basisdata_tugas4_elghiariel_IK2411035
Nama: Elghiariel Sima Tonga
Nim : IK2411035
README – Project SQL Perulangan

Deskripsi

Project ini berisi beberapa contoh penggunaan struktur perulangan (WHILE) pada MySQL menggunakan stored procedure. File-file SQL dibuat untuk latihan dasar pemrograman basis data.

Struktur File

1. pemprograman.sql

Berisi contoh stored procedure untuk menghitung total menggunakan perulangan.

2. perulangan.sql

Berisi beberapa contoh penggunaan perulangan pada MySQL.

3. program angka 1-10.sql

Contoh program perulangan angka menggunakan stored procedure.

4. program angka 1-20.sql

Program untuk menampilkan angka secara berurutan menggunakan WHILE.

5. program bilangan genap 2-20.sql

Program untuk menampilkan bilangan genap dari 2 sampai 20.


---

Contoh Program

Menghitung Total Angka

DELIMITER $$

CREATE PROCEDURE hitung_total()
BEGIN
    DECLARE v_counter INT DEFAULT 1;
    DECLARE v_total INT DEFAULT 0;

    WHILE v_counter <= 20 DO
        SET v_total = v_total + v_counter;
        SET v_counter = v_counter + 1;
    END WHILE;

    SELECT v_total AS total;
END$$

DELIMITER ;

Fungsi

Program digunakan untuk menghitung jumlah angka dari 1 sampai 20.


---

Menampilkan Bilangan Genap

DELIMITER $$

CREATE PROCEDURE bilangan_genap()
BEGIN
    DECLARE i INT DEFAULT 2;

    WHILE i <= 20 DO
        SELECT i AS bilangan_genap;
        SET i = i + 2;
    END WHILE;
END$$

DELIMITER ;

Fungsi

Program digunakan untuk menampilkan bilangan genap dari 2 sampai 20.


---

Cara Menjalankan

1. Buka MySQL atau phpMyAdmin.


2. Import file .sql yang tersedia.


3. Jalankan stored procedure menggunakan perintah:



CALL hitung_total();

atau

CALL bilangan_genap();


---

Teknologi yang Digunakan

MySQL

SQL Stored Procedure

Struktur Perulangan WHILE



---

Tujuan Pembelajaran

Memahami penggunaan perulangan pada SQL.

Memahami pembuatan stored procedure.

Melatih logika pemrograman dasar pada basis data.



---

Author

Elghiariel Sima Tonga
