# Laporan Praktikum  
##  LocalStack 
            Oleh:
	Nama                 : Rifhani
	Nim                  : 2023903430040
	Kelas                : TRKJ 2.B
	Jurusan              : Teknologi Informasi dan Komputer
	Program Studi	     : Teknologi Rekayasa Komputer Jaringan
	Dosen Pembimbing	: Muhammad Davi, S.Kom.,M.CS
    


###  PENDAHULUAN 

A. latar belakang   

    LocalStack merupakan sebuah platform open-source yang dirancang untuk meniru berbagai layanan AWS secara lokal di lingkungan pengembangan. Dengan menggunakan Docker sebagai basisnya, LocalStack memungkinkan para pengembang untuk membangun, menguji, dan menjalankan aplikasi berbasis layanan AWS tanpa harus terkoneksi langsung dengan cloud AWS yang sesungguhnya. Hal ini memberikan keuntungan besar dalam hal efisiensi waktu dan biaya, terutama selama proses pengembangan dan debugging. Dalam praktikum ini, fokus utama adalah mempelajari bagaimana LocalStack dapat digunakan untuk menyimulasikan layanan-layanan seperti Amazon S3 untuk penyimpanan file, AWS Lambda untuk fungsi serverless, Amazon DynamoDB sebagai database NoSQL, serta API Gateway untuk menerima data dari sensor.
---

B. Tujuan Praktikum 

Tujuan dari pratikum ini adalah: 

-   Mensimulasikan layanan AWS secara lokal tanpa biaya.

-   Mempercepat proses pengujian dan pengembangan aplikasi.

-   Mendukung pengujian tanpa koneksi internet (offline).

-   Menghindari risiko penggunaan layanan AWS langsung saat tahap awal.

-   Memudahkan integrasi dengan alat seperti AWS CLI dan Terraform.
C. Dasar Teori
    merupakan salah satu platform layanan cloud terbesar yang menyediakan berbagai infrastruktur dan layanan seperti penyimpanan data (S3), komputasi serverless (Lambda), basis data NoSQL (DynamoDB), dan API Gateway. Dalam pengembangan aplikasi berbasis cloud, layanan-layanan ini sering digunakan untuk membangun sistem yang fleksibel dan skalabel. Namun, mengakses layanan AWS secara langsung selama tahap pengembangan dapat memerlukan biaya dan koneksi internet yang stabil. Untuk mengatasi hal tersebut, LocalStack hadir sebagai solusi open-source berbasis Docker yang memungkinkan pengembang mensimulasikan layanan AWS secara lokal. Dengan menjalankan LocalStack di lingkungan lokal, pengembang dapat membangun, menguji, dan memverifikasi aplikasi tanpa harus terhubung langsung ke layanan AWS yang sebenarnya. Hal ini mendukung praktik Infrastructure as Code (IaC) dan mempercepat siklus pengembangan perangkat lunak modern.

###  D. Alat dan Bahan  
- Laptop/PC dengan OS Linux/Windows/macOS  
- Docker  
- Python 3.x  
- AWS CLI  
- LocalStack  
- Flask dan Boto3  
- Editor teks atau IDE (VS Code, PyCharm, dll)  
- Internet untuk instalasi paket


###  E. Langkah-Langkah Praktikum
1. Instalasi

- Instal Docker dan verifikasi dengan docker --version
- Instal Python dan pip, - verifikasi dengan python3 --version dan pip3 --version

- Instal AWS CLI: pip3 install awscli --upgrade --user

- Instal LocalStack: pip3 install localstack

2. Konfigurasi AWS CLI
![alt text](<img (2).jpg>)

2. Menjalankan LocalStack
![alt text](<img (3).jpg>)
 3. Pengujian Layanan AWS Lokal
 -Buat bucket S3:
 ![alt text](<img (5)-1.jpg>)
 4. Upload file ke S3:
![alt text](<img (7).jpg>)
 5. Membuat REST API
 ![alt text](<img (8).jpg>)
 6. Mendapatkan Root Resource ID
 ![alt text](<img (9).jpg>)
 7.Membuat Resource untuk Data Ingestion
 ![alt text](<img (10).jpg>)
 8. Membuat Metode POST
 ![alt text](<img (11).jpg>)
 9. Membuat dan Mengonfigurasi Fungsi Lambda
 ![alt text](<img (12).jpg>)
 10.   Mengintegrasikan API Gateway dengan Lambda
 ![alt text](<img (13).jpg>)
 11. Menyebarkan API
 ![alt text](<img (14).jpg>)
12.  Mengirim Data Uji ke Endpoint
 ![alt text](<img (15).jpg>)
 13. Membuat Tabel DynamoDB
 ![alt text](<img (16).jpg>)
 14.  Memverifikasi Data di DynamoDB
 ![alt text](<img (17).jpg>)
 ### Monitoring dan Analisis Data
  1: Membuat Dashboard dengan Flask
  ![alt text](<img (18).jpg>)
  -  Buat File dashboard.py
![alt text](<img (20).jpg>)
  - Hasil Web 
  ![alt text](<img (19)-1.jpg>)

F. Kesimpulan 
Penggunaan LocalStack memungkinkan pengembang untuk menyimulasikan berbagai layanan AWS secara lokal tanpa biaya dan tanpa perlu koneksi internet ke cloud AWS. Melalui simulasi layanan seperti S3, Lambda, DynamoDB, dan API Gateway, proses pengembangan dan pengujian dapat dilakukan dengan lebih cepat, fleksibel, dan efisien. LocalStack sangat berguna dalam membangun dan menguji sistem cloud-native secara lokal sebelum diterapkan di lingkungan produksi. Praktikum ini membuktikan bahwa LocalStack dapat menjadi alat yang efektif dalam mendukung pengembangan aplikasi berbasis AWS secara mandiri dan hemat sumber daya.
