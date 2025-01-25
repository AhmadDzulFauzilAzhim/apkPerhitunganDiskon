# Aplikasi PerhitunganDiskon
 
Aplikasi `apkPerhitunganDiskon` adalah sebuah aplikasi desktop berbasis Java Swing untuk membantu pengguna menghitung diskon pada suatu harga barang. Aplikasi ini menyediakan berbagai fitur untuk menghitung harga akhir setelah diskon, termasuk penghematan yang diperoleh, serta mendukung penggunaan kode kupon untuk diskon tambahan.

---

## Fitur Utama
1. **Input Harga Asli:**
   - Pengguna dapat memasukkan harga asli barang dalam kolom input.

2. **Input Kode Kupon:**
   - Mendukung kode kupon "10" untuk diskon tambahan sebesar 10%.
   - Jika kode kupon tidak valid, pengguna akan menerima notifikasi.

3. **Pengaturan Diskon dengan Slider dan ComboBox:**
   - Persentase diskon dapat disesuaikan dengan slider atau combo box.
   - Nilai slider dan combo box akan otomatis tersinkronisasi.

4. **Output Harga Akhir dan Penghematan:**
   - Menampilkan harga akhir setelah diskon serta jumlah penghematan.

5. **Log Hasil Perhitungan:**
   - Semua hasil perhitungan ditampilkan dalam area teks untuk referensi lebih lanjut.

---

## Cara Menggunakan

1. **Buka Aplikasi:**
   - Jalankan file `.jar` atau gunakan IDE seperti NetBeans/IntelliJ IDEA untuk menjalankan proyek.

2. **Masukkan Harga Asli:**
   - Isi kolom "Harga Asli" dengan harga barang yang ingin dihitung.

3. **Pilih Persentase Diskon:**
   - Atur slider untuk memilih persentase diskon, atau pilih dari combo box.

4. **Masukkan Kode Kupon (Opsional):**
   - Jika memiliki kode kupon, masukkan dalam kolom "Kupon Diskon".
   - Gunakan kode kupon "10" untuk mendapatkan diskon tambahan 10%.

5. **Klik Tombol Hitung:**
   - Klik tombol "Hitung" untuk mendapatkan harga akhir dan penghematan.

6. **Lihat Hasil:**
   - Harga akhir, penghematan, dan log hasil perhitungan akan ditampilkan.

---

## Komponen Utama

- **JLabel:** Label untuk menampilkan deskripsi setiap kolom atau elemen.
- **JTextField:** Input untuk harga asli, kode kupon, harga akhir, dan penghematan.
- **JSlider:** Slider untuk memilih persentase diskon.
- **JComboBox:** Dropdown untuk memilih persentase diskon secara cepat.
- **JButton:** Tombol untuk memproses perhitungan diskon.
- **JTextArea:** Area teks untuk menampilkan log hasil perhitungan.
- **JPanel:** Panel utama untuk mengatur tata letak komponen.

---

## Alur Perhitungan

1. **Menghitung Jumlah Diskon:**
   ```java
   double jumlahDiskon = hargaAsli * persentaseDiskon / 100.0;
   ```

2. **Mengurangi Harga Asli dengan Diskon:**
   ```java
   double hargaSetelahDiskon = hargaAsli - jumlahDiskon;
   ```

3. **Memproses Kode Kupon:**
   ```java
   if (kodeKupon.equals("10")) {
       diskonTambahan = hargaSetelahDiskon * 0.10;
       hargaSetelahDiskon -= diskonTambahan;
   }
   ```

4. **Menampilkan Hasil:**
   ```java
   jTextField3.setText(String.format("Rp %.2f", hargaSetelahDiskon));
   jTextField4.setText(String.format("Rp %.2f", jumlahDiskon + diskonTambahan));
   ```

---

## Validasi Input
- Memastikan harga asli dan persentase diskon hanya menerima angka.
- Menampilkan pesan kesalahan jika input tidak valid menggunakan `JOptionPane`:
  ```java
  JOptionPane.showMessageDialog(this, "Masukkan angka yang valid!", "Error", JOptionPane.ERROR_MESSAGE);
  ```

---

## Cara Menjalankan Proyek

1. Pastikan Java Development Kit (JDK) sudah terinstal.
2. Buka proyek ini di IDE (NetBeans, IntelliJ IDEA, atau Eclipse).
3. Jalankan file `apkPerhitunganDiskon.java` sebagai aplikasi Java.
4. Alternatif, build proyek menjadi file `.jar` dan jalankan dari terminal:
   ```
   java -jar apkPerhitunganDiskon.jar
   ```

---

## Catatan 
- Gunakan kode kupon yang valid untuk menghindari error.
- Input harus berupa angka untuk memastikan perhitungan berjalan dengan benar.

---

## Pembuat Aplikasi
Ahmad Dzul Fauzil Azhim - 2210010389

## Demo

![App Screenshot](https://github.com/AhmadDzulFauzilAzhim/apkPerhitunganDiskon/blob/main/img/demo%20aplikasi%20perhitungan%20diskon.gif)
