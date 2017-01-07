

Latar Belakang Masalah
 
1.      Apa itu Snort?
2.      Bagaimana cara instalasi snort pada centOS?
 
Pembahasan
 
Snort adalah sebuah sistem open source untuk pencegahan penyusupan jaringan yang mampu melakukan analisis lalu lintas jaringan secara real-time dan packet logger pada jaringan IP. Snort dapat melakukan analisis protocol, konten pencarian atau pencocokan dan dapat digunakan untuk mendeteksi berbagai serangan.
 
CARA INSTALASI SNORT PADA CENTOS:
 
Sebelum menginstall snort, install dulu beberapa paket yang dibutuhkan snort untuk berjalan.
 
Masukkan script dibawah ini:
 
# yum install libdnet libdnet-devel pcre pcre-devel gcc make flex byacc bison kernel-devel libxml2-devel wget -y
 
Selanjutnya membuat direktori atau folder untuk digunakan sebagai tempat instalasi.
 
Masukkan script dibawah ini:
 
# mkdir /usr/local/src/snort
 
# cd /usr/local/src/snort
 
Instalasi Libpcap.
 
Masukkan script dibawah ini:
 
# wget http://www.tcpdump.org/release/libpcap-1.3.0.tar.gz -O libpcap.tar.gz
 
# tar zxvf libpcap.tar.gz
 
# cd libpcap-*
 
# ./configure && make && make install
 
# echo “/usr/local/lib” >> /etc/ld.so.conf
 
# ldconfig -v
 
Instalasi DAQ.
 
Masukkan script dibawah ini:
 
# wget https://www.snort.org/downloads/snort/daq-2.0.6.tar.gz -O daq.tar.gz
 
# tar zxvf daq.tar.gz
 
# cd daq-*
 
# ./configure && make && make install
 
# ldconfig -v
 
Buat user dan group untuk snort.
 
Masukkan script dibawah ini:
 
# groupadd snort
 
# useradd -g snort snort
 
Masuk ke folder snort dan instalasi snort.
 
Masukkan script dibawah ini:
 
# cd /usr/local/src/snort
 
# wget https://www.snort.org/downloads/snort/snort-2.9.9.0.tar.gz -O snort.tar.gz
 
# tar zxvf snort.tar.gz
 
# cd snort-2*
 
# ./configure –prefix /usr/local/snort –enable-sourcefire && make && make install
 
PENUTUPAN
 
Kesimpulan
 
Dari penjelasan-penjelasan diatas dapat disimpulkan bahwa Snort adalah sebuah sistem open source untuk pencegahan penyusupan jaringan yang mampu melakukan analisis lalu lintas jaringan secara real-time dan packet logger pada jaringan IP. Snort juga dapat melakukan analisis protocol, konten pencarian atau pencocokan dan dapat digunakan untuk mendeteksi berbagai serangan.
 
Saran
Sebaiknya kita harus lebih memahami dan mempelajari materi mengenai snort ini dengan lebih dalam lagi agar dapat berguna untuk bekal kedepannya.

Link Github : 
Nama : Muh Akbar Tamrin
Npm : 1144012
Kelas : D4 TI 3C
Matakuliah : Sistem Keamanan Jaringan
Link Mata Kuliah : Keamanan Jaringan

Referensi :

https://hdr03086.wordpress.com/2012/10/30/snort-deskripsi-fitur-dan-penggunaan-deskripsi-snort/

Scan Plagiarisme :


