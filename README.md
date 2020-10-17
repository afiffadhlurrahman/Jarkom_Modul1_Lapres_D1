# Jarkom_Modul1_Lapres_D1

Affan Ahsanul Habib 5111740000091  
Muhammad Afif Fadhlurrahman 5111840000093

## Display Filter

1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!

	**Jawab**

	Webserver pada "testing.mekanis.me" dapat dilihat dengan langkah-langkah berikut ini  
	1. **Display Filter** seperti berikut, kemudian pilih baris paling atas > klik kanan > pilih **Follow** > **TCP Stream**  
		`http.host == "testing.mekanis.me"`  
	2. Maka akan terbuka seperti ini, kemudian find server, dan hasilnya : `Server: nginx/1.14.0 (Ubuntu)`

2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

	**Jawab**

	1. Klik **File** > **Export Objects** > **HTTP**  
	2. Akan muncul seperti dibawah  
	3. Cari “Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg” di **Text Filter**, kemudian **Save** pada directory yang diinginkan  
	4. Gambar sudah disimpan

3. Cari username dan password ketika login di "ppid.dpr.go.id"!

	**Jawab**

	Pada **Display Filter** melakukan filter `http.host == "ppid.dpr.go.id" && http.request.method == "POST"`

4. Temukan paket dari web-web yang menggunakan basic authentication method!
	
	**Jawab**
	
	Untuk menemukan web-web yang menggunakan basic authentication method, kita bisa menggunakan filter `http.authbasic`
	![GitHub Logo](/img/4a.png)
	
5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
	
	**Jawab**
	
	1. Masukkan display filter `http.host == "aku.pengen.pw"`, kemudian akan terbuka seperti ini
	![GitHub Logo](/img/5a.png)
	2. Kemudian pilih baris Hypertext Transfer Protocol > Authorization,  maka di bagian credential akan terdapat user dan password untuk akses web "aku.pengen.pw"<br>
	![GitHub Logo](/img/5b.png)
	3. Isi jawaban yang ada di web tersebut, lalu screenshot
	![GitHub Logo](/img/5c.png)
	
6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).
	
	**Jawab**
	
	1. Masukan filter `ftp-data.command ~ "zipkey.txt"`
	![GitHub Logo](/img/6a.png)
	2. Kemudian pilih baris paling atas > klik kanan > pilih **Follow** > **TCP Stream**
	![GitHub Logo](/img/6b.png)
	3. Setelah itu, masukan filter `ftp-data.command ~ "Answer.zip"`, pilih baris paling atas > klik kanan > pilih **Follow** > **TCP Stream**
	![GitHub Logo](/img/6c.png)
	4. Show and save data as RAW, lalu buka file zip > pilih file **Open This.pdf** > masukkan password
	![GitHub Logo](/img/6d.png)
	![GitHub Logo](/img/6e.png)
	5. Setelah itu file pdf akan seperti ini
	![GitHub Logo](/img/6d.png)

7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"
	
	**Jawab**
	
	1. Masukan filter `ftp-data contains "Yes.pdf"`
	2. Kemudian pilih baris paling atas > klik kanan > pilih **Follow** > **TCP Stream**
	3. Kemudian **Save** pada directory yang diinginkan
	4. Setelah itu file pdf akan seperti ini
	
8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!

	**Jawab**
	
	1. Pertama, mencari IP dari Microsoft FTP Service. Dengan cara filter `ftp contains "Microsoft"`. Ditemukan IP-nya `198.246.117.106`  
	2. Selanjutnya menggunakan filter `ftp.request.command == RETR` untuk melihat objek yang diunduh. Untuk mengetahui hasil unduhan dari Microsoft FTP Service, filter tersebut digabungkan dengan filter yang mencari IP dari Microsoft. Hasilnya `ftp.request.command == "RETR" && ip.addr == 198.246.117.106`

9. Cari username dan password ketika login FTP pada localhost!
	
	**Jawab**
	
	Masukan filter `ftp.request.command == "USER" || ftp.request.command == "PASS"`
	
10. Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46"

	**Jawab**

	1. Cari dengan **Find a packet**, seperti pada gambar. Atau dengan *Shortcut* **CTRL**+**F**  
	2. Ganti menjadi **Hex Velue**. Lalu masukkan clue tadi. Klik **Find**  
	3. Maka akan ada paket yang diblok hitam, seperti pada gambar  
	4. Klik kanan pada paket tersebut. Pilih **Follow** kemudian **TCP Stream**. Hasilnya  
	5. Ganti “Show and save data as” menjadi **RAW**, seperti pada gambar.  
	6. Kemudian Save As, beri nama dengan format “.pdf”. Hasilnya  

## Capture Filter
11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
