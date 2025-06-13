# 📘 CCNA: Switching, Routing, and Wireless Essentials – Module 2: Switching Concepts

**Platform**: [Cisco Networking Academy](https://www.netacad.com)  
**Tanggal Belajar**: 2025-06-13  
**Tipe Pembelajaran**: Instructor-led  
**Instruktur**: **Ziad Sobri**  
**Institusi**: Universitas Mitra Indonesia

* * *

## 🎯 Tujuan Modul

- Menjelaskan bagaimana switch layer 2 meneruskan data.

* * *

## 🗂️ Ringkasan Materi

### 🔸 Submodul 1: Pendahuluan

- Tinjauan topik pembelajaran.

### 🔸 Submodul 2: Penerusan Frame

- Ingress - Istilah untuk menggambarkan port tempat frame memasuki perangkat.
- Egress - Istilah untuk menggambarkan port yang akan digunakan frame saat meninggalkan perangkat.
- Switch meneruskan lalu lintas berdasarkan port ingress dan alamat MAC tujuan dari frame Ethernet.
- Switch mempelajari perangkat yang terhubung ke setiap port dan menyimpan alamat MAC-nya dalam MAC Address Table.
- Metode switch learn: Switch memeriksa alamat MAC sumber dari frame untuk membangun entri dalam MAC Address Table.
- Metode switch forward: Switch memeriksa alamat MAC dari perangkat tujuan yang terhubung ke port switch.
- Metode store-and-forward switching: Switch menerima seluruh frame, memverifikasi integritasnya menggunakan CRC, lalu meneruskan jika valid.
- Metode cut-through switching: Proses penerusan frame dimulai setelah alamat MAC tujuan dari frame yang masuk dan port keluar telah ditentukan.

### 🔸 Submodul 3: Domain tabrakan dan broadcast

- Switch digunakan untuk mengabaikan tabrakan dan mengurangi kemacetan.
- Secara default, switch menggunakan fitur autonegotiation untuk menentukan mode komunikasi (half/full-duplex).
- Switch tunggal menciptakan satu domain broadcast. Perangkat router digunakan untuk segmentasi hal tersebut.
- Fitur switch untuk mengurangi kemacetan: Kecepatan port yang cepat, kecepatan dalam switching internal, buffer frame yang besar, kepadatan port yang tinggi.

***

## 🌐 Praktik / Simulasi

- Tidak tersedia. 

***

## 🧠 Catatan Pribadi

💬 Perbedaan signifikan antara cut-through switching dengan store-and-forward switching terletak pada pengecekan kesalahan dan buffering otomatis. Store-and-forward switching menggunakan frame check sequence (FCS) dan memberikan fleksibilitas untuk mendukung kecepatan Ethernet apa pun, sehingga membutuhkan waktu dalam memutuskan penerusan frame. Sedangkan cut-through switching tidak melakukan pengecekan apa pun, sehingga frame dapat dikirimkan secepat mungkin.

*** 

## 📎 Referensi Modul
[Cisco Networking Academy](https://www.netacad.com)  

***

## 📄 Lisensi

Dokumentasi ini disusun berdasarkan proses belajar pribadi dari kursus Cisco Networking Academy dan **tidak menyertakan materi berbayar atau berlisensi resmi dari Cisco** seperti soal kuis, slide, atau konten tertutup lainnya.

Lisensi: [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/). Lihat detail lisensi di [LICENSE.md](./LICENSE.md)

* * *

> Ditulis oleh: **Ulil Akbar** pada 13 Juni 2025.
