# responsi-cloud-s5

## Cara Penggunaan
1. clone repositori ini
    
    ``git clone https://github.com/Proweex/responsi-cloud-s5.git``
    
2. masuk ke direktori 'responsi-cloud-s5'
    
    jika ingin langsung pull image server dari docker hub bisa uncomment dahulu baris ke 7 dan comment baris 5 dan 6.
    
    **sebelum**
    ```
    services:
      php:
        build: 
          context: .
        #image: firli/responsi-cloud-s5_php:firstpush
        ports:
          - 80:80
    volumes:
      - ./html:/var/www/html/
    ```
      
    **sesudah**
    ```
    services:
      php:
        #build: 
          #context: .
        image: firli/responsi-cloud-s5_php:firstpush
        ports:
          - 80:80
    volumes:
      - ./html:/var/www/html/
    ```
    [link to Dockerhub repo!](https://hub.docker.com/r/firli/responsi-cloud-s5_php)

3. jalankan docker compose

    ``docker-compose up -d``

4. akses localhost port 80

    jika terdapat error saat mengakses web. restart docker-compose dengan menghentikan proses docker-compose menggunakan perintah ``docker-compose down`` lalu jalankan kembali docker-compose.
    
    atau bisa tunggu dahulu beberapa saat sebelum mengakses web.

source web oleh user chapagain ([source](https://github.com/chapagain/crud-php-simple))
