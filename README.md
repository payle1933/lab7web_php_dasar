# Praktikum 7 - Pemrograman Web
```
MAULANA HASANUDIN
312010106
TI.20.D.1
Universitas Pelita Bangsa
```
# Buka XAMPP dan jalankan Apache
![11](https://user-images.githubusercontent.com/101716660/169491981-85a9b851-4f6c-4f51-a39c-a929a7142aa0.png)


Buat Folder lab7_php_dasar pada root directory web server (C:\xampp\htdocs) dan Buat file baru dengan nama php_dasar.php pada directory tersebut.
![22](https://user-images.githubusercontent.com/101716660/169492040-d981bb60-9887-4b88-8c95-0fc471f76f5f.png)
![33](https://user-images.githubusercontent.com/101716660/169492223-fd0e2664-4ff8-4fbf-b99b-d3140b27f402.png)



Untuk mengakses direktory tersebut pada web server dengan mengakses URL: http://localhost/lab7_php_dasar/
![4](https://user-images.githubusercontent.com/101716660/169492331-b19ddd84-1874-4c51-98b8-8d7814fd3112.png)

# LANGKAH 1
## Coding dasar pengenalan PHP
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
![5](https://user-images.githubusercontent.com/101716660/169492516-0b0fbe18-0e9a-45c1-9fe3-3cb438309945.png)

# LANGKAH 2
## Menambahkan Variable pada Program
```
<h2>Menggunakan Variable</h2>
<?php
    $nim = "0411500400";
    $nama = 'Abdullah';
    echo "NIM : " . $nim . "<br>";
    echo "Nama : $nama";
?>
```
![6](https://user-images.githubusercontent.com/101716660/169492686-ba729ae9-f92a-4d32-a60e-1fa866116ddf.png)

# LANGKAH 3
## Predefine Variable
```
<h2>Predefine Variable</h2>
<?php
    echo 'Selamat Datang ' . $_GET['nama'];
?>
```
![7](https://user-images.githubusercontent.com/101716660/169493422-4d252f15-f3ce-4f20-87c7-5e0843d79d34.png)


# LANGKAH 4
## Membuat Form Input
```
<h2>Form Input</h2>
<form method="post">
    <label>Nama: </label>
    <input type="text" name="nama">
    <input type="submit" value="Kirim">
</form>
<?php
    echo 'Selamat Datang ' . $_POST['nama'];
?>
```
![8](https://user-images.githubusercontent.com/101716660/169493534-979e544a-db22-43be-a40a-1de5df4bc98b.png)


# LANGKAH 5
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
![9](https://user-images.githubusercontent.com/101716660/169493660-a7b49158-90ba-4d6b-9b99-949a0f94d946.png)

# LANGKAH 6
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
![10](https://user-images.githubusercontent.com/101716660/169493762-e1f82f90-94d5-4c55-a9d8-e8c8b5e06690.png)

# LANGKAH 7
## Kondisi SWITCH
```
<h2>Kondisi SWITCH</h2>
    <?php
    $nama_hari = date("1");
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
![111](https://user-images.githubusercontent.com/101716660/169493865-677d6b7d-0b91-4b5b-8c6d-456109b3718b.png)


# LANGKAH 8
## Perulangan FOR
```
<h2>Perulangan FOR</h2>
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
![12](https://user-images.githubusercontent.com/101716660/169493980-65dd38ce-13ea-4fe1-9f14-e6b2aa315238.png)


# LANGKAH 9
## Perulangan WHILE
```
<h2>Perulangan WHILE</h2>
    <?php
        echo "Perulangan 1 sampai 10 <br />";
        $i=1;
        while ($i<=10) {
            echo "Perulangan ke: " . $i . '<br />';
            $i++;
        }
    ?>
 ```
![13](https://user-images.githubusercontent.com/101716660/169494099-95be619f-f3dd-4cf7-bfe0-f12d5749a610.png)


# LANGKAH 10
## Perulangan DOWHILE
```
<h2>Perulangan DOWHILE</h2>
    <?php
        echo "Perulangan 1 sampai 10 <br />";
        $i=1;
        do {
            echo "Perulangan ke: " . $i . '<br />';
            $i++;
        } while ($i<=10);
    ?>
```    
![14](https://user-images.githubusercontent.com/101716660/169494192-7d8cad7f-ddb3-43c8-a6d4-57cba48ba8c5.png)


# TUGAS
## Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang berbeda-beda sesuai pilihan pekerjaan.
# CODING
```
    <h2>TUGAS</h2>
    <form method="post">
            <label>Nama: </label>
            <input type="text" name="nama">
            <br>
            <label>Tanggal Lahir: </label>
            <input type="text" name="tgl_lahir">
            <br>
            <label>Pekerjaan: 
            <select name='pekerjaan'>
                <option value='Direktur'>Direktur</option>
                <option value='Manager'>Manager</option>
                <option value='Staff'>Staff</option>
                <option value='Operator'>Operator</option>
            </select>
            </label>
            <br>
            <input type="submit" value="Kirim">
    </form>
    <?php
        # Memanggil Nama
        echo 'Nama: ' . $_POST['nama'];

        # Merubah Tanggal Lahir menjadi Umur (Tahun)
        $tgl_lahir = @$_POST['tgl_lahir'];

        $lahir = new DateTime($tgl_lahir);
        $hari_ini = new DateTime();

        $diff = $hari_ini->diff($lahir);

        # Memanggil fungsi umur yg sudah dibuat diatas
        echo "<br> Umur: ". $diff->y ." Tahun";

        # Memanggil pekerjaan
        echo "<br> Pekerjaan: ". $_POST['pekerjaan'];

        # Kondisi if pekerjaan untuk menentukan gaji
        $pekerjaan = @$_POST['pekerjaan'];

        if($pekerjaan == "Direktur"){
            echo '<br> Gaji: Rp. 10.000.000,-';
        }elseif($pekerjaan == "Manager"){
            echo '<br> Gaji: Rp. 7.000.000,-';
        }elseif($pekerjaan == "Staff"){
            echo '<br> Gaji: Rp. 5.000.000,-';
        }elseif($pekerjaan == "Operator"){
            echo '<br> Gaji: Rp. 4.000.000,-';
        }
    ?>
 ```
![15](https://user-images.githubusercontent.com/101716660/169494370-8ef7517a-9ddd-42f8-9e05-fa57a7b4ae4d.png)

![16](https://user-images.githubusercontent.com/101716660/169494390-9e6731aa-bf83-469a-ab45-68ba542b31d5.png)


Perbedaan metode POST dan GET
* Metode GET akan menampilkan semua data dalam url (yang kemudian disebut sebagai query string).
* Sedangkan POST akan menyimpan data di dalam body request tanpa menampilkannya secara langsung di dalam URL.
![17](https://user-images.githubusercontent.com/101716660/169494488-2b72ac93-fd5c-419e-a7d7-3d2fee6aa44b.png)

