
Untuk mengikuti langkah-langkah dalam instruksi tersebut, berikut adalah petunjuk yang lebih terperinci untuk mengonfigurasi dan menjalankan proyek evm-auto-transfer:

1. Install Prasyarat:
Pastikan Anda telah menginstal versi Node.js (v14 atau lebih tinggi) dan npm (Node Package Manager). Jika belum, Anda bisa menginstalnya terlebih dahulu:

Install Node.js: Kunjungi Node.js download dan pilih versi yang sesuai.
Install npm: npm biasanya sudah terinstal bersama Node.js.
Verifikasi instalasi dengan perintah berikut:



node -v
npm -v
2. Clone Repository:
Clone proyek ke server atau mesin lokal Anda dengan menggunakan git:



git clone https://github.com/dante4rt/evm-auto-transfer.git
cd evm-auto-transfer
3. Install Dependencies:
Setelah masuk ke dalam direktori proyek, jalankan perintah berikut untuk menginstal semua dependensi yang diperlukan:



npm install
4. Konfigurasi Jaringan (Chains):
Buat file JSON untuk testnet dan mainnet di dalam direktori /chains:

testnet.json
mainnet.json
Contoh konfigurasi untuk testnet.json:


[
    {
        "name": "Plume Testnet",
        "rpcUrl": "https://plume-testnet-rpc.example.com",
        "chainId": 8888,
        "symbol": "PLUME",
        "explorer": "https://plume-testnet-explorer.example.com"
    }
]
Pastikan Anda menyesuaikan dengan detail jaringan yang Anda pilih (misalnya Tea Assam Testnet).

5. Menentukan Private Keys:
Buat file privateKeys.json di direktori root proyek dan masukkan private key Anda di dalam array:


[
    "0xYOUR_PRIVATE_KEY_1",
    "0xYOUR_PRIVATE_KEY_2"
]
Penting: Jaga agar file ini tetap aman dan jangan membagikan private key Anda!

6. Menentukan Target Address:
Buat file addresses.json di direktori root proyek dan masukkan alamat target yang akan Anda transfer dana:

[
    "0xTARGET_ADDRESS_1",
    "0xTARGET_ADDRESS_2"
]
7. Menjalankan Skrip:
Untuk menjalankan skrip secara acak (misalnya untuk menghasilkan alamat acak dan melakukan transaksi), gunakan perintah:


npm start
Untuk menggunakan fitur alamat target, jalankan perintah:


npm run target
Ketika menjalankan perintah tersebut, Anda akan diminta untuk memilih jaringan (Testnet/Mainnet) dan memilih chain yang telah Anda tentukan sebelumnya.

8. Konfigurasi dan Penggunaan Selesai:
Sekarang, Anda telah mengonfigurasi semua yang dibutuhkan untuk melakukan transaksi menggunakan evm-auto-transfer. Anda bisa melanjutkan dengan proses transaksi sesuai petunjuk yang diberikan di dalam dokumentasi proyek ini.

Jika ada kesalahan atau Anda mengalami masalah selama proses konfigurasi atau eksekusi, pastikan file JSON Anda valid dan semua dependensi sudah terinstal dengan benar.
