---
title: Berkenalan dengan ESP32 Microcontroller
date: 21-02-2026
description: Minggu 2
---

# Mengenal ESP32 – Untuk prototyping IoT  
**EL5183 – Sistem dan Aplikasi IoT**

Pada sesi praktik kali ini, kami mulai berkenalan dengan perangkat utama yang akan digunakan sepanjang perkuliahan, yaitu **ESP32 Development Board**. Perangkat ini menjadi fondasi utama dalam membangun sistem Internet of Things (IoT) yang akan dikembangkan ke arah Smart City.

Pertemuan ini terasa penting karena menjadi jembatan dari konsep IoT yang sebelumnya dibahas secara teoritis menuju implementasi nyata menggunakan perangkat keras.

---

## 🔎 Apa Itu ESP32?

ESP32 adalah mikrokontroler yang dikembangkan oleh Espressif Systems dan dirancang khusus untuk aplikasi IoT. Keunggulan utamanya adalah sudah memiliki **WiFi dan Bluetooth terintegrasi**, sehingga tidak perlu modul tambahan untuk konektivitas jaringan.

Beberapa fitur utama ESP32:
- Dual-core processor
- WiFi & Bluetooth built-in
- Banyak pin GPIO
- Mendukung ADC, PWM, I2C, SPI, UART
- Cocok untuk prototyping sistem IoT

Dengan fitur tersebut, ESP32 sangat fleksibel untuk berbagai aplikasi monitoring dan kontrol berbasis jaringan.

---

## 🧠 Peran ESP32 dalam Sistem IoT

Dalam arsitektur IoT, ESP32 berfungsi sebagai **IoT device** atau perangkat edge. Tugasnya adalah:

1. Membaca data dari sensor  
2. Memproses data awal  
3. Mengirim data melalui WiFi  
4. Mengontrol aktuator jika diperlukan  

Secara sederhana, alurnya seperti ini:


ESP32 menjadi penghubung antara dunia fisik (sensor) dan dunia digital (aplikasi).

---

## ⚙️ Setup Awal ESP32

Pada sesi ini juga dilakukan instalasi dan konfigurasi awal:

1. Install Arduino IDE  
2. Menambahkan board ESP32 melalui Board Manager  
3. Memilih tipe board “ESP32 Dev Module”  
4. Menghubungkan board ke laptop via USB  

Setelah konfigurasi selesai, dilakukan pengujian menggunakan program sederhana.

---

## 💡 Uji Coba Pertama – LED Blink

Sebagai validasi awal, dijalankan program LED Blink untuk memastikan board dapat diprogram dengan benar.

```cpp
#define LED 2

void setup() {
  pinMode(LED, OUTPUT);
}

void loop() {
  digitalWrite(LED, HIGH);
  delay(1000);
  digitalWrite(LED, LOW);
  delay(1000);
}

LED pada board berhasil berkedip setiap satu detik, yang menandakan proses upload dan komunikasi berjalan dengan baik.

Meskipun sederhana, percobaan ini penting sebagai langkah awal sebelum masuk ke integrasi sensor dan komunikasi jaringan.

## 🌐 Potensi Pengembangan

Setelah memahami dasar penggunaan ESP32, banyak kemungkinan pengembangan yang dapat dilakukan, seperti:

- Monitoring suhu dan kelembapan ruangan
- Sistem smart parking
- Monitoring level sampah
- Web server lokal
- MQTT client untuk komunikasi cloud

ESP32 memberikan gambaran nyata bagaimana konsep IoT dapat diimplementasikan dalam skala kecil namun tetap relevan dengan sistem Smart City.
