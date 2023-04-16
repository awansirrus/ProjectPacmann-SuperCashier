# ProjectPacmann-SuperCashier
SuperCashier adalah program self-service cashier supermarket sederhana yang memungkinkan costumer menginputkan item, jumlah dan harga yang ingin dibeli.

# Background
Seorang pemilik supermarket di suatu kota ingin melakukan perbaikan proses bisnis dengan cara membuat self-service kasir. Jadi, customer dapat membeli barang dari supermarket secara langsung mulai dari menginputkan pesanannya, memasukkan jumlah item, dan memasukkan harga belanjaannya. Jadi supermarket tersebut dapat menjangkau pasar yang lebih luas karena customer di luar kota tersebut dapat membeli barang-barang dari supermarketnya.

# Feature Requirements
1. Customer dapat menginput id-nya
2. Customer dapt menginput nama item, jumlah item, dan harga item
3. Jika ada kesalahan input, maka customer dapat:

    a. Update nama item
    
    b. Update jumlah item
    
    c. Update harga item
    
4. Jika batal item belanjaan, maka customer:
    a. Hapus salah satu item
    b. Langsung hapus transaksi/reset transaksi
5. Jika sudah selesai, customer mengecek list belanja
6. Pembeli mengecek total harga

# Flowcharts
<img width="545" alt="flowchart" src="https://user-images.githubusercontent.com/130228426/232286078-2fa13fc6-d816-4917-b2ca-b28e82a6ec97.png">

# Penjelasan Fungsi
SuperCashier terdiri dari dua file program, main.py dan SuperCashier.py. File main.py merupakan file utama yang dijalankan oleh user. Disini user dapat memasukkan user id nya.

![gambar](https://user-images.githubusercontent.com/130228426/232287189-b6ddf243-39c1-4111-a6e6-6c7791fc25b0.png)

Sedangkan SuperCashier.py berisi modul Transaction yang di-import oleh file main.py. Pada file SuperCashier.py terdapat beberapa method, diantaranya adalah:
1. Class Transaction


   ![gambar](https://user-images.githubusercontent.com/130228426/232287634-4915e712-70da-4c75-a14b-41d0a81f606a.png)


2. add_item()

    ![gambar](https://user-images.githubusercontent.com/130228426/232287861-ef197f33-28d4-465f-87a2-2f014cef6b4e.png)

3. delete_item()

    ![gambar](https://user-images.githubusercontent.com/130228426/232288097-851dc5d1-e0ae-4825-a463-f8b261f37841.png)

4. update_item_name() , update_item_qty() , update_item_price()

    ![gambar](https://user-images.githubusercontent.com/130228426/232288293-4e5a83eb-dd0c-441b-ad2a-a05669329fee.png)

5. check_order()

   ![gambar](https://user-images.githubusercontent.com/130228426/232288426-c777d69d-33e2-48c8-94ab-f84206dfcf16.png)

6. total_price(). Memiliki fungsi untuk menghitung total belanjaan pelanggan beserta dengan diskonnya. Diskon yang diperoleh pelanggan akan mengikuti            ketentuan sebagai berikut. 

    Jika total belanja diatas Rp 200.000 maka akan mendapatkan diskon 5%. 
    
    Jika total belanja diatas Rp 300.000 maka akan mendapatkan diskon 8%. 
    
    Jika total belanja diatas Rp 500.000 maka akan mendapatkan diskon 10%

   ![gambar](https://user-images.githubusercontent.com/130228426/232288890-6751e592-6aa5-4eb7-a343-390f107d3fbb.png)

7. reset_transaction()

   ![gambar](https://user-images.githubusercontent.com/130228426/232288985-3b0ec37d-6e9e-4556-bc07-27703adec5a9.png)


# Test Case
1. Saat awal program dijalankan, customer akan diminta memasukkan user id.

    ![gambar](https://user-images.githubusercontent.com/130228426/232309149-a8a4d6e6-0e90-4070-91ba-7f8ff1bcedf1.png)

2. Customer ingin menambahkan dua item baru menggunakan method add_item(). Item yang akan ditambahkan sebagai berikut:

    Nama Item: Ayam Goreng, Quantity 2, Harga: 20000. 
    
    Nama Item: Pasta Gigi, Quantity 3, Harga: 15000

    ![gambar](https://user-images.githubusercontent.com/130228426/232309606-c2e90d6a-2b9c-4cff-ad1f-866865daedc5.png)

3. Customer ingin menghapus salah satu item yang sudah ditambahkan menggunakan method delete_item(). Item yang akan dihapus adalah item Pasta Gigi.

    ![gambar](https://user-images.githubusercontent.com/130228426/232310103-9d87840f-3e67-49f9-9077-5d2a20fc8d92.png)
   
    ![gambar](https://user-images.githubusercontent.com/130228426/232309898-c5561032-d9cd-469f-9b5c-82d5ecb07c3e.png)
    
    
4. Customer ingin menghapus seluruh item yang telah diinput, method yang digunakan adalah reset_transaction().
    
    ![gambar](https://user-images.githubusercontent.com/130228426/232310940-c09d51e0-cd35-4f89-8deb-3bf8af2e79ba.png)
    
5. Customer menambahkan lagi item belanjanya yaitu berupa
    
    Item: Ayam Goreng, Quantity: 2, Harga: 20000
    
    Item: Pasta Gigi, Quantity: 3, Harga: 15000
    
    Item: Mainan Mobil, Quantity: 1, Harga: 200000
    
    Item: Mi Instan, Quantity: 5, Harga: 3000

    ![gambar](https://user-images.githubusercontent.com/130228426/232312347-a9b738ed-daab-4bfe-a414-4f443076d654.png)
    
6. Customer ingin menghitung total belanja yang telah ada pada keranjang menggunakan method total_price().

    ![gambar](https://user-images.githubusercontent.com/130228426/232312715-542be5b0-ef59-42f1-9135-fb57fa5976be.png)
    
    
# Conclusion / Future Work

Sistem kasir self service telah berjalan dengan baik dan berhasil melewati beberapa test case. Selain itu, sistem kasir self service masih dapat dilakukan berbagai pengembangan agar code dapat berjalan lebih efektif dan efesien. Kedepannya perlu dibangun database harga untuk menghindari fraud serta untuk menyimpan data transaksi setiap pembeli. Perlu membangun GUI agar semakin user-friendly.




