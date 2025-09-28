# Minpro2
Nama : Yuzar Rahmat Rafi Alhaq, Nim : 2509116025, Sistem Informasi A '2025
# Flowchart
<img width="1956" height="2217" alt="Flowchart sistem manajemen progress game drawio" src="https://github.com/user-attachments/assets/467b195e-2066-4e5d-bed0-c8a0c8d8bc6b" />

# Penjelasan Error
<img width="783" height="391" alt="image" src="https://github.com/user-attachments/assets/e88fc4a8-5688-4a90-9966-ce2b218816fd" />
(KeyboardInterrupt) Error ketika kita mencoba untuk menggunakan ctrl+c/fungsi keyboard yang mengganggu proses input
<img width="655" height="361" alt="image" src="https://github.com/user-attachments/assets/26b915d2-bcda-4707-8b91-3dc58f4bc56d" />
(ValueError) Error Ketika input yang harus menggunakan integer/angka diisi dengan input lain yang bukan angka
<img width="880" height="67" alt="image" src="https://github.com/user-attachments/assets/2fa2ec09-0b7b-488d-9dba-242172278206" />
(BaseException) Sebagai pengendalian/pemberitahuan ketika terjadi Error yang tidak diketahui dari program saya

# Penjelasan 
# Menu AwAL
<img width="428" height="193" alt="image" src="https://github.com/user-attachments/assets/620a22d4-a3ec-4db5-87ac-cafa28d4749e" />
Menu awal Ketika program dijalankan

# Memilih Login
<img width="631" height="467" alt="image" src="https://github.com/user-attachments/assets/42fe3b4d-38ea-40b9-beca-4a60f5594b50" />
<img width="802" height="399" alt="image" src="https://github.com/user-attachments/assets/8b7a97ae-d894-4490-8a2f-c692f530a777" />
Ini adalah tampilan ketika Login ketika menjadi admin dan ketika menjadi user

# Admin

# Penjelasan Pilihan 1
<img width="466" height="228" alt="Menu 1 Valid progres" src="https://github.com/user-attachments/assets/3f4db82e-3136-4b5e-ab2f-00310faa5615" />
<img width="427" height="225" alt="Menu 1 Invalid non angka progres" src="https://github.com/user-attachments/assets/5e99c21c-1243-4157-b8bc-882dff95d831" />
<img width="386" height="237" alt="Menu 1 Invalid not in range progres" src="https://github.com/user-attachments/assets/a083ee68-9e39-47f7-8ff0-2b991bff83fd" />
saat memilih pilihan 1, akan diminta mengisi input dan progress. setelah menginput judul dan input progress yang benar(%), judul akan langsung dimasukkan dalam list [Game_List] sebagai variabel dan tersimpan.
Sedangkan, saat menginput progress nya salah, yaitu menggunakan selain angka dan tidak di antara 0-100, sistem akan membatalkan proses dan mengembalikan tampilan menjadi menu pilihan.

# Penjelasan Pilihan 2
<img width="523" height="268" alt="Menu 2 Valid" src="https://github.com/user-attachments/assets/0dcc18d8-fde3-466a-95b6-b555547c5760" />
Saat memilih pilihan 2, program akan menampilkan list[Game_List]

# Penjelasan Pilihan 3
<img width="484" height="361" alt="Menu 3 Valid progres baru" src="https://github.com/user-attachments/assets/84d163be-b1db-4509-ad5b-e41476c6d026" />
<img width="602" height="340" alt="Menu 3 non angka" src="https://github.com/user-attachments/assets/529a2634-d2a6-40e8-9935-c5d76df45ca5" />
<img width="613" height="351" alt="Menu 3 Invalid angka not in range" src="https://github.com/user-attachments/assets/dcd363d1-b5ce-45fb-b719-d6f3a8e6e700" />
<img width="610" height="198" alt="Menu 3 Invalid, Seperti error progress pada menu 1" src="https://github.com/user-attachments/assets/78a398e7-7ca4-462b-8546-abbd70344fbd" />
Saat memilih pilihan 3, Program akan meminta untuk menginput nomor pilihan game mana yang akan di update progress nya sesuai urutan index (-1). jika input yang diisi salah(bukan angka/tidak dalam jangkauan total variabel dalam list), maka proses akan dibatalkan dan tampilan akan kembalikan ke menu pilihan.  jika input benar, akan diminta untuk mengisi input progress baru. Input Progress baru yang salah akan memiliki alur yang sama seperti saat menginput progress yang salah pada pilihan 1. Input progress baru yang benar akan menambah variael pada list sebagai "progress baru".

 # Penjelasan Pilihan 4
 <img width="598" height="351" alt="Menu 4 Valid hapus" src="https://github.com/user-attachments/assets/86444401-c1ec-4583-8b13-8186e7f3f830" />
<img width="619" height="363" alt="Menu 4 Invalid, seperti error input pada menu 3" src="https://github.com/user-attachments/assets/c123ea9c-55c2-4fea-9c5a-024c78e2f10d" />
Saat memilih pilihan 4,  Program akan meminta untuk menginput nomor pilihan game mana yang akan di hapus(.pop) sesuai urutan index (-1). jika input yang diisi salah(bukan angka/tidak dalam jangkauan total variabel dalam list), maka proses akan dibatalkan dan tampilan akan kembalikan ke menu pilihan. Jika input benar, maka program akan mengapus(.pop) game pada list [Game_List] dan menjadi bagian dari variabel pada list [game_terhapus]. 

# Penjelasan Pilihan 5 
<img width="774" height="399" alt="image" src="https://github.com/user-attachments/assets/2c2f0f80-8877-4ab9-869d-52bb267e6da2" />

Saat memilih Pilihan 5, Program akan akan kembali menampilkan menu awal yaitu menu login dan keluar

# Kondisi-kondisi tambahan - Belum ada game yang ditambahkan
<img width="425" height="193" alt="Invalid menu 2-4, list kosong, belum  di isi" src="https://github.com/user-attachments/assets/816e0eb9-78e5-4b43-a36d-c6cbc7df2c1e" />
Saat memilih pilihan antara 2-4, tetapi belum ada game yang ditambahkan pada list, maka program akan menampilkan ulang menu pilihan dan memberitahu bahwa belum ada game yang ditambahkan.

# Kondisi-kondisi tambahan - menginput pilihan diluar dari angka (1-5) pada menu pilihan
<img width="405" height="357" alt="Input menu invalid, dan perluangan atau looping" src="https://github.com/user-attachments/assets/1d06a97d-dd3a-4431-b062-7468d96d16fd" />
Saat menginput pilihan diluar dari angka (1-5) pada menu pilihan, maka program akan menampilkan ulang menu pilihan dan memberikan pemberitahuan input invalid.
