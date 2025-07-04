## 📘 CCNA: Switching, Routing, and Wireless Essentials – Module 9: FHRP Concepts

**Platform**: [Cisco Networking Academy](https://www.netacad.com)
**Tanggal Belajar**: 2025-07-04
**Tipe Pembelajaran**: Instructor-led
**Instruktur**: **Ziad Sobri**
**Institusi**: Universitas Mitra Indonesia

---

## 🎯 Tujuan Modul

* Menjelaskan bagaimana *FHRP* menyediakan layanan *default gateway* dalam jaringan yang redundan.

---

## 🗂️ Ringkasan Materi

### 🔸 Submodul 1: Pendahuluan

* Memberikan gambaran umum mengenai topik yang akan dibahas dalam modul ini.

### 🔸 Submodul 2: *First Hop Redundancy Protocols*

* Jika antarmuka *router* atau perangkat *router* yang berfungsi sebagai *default gateway* mengalami kegagalan, maka *host* yang telah dikonfigurasi dengan *default gateway* tersebut akan terisolasi dari jaringan luar.
* Untuk menghindari titik kegagalan tunggal, diperlukan mekanisme penyedia *default gateway* alternatif pada jaringan yang memiliki dua atau lebih *router* yang terhubung dalam VLAN yang sama.
* Mekanisme ini difasilitasi oleh *First Hop Redundancy Protocols (FHRP)*.
* Salah satu pendekatan untuk mengatasi masalah tersebut adalah dengan menerapkan *router virtual* sebagai *default gateway*.
* Beberapa opsi *FHRP* yang tersedia di antaranya: *Hot Standby Router Protocol (HSRP)*, *HSRP for IPv6*, *Virtual Router Redundancy Protocol version 2 (VRRPv2)*, *VRRPv3*, *Gateway Load Balancing Protocol (GLBP)*, *GLBP for IPv6*, dan *ICMP Router Discovery Protocol (IRDP)*.

### 🔸 Submodul 3: *HSRP*

* *HSRP* digunakan dalam kelompok *router* untuk menentukan perangkat *aktif* dan *siaga*.
* Perangkat *aktif* adalah perangkat yang digunakan untuk *routing* lalu lintas jaringan.
* Perangkat *siaga* akan mengambil alih fungsi *routing* jika perangkat *aktif* mengalami kegagalan, atau ketika kondisi tertentu terpenuhi.
* Peran utama *router* siaga adalah memantau status operasional kelompok *HSRP* dan segera mengambil alih proses *packet-forwarding* jika *router* aktif gagal.
* Secara bawaan, nilai *prioritas HSRP* adalah 100. Jika dua *router* memiliki nilai prioritas yang sama, maka *router* dengan alamat IPv4 numerik tertinggi akan dipilih sebagai *router aktif*.
* *Preemption* adalah kemampuan *router* untuk memicu pemilihan ulang. Dengan fitur ini diaktifkan, *router* dengan prioritas lebih tinggi yang kembali aktif dapat langsung mengambil peran *router aktif*.
* Status dalam proses kerja *HSRP* meliputi: *Initial*, *Learn*, *Listen*, *Speak*, *Standby*, dan *Active*.

---

## 🌐 Praktik / Simulasi

- 🖥️ **Lab**: HSRP Configuration Guide  
- 🔧 **Tools**: *Packet Tracer*, *CLI*, *Utilitas Ping*  
- 🔄 **Hasil**: Berhasil melakukan konfigurasi dan mengaktifkan *HSRP* pada *redundant router*.  
- 📁 **File Lab**: [HSRP Configuration Guide PKA File](../labs/module-9/9.3.3-packet-tracer---hsrp-configuration-guide.pka) - ✅ 100% selesai

\---

- 🖥️ **Lab**: Data Center Exploration 
- 🔧 **Tools**: *Packet Tracer*, *CLI*, *Utilitas Ping*  
- 🔄 **Hasil**: Belum mampu diselesaikan karena praktikum berbasis *physical topology* ini membutuhkan kapasitas penyimpanan besar, sehingga perangkat mengalami gangguan saat proses pengerjaan.  
- 📁 **File Lab**: [Data Center Exploration PKA File](../labs/module-9/9.3.4-packet-tracer---data-center-exploration---physical-mode.pka) - ❌ 0% selesai

---

## 🧠 Catatan Pribadi

💬 Dalam jaringan dengan *topologi redundant*, keberadaan lebih dari satu *default gateway* dapat mencegah isolasi *host* ketika terjadi kegagalan pada salah satu *router*. Konsep inilah yang diimplementasikan oleh *First Hop Redundancy Protocols (FHRP)*. Selama praktik konfigurasi *HSRP*, saya memahami bagaimana dua *router* dapat saling berbagi peran sebagai *router aktif* dan *siaga* dengan menggunakan alamat virtual bersama. Mekanisme *preemption* juga sangat penting, karena memungkinkan *router* dengan prioritas lebih tinggi untuk secara otomatis mengambil kembali peran sebagai *router aktif* setelah kembali online. Pengalaman ini memperkuat pemahaman saya mengenai bagaimana jaringan tetap dapat beroperasi secara optimal meskipun terjadi gangguan pada salah satu perangkat inti.

---

## 📎 Referensi Modul

* [Cisco Networking Academy](https://www.netacad.com)

---

> Ditulis oleh: **Ulil Akbar** pada 2025-07-04.
