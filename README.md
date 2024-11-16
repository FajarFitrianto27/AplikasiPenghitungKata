# AplikasiPenghitungKata
 Latihan 5 - (Muhammad Fajar Fitrianto_2210010748)
 
Kelas : 5B NonReg Banjarmasin


---

# Aplikasi PenghitungKataForm

## Gambaran Umum
**PenghitungKataForm** adalah aplikasi sederhana berbasis Java Swing yang menghitung jumlah kata, karakter, dan kalimat dalam teks yang diberikan. Aplikasi ini dirancang dengan antarmuka grafis pengguna (GUI) untuk memberikan pengalaman yang mudah digunakan bagi pengguna yang perlu menganalisis konten teks mereka.

## Fitur
- **Area input teks**: Pengguna dapat mengetik atau menempelkan teks ke dalam area teks utama.
- **Tombol Hitung**: Tombol yang diberi label "HITUNG" untuk memproses teks yang dimasukkan dan menampilkan hasilnya.
- **Tampilan hasil**: Menampilkan jumlah kata, karakter, dan kalimat.

## Penjelasan Kode
### Komponen Utama
- **Komponen GUI**:
  - `JPanel`, `JLabel`, `JTextArea`, `JButton` digunakan untuk membangun antarmuka pengguna.
- **Logika**:
  - Aplikasi ini menggunakan manipulasi string sederhana (`split`, `length`, dll.) untuk menghitung jumlah kata, karakter, dan kalimat.

### Metode Utama
Metode `public static void main(String[] args)` menginisialisasi aplikasi dengan memanggil `PenghitungKataForm()`.

### Potongan Kode Contoh
Berikut adalah potongan kode yang menunjukkan bagaimana logika utama untuk menghitung diterapkan:
```java
private void hitungButtonActionPerformed(java.awt.event.ActionEvent evt) {
    String teks = jTextArea.getText();
    String[] kata = teks.trim().split("\\s+");
    int jumlahKata = (teks.isEmpty()) ? 0 : kata.length;
    int jumlahKarakter = teks.length();
    String[] kalimat = teks.split("[.!?]");
    int jumlahKalimat = (teks.isEmpty()) ? 0 : kalimat.length;

    labelHasilKata.setText("Jumlah Kata: " + jumlahKata);
    labelHasilKarakter.setText("Jumlah Karakter: " + jumlahKarakter);
    labelHasilKalimat.setText("Jumlah Kalimat: " + jumlahKalimat);
}
```

## Cara Menjalankan
1. **Kompilasi**: Gunakan `javac PenghitungKataForm.java` untuk mengkompilasi file.
2. **Jalankan**: Jalankan program menggunakan `java PenghitungKataForm`.

## Persyaratan
- **Java SE Development Kit (JDK)** versi 8 atau lebih tinggi.
- **NetBeans IDE** atau IDE yang mendukung Java disarankan untuk pengembangan dan eksekusi yang lebih mudah.


---

