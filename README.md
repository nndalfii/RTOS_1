# RTOS_1
## Deskripsi
Proyek ini menggunakan mikrokontroler STM32 yang mengimplementasikan pembacaan nilai ADC secara periodik, menampilkan data di OLED display, dan berinteraksi melalui UART. Proyek ini juga menggunakan tombol fisik untuk mengontrol LED, dengan multitasking yang dikelola oleh FreeRTOS.

## Fitur Utama
1. **Pembacaan ADC**: Pembacaan nilai ADC dilakukan secara periodik menggunakan task FreeRTOS.
2. **Tampilan OLED**: Nilai hasil pembacaan ADC ditampilkan secara real-time pada layar OLED.
3. **Interaksi UART**: Komunikasi antara STM32 dan komputer dilakukan melalui UART. STM32 mengirimkan pesan status tombol melalui UART.
4. **Kontrol LED**: LED akan menyala ketika tombol fisik ditekan. Status penekanan tombol juga dikirim melalui UART.

## Cara Kerja
- Nilai ADC dibaca setiap periode tertentu dan ditampilkan di layar OLED.
- Ketika tombol fisik ditekan, STM32 akan mengirimkan pesan melalui UART, misalnya `Button1 pressed`, dan LED akan menyala sebagai indikasi.

## Dokumentasi

https://github.com/user-attachments/assets/2c0f89cb-707d-487e-9373-0a7e4081494d


  
## Instalasi

Langkah-langkah untuk menginstal proyek di lingkungan lokal:

1. Clone repositori ini:
   ```bash
   git clone https://github.com/nndalfii/RTOS_1.git


## Prasyarat
Sebelum memulai instalasi, pastikan bahwa Anda memiliki:
- STM32CubeIDE versi 1.16.0
- Board STM32 STM32F407VGT6
- Mini Debugger ST-Link
- Layar OLED 0.96 I2C
- Kabel USB untuk koneksi ke board STM32

## Dependensi
Proyek ini membutuhkan beberapa library berikut:
- STM32Cube HAL Library
- FreeRTOS
- SSD1306 OLED Display Library

## Struktur Proyek (Optional)
Berikut adalah struktur direktori utama dari proyek ini:
```bash
RTOS_1/
│
├── Core/                 # Kode sumber utama (src)
├── Drivers/              # Driver STM32 dan OLED
├── Middlewares/          # FreeRTOS
└── README.md             # File README ini

