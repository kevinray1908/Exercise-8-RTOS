# Exercise 8: Using Semaphores to Protect Critical Sections
## Tujuan
1. Menerapkan semaphore untuk melindungi akses ke bagian kritis dari kode.
2. Memastikan tugas multitasking dapat berjalan tanpa konflik saat mengakses sumber daya bersama.

## Peralatan
1. STM 32
2. STM32CubeIDE.
3. FreeRTOS library.
4. Langkah-langkah

## Langkah langkah
**Persiapan Proyek**
1. Tambahkan xSemaphoreHandle dalam proyek FreeRTOS.
2. Buat dua tugas (Task1 dan Task2) yang bersaing untuk mengakses sumber daya bersama.

**Implementasi Kode** 
1. Buat semaphore dengan fungsi xSemaphoreCreateBinary().
2. Gunakan xSemaphoreTake() sebelum tugas mengakses sumber daya, dan xSemaphoreGive() setelah selesai.

**Uji Program**
1. Flash kode ke STM32F4 Discovery Board.
2. Amati perubahan stabilitas sistem sebelum dan sesudah penggunaan semaphore.

## Hasil yang Diharapkan
1. Tanpa Semaphore: Konflik terjadi saat tugas mengakses sumber daya bersama.
2. Dengan Semaphore: Konflik dapat dihindari, karena hanya satu tugas yang dapat mengakses sumber daya dalam satu waktu.

## Hasil Percobaan
https://github.com/user-attachments/assets/473b745d-db70-4363-92bf-2f56dfd30bcf

