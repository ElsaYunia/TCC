# Infrastructure as Code
Infrastructure as Code adalah proses penyediaan IT infrastruktur dimana sistem dibangun dan dikelola melalui kode secara automasi (otomatis), bukan secara manual. Atau bisa disebut juga bahasa kerennya Programmable Infrastructure.

Dengan menggunakan kode dan meng-automasi, proses setting dan konfigurasi baremetal, virtual mesin, cloud computing baik itu instalasi baru, perubahan konfigurasi dapat dilakukan secara cepat, mudah, dan berulang. Di sisi lain juga, ada manfaat lainnya yaitu dokumentasi. Jadi siapapun tahu konfigurasi server, kebutuhan aplikasi server dan sebagainya.

Disni, saya mengaplikasikan IAC dengan menggunakan CFEngine

![2000px-cfengine-logo svg_](https://user-images.githubusercontent.com/43244821/49914697-e55e2e80-fec4-11e8-883c-766b67515db8.png)

CFEngine adalah sistem manajemen konfigurasi yang menyediakan framework untuk pengelolaan infrastruktur IT secara otomatis. CFEngine terdesentralisasi dan sangat skalabel. 

## Fitur CFEngine 
1. Menentukan konfigurasi dari keseluruhan sistem, termasuk: Perangkat, Pengguna, Aplikasi, dan Layanan.
2. Membantu mempertahankan sistem itu dari waktu ke waktu.
3. Memeriksa status sistem pada suatu momen tertentu.
4. Memastikan kepatuhan dengan status sistem yang diinginkan.
5. Menyebarkan modifikasi atau pembaruan real-time di seluruh sistem.

## Configure the host
Pertama, memastikan bahwa hostname yang diminta untuk mengakses Mission Portal sudah benar
![screenshot_6](https://user-images.githubusercontent.com/43244821/49915025-33bffd00-fec6-11e8-8aaa-3e06bdad9c46.jpg)

Kemudian, memastikan bahwa ini adalah host fqdn sehingga sertifikat ssl yang dihasilkan selama installasi akan cocok.
![screenshot_7](https://user-images.githubusercontent.com/43244821/49915105-88637800-fec6-11e8-9833-a013e4b7a0fc.jpg)

## Install Package
Mengunduh dan menginstall Paket Hub Ubuntu, dengan menggunakan quick install script. Ini menginstal versi LTS terbaru dari CFEngine Enterprise secara default.
Download script :
![screenshot_8](https://user-images.githubusercontent.com/43244821/49915197-e1cba700-fec6-11e8-8aee-7fc54527d7f0.jpg)

Install 3.11 version :
![screenshot_9](https://user-images.githubusercontent.com/43244821/49915239-09227400-fec7-11e8-94ac-7bd6af866bc0.jpg)
![screenshot_10](https://user-images.githubusercontent.com/43244821/49915298-61597600-fec7-11e8-8019-8914b7811984.jpg)
![screenshot_11](https://user-images.githubusercontent.com/43244821/49915307-6fa79200-fec7-11e8-8e15-527820fb92a3.jpg)

## Bootstrap Hub
menghubungkan ke dirinya sendiri :
![screenshot_12](https://user-images.githubusercontent.com/43244821/49915340-a1b8f400-fec7-11e8-9bc7-720c7998a7cb.jpg)

Menjalankan policy untuk menyelesaikan proses installasi :
![screenshot_14](https://user-images.githubusercontent.com/43244821/49915412-0e33f300-fec8-11e8-9650-a52a2f5d6ff2.jpg)

## Collect Reports
Dalam beberapa menit ke depan, hub akan mengumpulkan laporan dari kebijakan sebelumnya dan Mision Portal akan diisi dengan data. 
![screenshot_15](https://user-images.githubusercontent.com/43244821/49915450-49362680-fec8-11e8-9751-f1f476f85848.jpg)

## Log in to Mission Portal
Masuk ke portal Mission :
![screenshot_16](https://user-images.githubusercontent.com/43244821/49915477-6b2fa900-fec8-11e8-8d87-19433322955b.jpg)

Login :
![screenshot_17](https://user-images.githubusercontent.com/43244821/49915612-0cb6fa80-fec9-11e8-8e33-a7f951a1a394.jpg)

![screenshot_18](https://user-images.githubusercontent.com/43244821/49915634-22c4bb00-fec9-11e8-92c1-965c6421fcc1.jpg)

Demikian penjelasan dari penggunaan CFEngine sebagai IaC. apabila ada kesalahan saya mohon maaf dan mohon kritik dan sarannya. Terimakasih :) 










