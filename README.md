# Praktikum 7
# Pemrograman Web
```
Muhammad Rizkiansyah
311910071
TI.19.C.1
Universitas Pelita Bangsa
```
## Menjalankan Web Server
Untuk menjalankan web server dari menu XAMPP Control.
![1](https://user-images.githubusercontent.com/81758407/117910464-2bbe4e80-b306-11eb-9b75-97c02292c817.PNG)
## Memulai PHP
Buat folder lab7_php_dasar pada root directory web server (d:\xampp\htdocs)
![2](https://user-images.githubusercontent.com/81758407/117989370-753e8600-b366-11eb-8de8-b68ce9f10e03.PNG)
Kemudian untuk mengakses direktory tersebut pada web server dengan mengakses URL:
http://localhost/lab7_php_dasar/
![3](https://user-images.githubusercontent.com/81758407/117989553-9e5f1680-b366-11eb-9471-fb33da3c564d.PNG)
## PHP Dasar
Buat file baru dengan nama php_dasar.php pada directory tersebut. Kemudian buat
kode seperti berikut.
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP Dasar</h1>
    <?php
        echo "Hello World";
    ?>
</body>
</html>
```
Kemudian untuk mengakses hasilnya melalui URL:
http://localhost/lab7_php_dasar/php_dasar.php
![4](https://user-images.githubusercontent.com/81758407/117990049-fdbd2680-b366-11eb-8f16-1bf0ab3f8e50.PNG)
## Variable PHP
Menambahkan variable pada program.
```
<h2>Menggunakan Variable</h2>
    <?php
        $nim = "311910263";
        $nama = 'Mardiansyah';
        echo "NIM : " . $nim . "<br>";
        echo "Nama : $nama";
    ?>
```
![5](https://user-images.githubusercontent.com/81758407/117990264-33620f80-b367-11eb-8c4f-461a45f5de2d.PNG)
## Predefine Variable $_GET
```
<h2>Predefine Variable</h2>
    <?php 
        echo 'Selamat Datang ' . $_GET['nama'];
    ?>
```

Untuk mengaksesnya gunakan URL:
http://localhost/lab7_php_dasar/latihan2.php?nama=Mardiansyah
![6](https://user-images.githubusercontent.com/81758407/117990427-5c82a000-b367-11eb-90b4-cab074775ce8.PNG)
## Membuat Form Input
```
<h2>Form Input</h2>
    <form method="post">
        <label>Nama: </label>
        <input type="text" name="nama">
        <input type="submit" value="Kirim">
    </form>
    <?php 
        echo 'Selamat Datang ' . $_GET['nama'];
    ?>
```
![7](https://user-images.githubusercontent.com/81758407/117991306-20037400-b368-11eb-9e63-66526c2d7e1f.PNG)
## Operator
```
<h2>Operator</h2>
    <?php
        $gaji = 1000000;
        $pajak = 0.1;
        $thp = $gaji - ($gaji*$pajak);
            echo "Gaji sebelum pajak = Rp. $gaji <br>";
            echo "Gaji yang dibawa pulang = Rp. $thp";
    ?>
```
![8](https://user-images.githubusercontent.com/81758407/117991575-62c54c00-b368-11eb-844e-aa1db9e1f932.PNG)
## Kondisi IF
```
<h2>Kondisi IF</h2>
    <?php
        $nama_hari = date("l");
            if ($nama_hari == "Sunday") {
        echo "Minggu";
            } elseif ($nama_hari == "Monday") {
        echo "Senin";
            } else {
        echo "Selasa";
        }
    ?>
```
![9](https://user-images.githubusercontent.com/81758407/117991740-88eaec00-b368-11eb-9b0d-2884854a0bbc.PNG)
## Kondisi Switch
```
<h2>Kondisi Switch</h2>
    <?php
        $nama_hari = date("l");
            switch ($nama_hari) {
            case "Sunday":
        echo "Minggu";
            break;
            case "Monday":
    echo "Senin";
            break;
            case "Tuesday":
    echo "Selasa";
            break;
            default:
    echo "Sabtu";
            }
    ?>
```
![10](https://user-images.githubusercontent.com/81758407/117994196-8f7a6300-b36a-11eb-8f56-70e57f94866c.PNG)

## Perulangan for
```
<h2>Perulangan For</h2>
    <?php
        echo "Perulangan 1 sampai 10 <br />";
            for ($i=1; $i<=10; $i++) {
        echo "Perulangan ke: " . $i . '<br />';
        }
        echo "Perulangan Menurun dari 10 ke 1 <br />";
            for ($i=10; $i>=1; $i--) {
        echo "Perulangan ke: " . $i . '<br />';
        }
    ?>
```
![11](https://user-images.githubusercontent.com/81758407/117992113-dcf5d080-b368-11eb-96d4-77dea30ed22c.PNG)
## Perulangan while
```
 <h2>Perulangan While</h2>
    <?php
        echo "Perulangan 1 sampai 10 <br />";
            $i=1;
            while ($i<=10) {
        echo "Perulangan ke: " . $i . '<br />';
            $i++;
        }
    ?>
```
![12](https://user-images.githubusercontent.com/81758407/117993044-9654a600-b369-11eb-931e-1d52e14bde19.PNG)
## Perulangan dowhile
```
<h2>Perulangan Dowhile</h2>
    <?php
        echo "Perulangan 1 sampai 10 <br />";
            $i=1;
            do {
        echo "Perulangan ke: " . $i . '<br />';
            $i++;
            } while ($i<=10);
    ?>
```
![13](https://user-images.githubusercontent.com/81758407/117993200-b6846500-b369-11eb-80f4-94dae5165dc3.PNG)
## Pertanyaan dan Tugas
Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang berbeda-beda sesuai pilihan pekerjaan.
```
<h2>Pertanyaan dan Tugas</h2>
    <form method="post">
            <label>Nama Lengkap: </label>
            <input type="text" name="nama">
            <br>
            <label>Tempat Lahir: </label>
            <input type="text" name="tempat_lahir">
            <br>
            <label>Tanggal Lahir: </label>
            <input type="date" name="tgl_lahir">
            <br>
            <label>Alamat: </label>
            <input type="text" name="alamat">
            <br>
            <label>Pekerjaan:
            <select name='pekerjaan'>
                <option value='Presiden'>Presiden</option>
                <option value='Mentri'>Mentri</option>
                <option value='Gubernur'>Gubernur</option>
                <option value='Bupati'>Bupati</option>
            </select>
            </label>
            <br>
            <input type="submit" value="Kirim">
    </form>
    <h2>Output</h2>
    <?php
        echo '<br> Nama Lengkap : ' . $_POST['nama'];
        echo '<br> Tempat Lahir : ' . $_POST['tempat_lahir'];
        echo '<br> Alamat : ' . $_POST['alamat'];
            $tgl_lahir = @$_POST['tgl_lahir'];
            $lahir = new DateTime($tgl_lahir);
            $hari_ini = new DateTime();
            $diff = $hari_ini->diff($lahir);
        echo "<br> Usia : ". $diff->y ." Tahun";
        echo "<br> Pekerjaan : ". $_POST['pekerjaan'];
            $pekerjaan = @$_POST['pekerjaan'];
            if($pekerjaan == "Presiden"){
                echo '<br> Gaji : Rp. 1.000.000.000,-';
            }
            elseif($pekerjaan == "Mentri"){
                echo '<br> Gaji : Rp. .500.000.000,-';
            }
            elseif($pekerjaan == "Gubernur"){
                echo '<br> Gaji : Rp. 250.000.000,-';
            }
            elseif($pekerjaan == "Bupati"){
                echo '<br> Gaji : Rp. 150.000.000,-';
            }
    ?>
```
![code](https://user-images.githubusercontent.com/81758407/117995693-bbe2af00-b36b-11eb-8cdf-289f01021429.PNG)
![tugas](https://user-images.githubusercontent.com/81758407/117995708-be450900-b36b-11eb-847d-5cc1c9c48534.PNG)







