# Tugas-Mata-Kuliah-Sistem-Operasi-
Membuat kalkulator dilinux

def kalkulator():
    print("Pilih operasi:")
    print("1. Tambah")
    print("2. Kurang")
    print("3. Kali")
    print("4. Bagi")

    pilihan = input("Masukkan pilihan (1/2/3/4): ")

    if pilihan in ('1', '2', '3', '4'):
        angka1 = float(input("Masukkan angka pertama: "))
        angka2 = float(input("Masukkan angka kedua: "))

        if pilihan == '1':
            hasil = angka1 + angka2
            operasi = "+"
        elif pilihan == '2':
            hasil = angka1 - angka2
            operasi = "-"
        elif pilihan == '3':
            hasil = angka1 * angka2
            operasi = "*"
        elif pilihan == '4':
            if angka2 == 0:
                print("Error! Pembagian dengan nol tidak diperbolehkan.")
                return
            hasil = angka1 / angka2
            operasi = "/"

        print(f"Hasil: {angka1} {operasi} {angka2} = {hasil}")
    else:
        print("Pilihan tidak valid!")

while True:
    kalkulator()
    lanjut = input("Ingin menghitung lagi? (y/n): ").lower()
    if lanjut != 'y':
        print("Terima kasih telah menggunakan kalkulator!")
        break

        
