🧪 OrangeHRM Login Test Cases
Proyek ini berisi kumpulan test case (TC) untuk menguji fungsionalitas login pada sistem OrangeHRM. Pengujian dilakukan secara automation berdasarkan berbagai skenario valid dan invalid untuk memastikan sistem menangani input dengan benar.

📁 Struktur Berkas
OrangeHRM_Test Case.xlsx — Berkas utama yang berisi seluruh test case.

Folder /cypress/screenshots — Berisi screenshot hasil uji (pass/fail) untuk tiap test case, bernama sesuai ID test case (misalnya: TC.Log.001-SuccessfulLogin.png).

✅ Daftar Test Case
TC ID	Deskripsi Skenario	Status	Keterangan
TC.Log.001	Login dengan username dan password valid	Pass	User berhasil login
TC.Log.002	Login dengan username dan password tidak valid	Pass	Tampil pesan error
TC.Log.003	Login dengan username tidak valid	Pass	Tampil pesan error
TC.Log.004	Login dengan password tidak valid	Pass	Tampil pesan error
TC.Log.005	Login dengan username huruf kecil semua dan password valid
TC.Log.006	Login dengan password huruf kapital semua	Pass	Tampil pesan error
TC.Log.007	Login dengan kolom username dan password kosong	Pass	Tampil pesan error
TC.Log.008	Login dengan kolom username kosong	Pass	Tampil pesan error
TC.Log.009	Login dengan kolom password kosong	Pass	Tampil pesan error

❌ Fail pada TC.Log.005
Skenario: Pengguna mencoba login menggunakan username 'admin' (huruf kecil semua) dan password yang valid.

Ekspektasi: Login gagal karena sistem seharusnya membedakan huruf besar-kecil (case-sensitive).

Hasil aktual: Login berhasil, yang berarti sistem tidak membedakan huruf besar-kecil pada username, atau validasi username tidak ketat.

Kesimpulan: Ini merupakan bug potensial terkait keamanan dan validasi input. Sistem seharusnya membedakan 'Admin' dengan 'admin'.


📌 Catatan
Semua pengujian dilakukan secara automation menggunakan browser Chrome.

Screenshot disertakan untuk setiap test case sebagai dokumentasi hasil.
