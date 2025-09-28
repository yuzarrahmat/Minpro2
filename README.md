# Minpro2
Nama : Yuzar Rahmat Rafi Alhaq, Nim : 2509116025, Sistem Informasi A '2025
# Flowchart
<img width="1956" height="2217" alt="Flowchart sistem manajemen progress game drawio" src="https://github.com/user-attachments/assets/467b195e-2066-4e5d-bed0-c8a0c8d8bc6b" />
# Codingan

#Program Sistem Manajemen Progress Game 
game_list = []  # Ini adalah List Game yang Saat Ini Ku Mainkan
pilihan = [] # Menampung data
#--------------------------------------------------------------------------------------
#Fungsi Login
def login_admin():
    admin = {"username": "admin", "password": "admin123"}
    try:
        input_username = input("Masukkan username: ")
        input_password = input("Masukkan password: ")
        if input_username == admin["username"] and input_password == admin["password"]:
            print("Login berhasil!")
            main_admin()
        else:
            print("Login gagal! Silakan coba lagi.")
            login_system()
    except KeyboardInterrupt:
        print("\nERROR: Anda jangan pake ctrl+c dong")
    except BaseException:
        print("Terjadi kesalahan tak diketahui")

def login_user():
    user = {"username": "user", "password": "user123"}
    try:
        input_username = input("Masukkan username: ")
        input_password = input("Masukkan password: ")
        if input_username == user["username"] and input_password == user["password"]:
            print("Login berhasil!")
            main_user()
        else:
            print("Login gagal! Silakan coba lagi.")
        login_system()
    except KeyboardInterrupt:
        print("\nERROR: Anda jangan pake ctrl+c dong")
    except BaseException:
        print("Terjadi kesalahan tak diketahui")

#--------------------------------------------------------------------------------------
#Fungsi Utama Admin
def main_admin():
    while True:
        print("\n=== SISTEM MANAJEMEN PROGRESS GAME ===")
        print("1. Tambah Game Baru")
        print("2. Lihat Daftar Game")
        print("3. Update Progress Game")
        print("4. Hapus Game")
        print("5. Logout")

        pilihan = input("Pilih menu (1-5): ")
        if pilihan == '1':
            # Menambah game baru
            judul = input("Judul Game: ")
            try:
                progress = int(input("Progress (%): "))
                if progress < 0 or progress > 100:
                    print("Progress harus antara 0-100%!")
                    continue
            except ValueError:
                print("Progress harus berupa angka!")
                continue
                
            # Tentukan status berdasarkan progress
            if progress == 0:
                status = "Baru Dimulai"
            elif progress == 100:
                status = "Sudah Tamat/Selesai"
            else:
                status = "Lagi Dimainkan"
                
            # Simpan sebagai tuple dalam list
            game_baru = (judul, progress, status)
            game_list.append(game_baru)
            print("Game ", judul, "berhasil ditambahkan!")
            
        elif pilihan == '2':
            # Menampilkan daftar game ku
            if not game_list:
                print("Belum ada game yang ditambahkan.")
            else:
                print("\nDAFTAR GAME:")
                print("=" * 45 * len(game_list))
                print(game_list)
                print("=" * 45 * len(game_list))
        elif pilihan == '3':
            # Update progress game ku
            if not game_list:
                print("Belum ada game yang ditambahkan.")
                continue
                
            # Tampilkan game untuk dipilih
            print("\nPilih game yang akan diupdate:")
            print("=" * 45 * len(game_list))
            print(game_list)
            print("=" * 45 * len(game_list))
            print("Input = 1, 2, 3, dst sesuai urutan game di list")
            
            try:
                pilihan = int(input("Nomor game: ")) - 1
                if 0 <= pilihan < len(game_list):
                    try:
                        progress_baru = int(input("Progress baru (%): "))
                        if progress_baru < 0 or progress_baru > 100:
                            print("Progress harus antara 0-100%!")
                            continue
                    except ValueError:
                        print("Progress harus berupa angka!")
                        continue
                        
                    # Update status berdasarkan progress baru
                    if progress_baru == 0:
                        status_baru = "Baru Dimulai"
                    elif progress_baru == 100:
                        status_baru = "Sudah Tamat/Selesai"
                    else:
                        status_baru = "Lagi Dimainkan"
                        
                    # Update data game
                    game_list[pilihan] = (game_list[pilihan][0], game_list[pilihan][1], game_list[pilihan][2], progress_baru, status_baru)
                    print("Progress game berhasil diupdate!")
                else:
                    print("Nomor tidak valid!")
            except ValueError:
                print("Input harus berupa angka!")
                
        elif pilihan == '4':
            # Hapus game dari List  
            if not game_list:
                print("Belum ada game yang ditambahkan.")
                continue
                
            # Tampilkan game untuk dipilih
            print("\nPilih game yang akan dihapus:")
            print("=" * 45 * len(game_list))
            print(game_list)
            print("=" * 45 * len(game_list))
            print("Input = 1, 2, 3, dst sesuai urutan game di list")
            try:
                pilihan = int(input("Nomor game: ")) - 1
                if 0 <= pilihan < len(game_list):
                    game_terhapus = game_list.pop(pilihan)
                    print("Game ", game_terhapus[0], "berhasil dihapus!")
                else:
                    print("Nomor tidak valid!")
            except ValueError:
                print("Input harus berupa angka!")
        elif pilihan == '5':
            print("Logout berhasil.")
            login_system()
        else:
            print("Pilihan tidak valid. Silakan pilih 1-5.")
#Fungsi Utama User
def main_user():
    while True:
        print("\n=== SISTEM MANAJEMEN PROGRESS GAME ===")
        print("1. Lihat Daftar Game")
        print("2. logout")
        try:
            pilihan = input("Pilih menu (1-2): ")
            if pilihan == '1':
                # Menampilkan daftar game ku
                if not game_list:
                    print("Belum ada game yang ditambahkan.")
                else:
                    print("\nDAFTAR GAME:")
                    print("=" * 45 * len(game_list))
                    print(game_list)
                    print("=" * 45 * len(game_list))
            elif pilihan == '2':
                print("Logout berhasil.")
                login_system()
        except KeyboardInterrupt:
            print("\nERROR: Anda jangan pake ctrl+c dong")
            main_user()
        except BaseException:
            print("Terjadi kesalahan tak diketahui")
            main_user()
#--------------------------------------------------------------------------------------
#login system
def login_system():
    while True:
        print("=== SELAMAT DATANG DI SISTEM MANAJEMEN PROGRESS GAME ===")
        print("1. Login sebagai Admin")
        print("2. Login sebagai User")
        print("3. Keluar")
        try:
            pilihan = input("Pilih opsi (1-3): ")
            if pilihan == '1':
                login_admin()
            elif pilihan == '2':
                login_user()
            elif pilihan == '3':
                print("Mantap, jangan lupa deadline tugas bosku.")
                break
            else:
                print("Pilihan tidak valid. Silakan pilih 1-3.")
                login_system()
        except KeyboardInterrupt:
            print("\nERROR: Anda jangan pake ctrl+c dong")
            login_system()
        except BaseException:
            print("Terjadi kesalahan tak diketahui")
            login_system()
#--------------------------------------------------------------------------------------
login_system()

# Penjelasan Error
