Penjelasan tiap baris pemrograman

import java.util.Scanner;     (Mengimpor kelas Scanner dari java.util untuk membaca input dari pengguna)

public class Soal1Tim5 {      (Mendeklarasikan kelas utama dengan nama Soal1Tim5)

    public static void main(String[] args) { (Method main adalah titik awal eksekusi program)

Scanner scanner = new Scanner(System.in); (Membuat objek Scanner untuk membaca input dari pengguna melalui konsol)

String[] cabangOlahraga = {"Badminton", "Basket", "Bola Voli"}; (Membuat array cabangOlahraga yang berisi: "Badminton", "Basket", dan "Bola Voli")

String[] atlet = new String[18]; (Membuat array atlet dengan ukuran 18 untuk menyimpan nama-nama atlet)

for (int i = 0; i < cabangOlahraga.length; i++) {
    System.out.println("Masukkan nama atlet untuk cabang " + cabangOlahraga[i] + ":"); (Perulangan for pertama "i" digunakan untuk mengakses setiap cabang olahraga)

for (int j = 0; j < 2; j++) { 
        System.out.println("Politeknik " + (j + 1) + ":"); (Perulangan for kedua "j" digunakan untuk mewakili dua politeknik yang berpartisipasi)

for (int k = 0; k < 3; k++) {  (perulangan for ketiga "k" digunakan untuk meminta tiga nama atlet dari setiap politeknik)

String namaAtlet; (Variabel namaAtlet menyimpan input pengguna)

            do {  (Menggunakan do-while untuk memaksa pengguna memasukkan nama atlet yang tidak kosong)
                System.out.print("Atlet " + (k + 1) + ": ");
                namaAtlet = scanner.nextLine();

                if (namaAtlet.isEmpty()) {  (Jika pengguna memasukkan string kosong " ", maka akan muncul pesan error dan meminta input ulang)
                    System.out.println("Nama atlet tidak boleh kosong. Silakan masukkan lagi.");
                }
            } while (namaAtlet.isEmpty());

 atlet[k] = namaAtlet; (Menyimpan nama atlet ke dalam array atlet, tapi hanya menggunakan indeks k, yang akan menyebabkan data ditimpa di setiap iterasi)

System.out.println("\nInformasi Nama Atlet:"); (Menampilkan header untuk daftar nama atlet)

for (int i = 0; i < cabangOlahraga.length; i++) { (Perulangan for pertama "i" untuk menampilkan data berdasarkan cabang olahraga)
    System.out.println("Cabang " + cabangOlahraga[i] + ":");

for (int j = 0; j < 2; j++) { (Perulangan for kedua "j" untuk menampilkan politeknik yang berpartisipasi)
        System.out.println("Politeknik " + (j + 1) + ":");

for (int k = 0; k < 3; k++) { (Perulangan for ketiga "k" untuk menampilkan atlet)
            System.out.println("Atlet " + (k + 1) + ": " + atlet[k]);
        }

scanner.close(); (Menutup objek Scanner untuk mencegah kebocoran sumber daya)
