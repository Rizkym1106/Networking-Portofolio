# 🛡️ Multi-VLAN Enterprise Network with Telnet-Based In-Band Management

Dokumentasi lab ini membahas simulasi dan analisis implementasi *In-Band Management* berbasis protokol Telnet pada jaringan enterprise multi-VLAN, serta evaluasi risiko keamanan dan rekomendasi penguatannya (*security hardening*).

---

## 📌 Deskripsi Proyek

Pada proyek ini, jaringan enterprise dikonfigurasi dengan beberapa VLAN untuk pemisahan departemen. Pengelolaan jarak jauh (*remote management*) pada perangkat jaringan (Switch & Router) dilakukan menggunakan antarmuka Telnet melalui *Switch Virtual Interface* (SVI). Proyek ini difokuskan untuk mendemonstrasikan cara kerja Telnet sekaligus menganalisis kelemahan utamanya dari sudut pandang keamanan jaringan.

---

## 🎯 Tujuan Lab

1. **Implementasi In-Band Management**: Mengkonfigurasi IP Address pada SVI (VLAN Management) agar perangkat switch dan router dapat diakses secara *remote*.
2. **Pengujian Akses Telnet**: Melakukan konfigurasi jalur VTY (`line vty 0 4`) dan otentikasi kata sandi untuk akses Telnet.
3. **Analisis Keamanan Jaringan**: Menganalisis risiko keamanan protokol Telnet yang mengirimkan kredensial (*username/password*) dan perintah CLI dalam bentuk teks biasa (*plain-text*).
4. **Rekomendasi Hardening**: Memahami langkah-langkah mitigasi seperti migrasi ke SSHv2 dan pembatasan akses VTY menggunakan *Access Control List* (ACL).

---

## 🛠️ Perangkat & Teknologi

* **Simulator**: Cisco Packet Tracer (v8.0+)
* **Perangkat Jaringan**: Cisco Router & Cisco Catalyst Switch
* **Protokol**: IEEE 802.1Q (VLAN & Trunking), Telnet (TCP Port 23), SVI (Switch Virtual Interface)

---

## 📸 Dokumentasi Konfigurasi

### 1. Konfigurasi Telnet pada Perangkat
Berikut adalah dokumentasi langkah konfigurasi Telnet pada perangkat jaringan:

![Cara Konfigurasi Telnet](Cara%20konfigurasi%20telnet.png)

---

## 🔒 Analisis Keamanan (Telnet vs. SSH)

| Fitur / Parameter | Telnet | SSH (Secure Shell) |
| :--- | :--- | :--- |
| **Enkripsi Data** | Tidak Ada (*Plain-text*) | Terenkripsi (*Symmetric/Asymmetric*) |
| **Port Default** | TCP 23 | TCP 22 |
| **Risiko Keamanan** | *Packet Sniffing*, *Eavesdropping*, *Man-in-the-Middle* (MitM) | Sangat Aman terhadap *Sniffing* |
| **Rekomendasi** | Hanya untuk Lab / Pengujian | Standar Industri (*Production Environment*) |

---

## 📂 Struktur Berkas Lab

```text
05-telnet-security-analysi/
├── Multi-VLAN Enterprise Network with Telnet-Based In-Band Management.pkt
├── Cara konfigurasi telnet.png
└── README.md
