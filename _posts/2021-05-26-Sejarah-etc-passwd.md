---
layout: post
title: Sejarah File /etc/passwd pada linux
tags: pengetahuan, linux
category: Pengetahuan, Informasi, Linux
description: Banyak hal menarik dibalik sejarah file /etc/passwd
comments: true
fullview: false
---
<!-- excerpt-start -->Dulu, 26 tahun yang lalu, sistem UNIX menyimpan password pengguna dalam teks biasa, di file <b>/etc/passwd</b><!-- experpt-end --> (karena itulah namanya.) Ini untuk alasan yang sangat jelas, karena sangat tidak aman. Tetapi tidak ada solusi sederhana untuk ini karena setiap perubahan pada sistem password terenskripsi akan merusak kompatibilitas pada file /etc/passwd itu sendiri dan pada semua sistem yang bergantung pada file ini. Solusinya adalah membuat file baru, file /etc/shadow! Sesuai namanya "shadow" yang artinya "bayangan", file ini akan "membayangi" file /etc/passwd dan menyediakan tempat untuk sandi terenkripsi baru bersama dengan beberapa kontrol sandi tambahan. Jadi, meskipun memiliki file terpisah agak aneh saat ini, ia memiliki konteks historis yang membuatnya masuk akal. Tidak ada fungsionalitas yang hilang dan kerumitan tambahan bersifat nominal. (Linux dan sebagian besar UNIX menggunakan file ini. BSD, sebaliknya, menggunakan /etc/master.passwd.)

<u><i><q>Pelajaran Sejarah UNIX: Sistem password shadow pertama kali diperkenalkan pada pertengahan 1980-an oleh sistem SunOS UNIX Sun dan pada tahun 1990 disalin secara luas dan pada dasarnya ada di mana-mana dalam sistem UNIX. Jadi konsep bayangan telah menjadi bagian dari Linux sejak awal.<br><br>
Tidak seperti file /etc/passwd dan /etc/group, /etc/shadow dilindungi dan pengguna biasa tidak dapat melihat isinya. Ini memberikan tingkat keamanan tambahan untuk itu. Pengguna tidak perlu melihat isi /etc/shadow, tetapi file lain berguna untuk melihat akun apa yang tersedia, grup yang ada, dan siapa yang menjadi anggotanya.
</i></u></q><br><br>
Contoh urutan pada file /etc/passwd:

