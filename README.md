# responsi-cloud-s5

## Cara Penggunaan
1. clone repositori ini
    ``git clone https://github.com/Proweex/responsi-cloud-s5.git``
2. masuk ke direktori 'responsi-cloud-s5'
3. clone apl web dari user chapagain
    ``git clone https://github.com/chapagain/crud-php-simple.git``
4. ubah nama direktori crud-php-simple menjadi html
    Linux command : ``mv crud-php-simple/ html``
5. ubah nilai dari variabel $databaseHost pada file config.php didalam direktori html
    **dari**
    ```$databaseHost = 'localhost';```
    **menjadi**
    ```$databaseHost = 'db';```
6. jalankan docker compose
    ``docker-compose up -d``
7. akses localhost port 80
    jika terdapat error saat mengakses web. restart docker-compose dengan menghentikan proses docker-compose menggunakan perintah ``docker-compose down`` lalu jalankan kembali docker-compose
