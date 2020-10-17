# Jarkom_Modul1_Lapres_D1

Affan Ahsanul Habib 5111740000091  
Muhammad Afif Fadhlurrahman 5111840000093

## Display Filter

1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!

	**Jawab**

	Webserver pada "testing.mekanis.me" dapat dilihat dengan langkah-langkah berikut ini  
	1. **Display Filter** seperti berikut, kemudian pilih baris paling atas > klik kanan > pilih **Follow** > **TCP Stream**  
		`http.host == "testing.mekanis.me"`  
	![No 1](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/1a.png)
	2. Maka akan terbuka seperti ini, kemudian find server, dan hasilnya : `Server: nginx/1.14.0 (Ubuntu)`  
	![No 1](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/1b.png)

2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

	**Jawab**

	1. Klik **File** > **Export Objects** > **HTTP**  
	![No 2](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/2a.png)
	2. Akan muncul seperti dibawah  
	![No 2](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/2b.png)
	3. Cari “Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg” di **Text Filter**, kemudian **Save** pada directory yang diinginkan  
	![No 2](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/2c.png)
	4. Gambar sudah disimpan  
	![No 2](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/2d.png)

3. Cari username dan password ketika login di "ppid.dpr.go.id"!

	**Jawab**

	Pada **Display Filter** melakukan filter `http.host == "ppid.dpr.go.id" && http.request.method == "POST"`  
	![No 3](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/3b.png)
	![No 3](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/3b.png)

4. Temukan paket dari web-web yang menggunakan basic authentication method!
	
	**Jawab**
	
	Untuk menemukan web-web yang menggunakan basic authentication method, kita bisa menggunakan filter `http.authbasic` <br>
	![No 4](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/4a.png)
	
5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
	
	**Jawab**
	
	1. Masukkan display filter `http.host == "aku.pengen.pw"`, kemudian akan terbuka seperti ini <br>
	![No 5](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/5a.png)
	2. Kemudian pilih baris Hypertext Transfer Protocol > Authorization,  maka di bagian credential akan terdapat user dan password untuk akses web "aku.pengen.pw"<br>
	![No 5](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/5b.png)
	3. Isi jawaban yang ada di web tersebut, lalu screenshot <br>
	![No 5](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/5c.png)
	
6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).
	
	**Jawab**
	
	1. Masukan filter `ftp-data.command ~ "zipkey.txt"` <br>
	![No 6](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/6a.png)
	2. Kemudian pilih baris paling atas > klik kanan > pilih **Follow** > **TCP Stream** <br>
	![No 6](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/6b.png)
	3. Setelah itu, masukan filter `ftp-data.command ~ "Answer.zip"`, pilih baris paling atas > klik kanan > pilih **Follow** > **TCP Stream** <br>
	![No 6](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/6c.png)
	4. Show and save data as RAW, lalu buka file zip > pilih file **Open This.pdf** > masukkan password <br>
	![No 6](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/6d.png)
	![No 6](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/6e.png)
	5. Setelah itu file pdf akan seperti ini <br>
	![No 6](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/6f.png)

7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"
	
	**Jawab**
	
	1. Masukan filter `ftp-data contains "Yes.pdf"` <br>
	2. Kemudian pilih baris paling atas > klik kanan > pilih **Follow** > **TCP Stream** <br>
	![No 7](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/7a.png)
	3. Kemudian **Save** pada directory yang diinginkan <br>
	![No 7](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/7b.png)
	4. Setelah itu file pdf akan seperti ini <br>
	![No 7](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/7c.png)

8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!

	**Jawab**
	
	1. Pertama, mencari IP dari Microsoft FTP Service. Dengan cara filter `ftp contains "Microsoft"`. Ditemukan IP-nya `198.246.117.106`  
	![No 8](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/8a.png)
	2. Selanjutnya menggunakan filter `ftp.request.command == RETR` untuk melihat objek yang diunduh. Untuk mengetahui hasil unduhan dari Microsoft FTP Service, filter tersebut digabungkan dengan filter yang mencari IP dari Microsoft. Hasilnya `ftp.request.command == "RETR" && ip.addr == 198.246.117.106`  
	![No 8](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/8b.png)

9. Cari username dan password ketika login FTP pada localhost!
	
	**Jawab**
	
	Masukan filter `ftp.request.command == "USER" || ftp.request.command == "PASS"` <br>
	![No 9](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/9a.png)
	
10. Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46"

	**Jawab**

	1. Cari dengan **Find a packet**, seperti pada gambar. Atau dengan *Shortcut* **CTRL**+**F**  
	![No 10](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/10a.png)
	2. Ganti menjadi **Hex Velue**. Lalu masukkan clue tadi. Klik **Find**  
	![No 10](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/10b.png)
	3. Maka akan ada paket yang diblok hitam, seperti pada gambar  
	![No 10](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/10c.png)
	4. Klik kanan pada paket tersebut. Pilih **Follow** kemudian **TCP Stream**. Hasilnya  
	![No 10](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/10d.png)
	5. Ganti “Show and save data as” menjadi **RAW**, seperti pada gambar.  
	![No 10](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/10e.png)
	6. Kemudian Save As, beri nama dengan format “.pdf”. Hasilnya  
	![No 10](https://github.com/afiffadhlurrahman/Jarkom_Modul1_Lapres_D1/blob/main/img/10f.png)

## Capture Filter
11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
