# AplikasiPenambahanDuaAngka
 Latihan 1-Muhammad Azhari Nur Pratama-2210010326

## 1. Deskripsi Program:
  • Pengguna memasukkan dua angka
• Saat tombol Tambah diklik akan menampilkan hasil pertambahan
• Saat tombol Hapus diklik akan menghapus nilai di TextField dan
mengarahkan fokus ke TextField angka pertama

## 2. Komponen GUI: 
JFrame, JPanel, JLabel, JTextField, JButton

## 3. Logika Program: 
Penambahan dua angka, validasi input numerik

## 4. Events:
-ActionListener untuk tombol Tambah, Hapus, dan Keluar
A.Tambah
```
private void btnTambahActionPerformed(java.awt.event.ActionEvent evt) {                                          
       try {
        int angka1 = Integer.parseInt(Angka1.getText());
        int angka2 = Integer.parseInt(Angka2.getText());
        int hasil = angka1 + angka2;
        Hasil.setText(" " + hasil);
```
B.Hapus
```
private void btnHapusActionPerformed(java.awt.event.ActionEvent evt) {                                         
     Angka1.setText("");
     Angka2.setText("");
     Hasil.setText("");
     Angka1.requestFocus();
    }  
```
C.Keluar
```
private void btnKeluarActionPerformed(java.awt.event.ActionEvent evt) {                                                 
        System.exit(0);
    }
```
## 5. Variasi:
A.KeyAdapter pada JTextField untuk membatasi input hanya angka
   ```
               char karakter = evt.getKeyChar();
    // Memeriksa apakah karakter bukan angka
    if (!Character.isDigit(karakter)) {
        evt.consume(); // Mengabaikan karakter non-angka
    }
```
B.Gunakan JOptionPane untuk menampilkan error input
```
} catch (NumberFormatException e) {
        JOptionPane.showMessageDialog(this, "Input harus berupa angka!", "Error", JOptionPane.ERROR_MESSAGE);
    }
```
C.Implementasikan FocusListener untuk membersihkan JTextField
saat mendapatkan fokus.
   ```
 private void txtAngka1FocusGained(java.awt.event.FocusEvent evt) {                                      
         Angka1.setText("");
    }                                  
```
## Contoh Gambar Project Setelah di Run
![](https://github.com/Azharipratama09/AplikasiPenambahanDuaAngka/blob/main/Cuplikan%20layar%202024-11-03%20220536.png)
    

## Indikator Penilaian:

| No  | Komponen         |  Persentase  |
| :-: | --------------   |   :-----:    |
|  1  | Komponen GUI     |    20    |
|  2  | Logika Program   |    20    |
|  3  | Kesesuaian UI    |    15    |
|  4  | Constructor      |    15    |
|  5  | Memenuhi Variasi |    30    |
|     | TOTAL        | 100 |

## Pembuat

Nama:Muhammad Azhari Nur Pratama
NPM:2210010326
