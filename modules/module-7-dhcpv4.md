# 📘 CCNA: Switching, Routing, and Wireless Essentials – Module 7: DHCPv4

**Platform**: [Cisco Networking Academy](https://www.netacad.com)  
**Tanggal Belajar**: 2025-06-23  
**Tipe Pembelajaran**: Instructor-led  
**Instruktur**: **Ziad Sobri**  
**Institusi**: Universitas Mitra Indonesia

---

## 🎯 Tujuan Modul

- Menerapkan *DHCPv4* agar dapat beroperasi pada beberapa jaringan *LAN*.

---

## 🗂️ Ringkasan Materi

### 🔸 Submodul 1: Pendahuluan

- Tinjauan awal terhadap konsep dan topik utama yang dibahas dalam modul ini.

### 🔸 Submodul 2: Konsep DHCPv4

- *Dynamic Host Configuration Protocol version 4 (DHCPv4)* merupakan protokol jaringan yang memungkinkan alokasi alamat *IPv4* dan parameter konfigurasi jaringan lainnya secara dinamis dan otomatis. Penggunaan *DHCP* sangat membantu dalam mengurangi beban konfigurasi manual oleh administrator jaringan.
- Proses penyewaan alamat dimulai ketika *klien* mengirimkan permintaan ke *server DHCPv4*. *Server* kemudian merespons dengan memberikan alamat *IPv4* beserta informasi jaringan lainnya yang diperlukan.
- *DHCPv4* dapat berfungsi sebagai *server* maupun *klien*, tergantung konfigurasi perangkat.
- Tahapan dalam proses penyewaan meliputi:
  - **DHCP Discover (DHCPDISCOVER)**: *Klien* mengirim pesan *broadcast* menggunakan alamat *MAC* untuk mencari *server DHCP*.
  - **DHCP Offer (DHCPOFFER)**: *Server* merespons permintaan dan menawarkan alamat *IPv4* yang tersedia.
  - **DHCP Request (DHCPREQUEST)**: *Klien* mengajukan permintaan terhadap alamat yang ditawarkan untuk keperluan awal penyewaan maupun perpanjangan.
  - **DHCP Acknowledgment (DHCPACK)**: *Server* memverifikasi dan mengonfirmasi bahwa informasi penyewaan telah diterima dan valid.
- Untuk proses perpanjangan sewa, *klien* akan mengirim ulang pesan *DHCPREQUEST* langsung ke *server DHCPv4* yang sebelumnya menawarkan alamat. Selanjutnya, *server* memverifikasi kembali melalui pesan *DHCPACK*.

### 🔸 Submodul 3: Konfigurasi Server DHCPv4 Cisco IOS

- Langkah-langkah konfigurasi meliputi:
  - Mengecualikan alamat *IPv4* tertentu dari jangkauan penyewaan.
  - Menetapkan nama *DHCP pool*.
  - Mengatur parameter konfigurasi pada *DHCP pool* yang dibuat.
- Perintah-perintah yang digunakan untuk memverifikasi operasi *DHCPv4*:
  - `show running-config | section dhcp`
  - `show ip dhcp binding`
  - `show ip dhcp server statistics`
  - `ipconfig /all` (digunakan pada *Windows Client*)
- Perintah `no service dhcp` di *global configuration mode* berfungsi untuk menonaktifkan layanan *DHCP*.
- Perintah `ip helper-address` digunakan pada antarmuka *router* untuk mengaktifkan fungsi *DHCP Relay*.

### 🔸 Submodul 4: Konfigurasi Klien DHCPv4

- Perintah `ip address dhcp` digunakan untuk mengonfigurasi antarmuka *router* sebagai *DHCP Client*.

---

## 🌐 Praktik / Simulasi

- 🖥️ **Lab**: Configure DHCPv4  
- 🔧 **Tools**: *Packet Tracer*, *CLI*, *Utilitas Ping*  
- 🔄 **Hasil**: Konfigurasi *DHCPv4 Server*, *Client*, dan *Relay* berhasil dilakukan pada masing-masing *router* untuk mendukung kebutuhan host di dalam jaringan *LAN*.  
- 📁 **File Lab**: [Configure DHCPv4 PKA File](../labs/module-7/7.2.10-packet-tracer---configure-dhcpv4.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Implement DHCPv4  
- 🔧 **Tools**: *Packet Tracer*, *CLI*, *Utilitas Ping*  
- 🔄 **Hasil**: Implementasi penuh *DHCPv4 Server*, *Client*, dan *Relay* telah dilakukan secara tepat pada setiap *router*, untuk mendukung pengalamatan dinamis dalam jaringan *LAN*.  
- 📁 **File Lab**: [Implement DHCPv4 PKA File](../labs/module-7/7.4.1-packet-tracer---implement-dhcpv4.pka) - ✅ 100% selesai

---

## 🧠 Catatan Pribadi

💬 Dalam beberapa skenario, *router* yang bertindak sebagai *DHCP server* tidak berada dalam *subnet* yang sama dengan *klien*. Karena *klien* menggunakan pesan *broadcast* untuk menemukan layanan *DHCP*, maka antarmuka *router* yang terhubung ke jaringan tempat *klien* berada harus dikonfigurasi sebagai *DHCP Relay*. Dengan demikian, pesan *broadcast* dari *klien* dapat diteruskan ke *server DHCP*, sehingga alamat dapat diberikan dengan benar kepada *klien* yang bersangkutan.

---

## 📎 Referensi Modul

- [Cisco Networking Academy](https://www.netacad.com)

---

> Ditulis oleh: **Ulil Akbar** pada 2025-06-23.
