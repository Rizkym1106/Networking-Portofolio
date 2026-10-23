# 🔐 Multi-Room Enterprise Network Infrastructure with VTP & Secure SSH Management

Lab ini berfokus pada efisiensi pengelolaan VLAN berskala besar menggunakan *VLAN Trunking Protocol* (VTP) serta penerapan protokol *Secure Shell* (SSH) untuk manajemen jarak jauh perangkat jaringan yang aman.

---

## 🎯 Fitur & Konfigurasi Utama

* **VLAN Trunking Protocol (VTP)**: Sinkronisasi database VLAN secara otomatis antar-switch (VTP Server & VTP Client).
* **Otentikasi Lokal**: Pembuatan akun pengguna lokal (*Local User Database*) dengan kredensial terenkripsi.
* **Remote SSH Management**: Menggantikan Telnet dengan enkripsi SSH pada baris VTY.
* **Centralized Sub-interfaces & DHCP**: Distribusi IP dinamis terintegrasi.

---

## 📸 Bukti Konfigurasi

### 1. Konfigurasi SSH pada Router
![Konfigurasi SSH](Configurasi%20SSH%20di%20router.png)

### 2. Membuat User Login Local
![User Login Local](Membuat%20user%20login%20local.png)

### 3. Konfigurasi Sub-Interface
![Sub Interface](Configuration%20sub%20inteface.png)

### 4. Konfigurasi DHCP Server
![DHCP Server](Configuration%20DHCP%20server.png)

---

## 🛠️ Komponen & File
* **File Simulasi**: `Multi-Room Enterprise Network Infrastructure with VTP & Secure SSH Management.pkt`
* **Dokumentasi Gambar**:
  * `Configurasi SSH di router.png`
  * `Membuat user login local.png`
  * `Configuration sub inteface.png`
  * `Configuration DHCP server.png`
