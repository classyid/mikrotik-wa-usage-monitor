# README.md
# MikroTik WhatsApp Usage Monitor 📊

Monitor penggunaan data pelanggan MikroTik dengan notifikasi WhatsApp otomatis. Sistem ini memungkinkan ISP atau administrator jaringan untuk mengirimkan laporan penggunaan bandwidth kepada pelanggan secara berkala melalui WhatsApp.

## 🌟 Fitur Utama
- Monitoring penggunaan data (Upload/Download)
- Notifikasi WhatsApp otomatis
- Status penggunaan yang informatif
- Pemantauan kondisi sistem
- Pesan yang mudah dipahami
- Dukungan multiple pelanggan
- Delay sistem untuk pengiriman optimal

## 📋 Prasyarat
- RouterOS v6.x atau lebih tinggi
- API WhatsApp (kirimwa.id)
- Scheduler untuk penggunaan data
- Akses ke router MikroTik

## ⚙️ Konfigurasi
1. Siapkan API WhatsApp
```routeros
:local apikey "YOUR_API_KEY"
:local sender "YOUR_SENDER_NUMBER"
```

2. Atur Daftar Pelanggan
```routeros
:local pelangganList "User1,User2,User3"
:local nohpList "08123456789,08123456790,08123456791"
:local dataUsagePrefixList "USER1,USER2,USER3"
```

3. Pasang Script
- Copy seluruh script ke terminal Mikrotik
- Atau simpan sebagai scheduler untuk eksekusi berkala

## 📊 Format Pesan
Pesan yang dikirim akan berisi:
- Detail pelanggan
- Informasi penggunaan data
- Status penggunaan
- Kondisi sistem
- Waktu dan lokasi

## 🔧 Kustomisasi
Anda dapat menyesuaikan:
- Batas penggunaan data untuk status
- Format pesan
- Interval pengiriman
- Informasi yang ditampilkan

## 📝 Contoh Penggunaan
```routeros
# Jalankan script secara manual
/system script run wa-usage-monitor

# Atau jadwalkan melalui scheduler
/system scheduler add name=wa-monitor interval=1d \
    on-event="/system script run wa-usage-monitor"
```

## 🤝 Kontribusi
Kontribusi sangat diterima! Silakan buat pull request atau laporkan masalah melalui issues.

## 📜 Lisensi
MIT License - Silakan gunakan dan modifikasi sesuai kebutuhan Anda.

## 📫 Kontak
Jika Anda memiliki pertanyaan atau saran, silakan buat issue atau hubungi kami.

---
