Berikut adalah langkah-langkah yang disusun secara lebih sederhana untuk menyiapkan dan menjalankan proyek evm-auto-transfer:

1. Persiapkan Prasyarat
Pastikan Anda sudah menginstal Node.js (versi 14 atau lebih tinggi) dan npm. Cek dengan perintah:

bash
Salin
Edit
node -v
npm -v
2. Clone Repository
Clone repositori proyek dan masuk ke dalam folder proyek:

bash
Salin
Edit
git clone https://github.com/dante4rt/evm-auto-transfer.git
cd evm-auto-transfer
3. Install Dependencies
Install semua dependensi yang dibutuhkan:

bash
Salin
Edit
npm install
4. Konfigurasi Jaringan
Buat folder /chains jika belum ada.
Buat dua file JSON: testnet.json dan mainnet.json.
Isi file testnet.json dengan konfigurasi jaringan testnet, misalnya:

json
Salin
Edit
[
    {
        "name": "Tea Assam Testnet",
        "rpcUrl": "https://assam-rpc.tea.xyz",
        "chainId": 93384,
        "symbol": "TEA",
        "explorer": "https://assam.tea.xyz"
    }
]
5. Konfigurasi Private Keys
Buat file privateKeys.json di direktori root dan masukkan private key Anda:
json
Salin
Edit
[
    "0xYOUR_PRIVATE_KEY_1",
    "0xYOUR_PRIVATE_KEY_2"
]
Penting: Jangan sampai private key Anda terekspos.

6. Konfigurasi Alamat Target
Buat file addresses.json di direktori root dan masukkan alamat tujuan transfer dana:
json
Salin
Edit
[
    "0xTARGET_ADDRESS_1",
    "0xTARGET_ADDRESS_2"
]
7. Jalankan Skrip
Untuk menjalankan skrip transaksi acak:

bash
Salin
Edit
npm start
Untuk menjalankan dengan alamat target:

bash
Salin
Edit
npm run target
Ikuti instruksi untuk memilih jaringan dan mengonfigurasi transaksi.
