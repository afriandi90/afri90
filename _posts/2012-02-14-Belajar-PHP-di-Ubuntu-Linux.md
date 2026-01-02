---           
layout: post
title: Belajar PHP di Ubuntu Linux
date: 2012-02-14 06:35:09 UTC
updated: 2012-02-14 06:35:09 UTC
comments: false
categories: linux
---
<h2>Pengenalan PHP</h2><br />
<strong>PHP</strong> merupakan singkatan rekursif (akronim berulang) dari <strong>PHP Hypertext Preprocessor</strong>. PHP merupakan sebuah bahasa pemrograman web yang bekerja di sisi server (<em>server side scripting</em>) yang dapat melakukan konektifitas pada database yang di mana hal itu tidak dapat dilakukan hanya dengan menggunakan sintaks-sintaks HTML biasa.<br />
<br />
Pada awalnya PHP merupakan kependekan dari Personal Home Page (Situs Personal). PHP pertama kali dibuat oleh <strong>Rasmus Lerdorf</strong> pada tahun 1995.<br />
<a name='more'></a><br />
<br />
<strong>Kelebihan PHP dari bahasa pemrograman lain :</strong><br />
<ol><li>Bahasa pemrograman PHP adalah sebuah bahasa script yang tidak melakukan sebuah kompilasi dalam penggunaanya.</li>
<li>Web Server yang mendukung PHP dapat ditemukan dimana - mana dari mulai apache, IIS, Lighttpd, nginx, hingga Xitami dengan konfigurasi yang relatif mudah.</li>
<li>Dalam sisi pengembangan lebih mudah, karena banyaknya milis - milis dan developer yang siap membantu dalam pengembangan.</li>
<li>Dalam sisi pemahamanan, PHP adalah bahasa scripting yang paling mudah karena memiliki referensi yang banyak.</li>
<li>PHP adalah bahasa open source yang dapat digunakan di berbagai mesin (Linux, Unix, Macintosh, Windows) dan dapat dijalankan secara runtime melalui console serta juga dapat menjalankan perintah-perintah system.</li>
<em>(wikipedia)</em></ol><br />
<strong>Cara kerja PHP :</strong><br />
<blockquote>Seperti yang telah disebutkan di atas bahwa PHP adalah aplikasi di sisi server atau dengan kata lain beban kerja ada di server bukan di client. Pada saat browser meminta dokumen PHP, web server langsung menggunakan modul PHP untuk mengolah dokumen tersebut. Jika pada dokumen terkandung fungsi yang mengakses database maka modul PHP menghubungi database server yang bersangkutan. Dokumen yang berformat PHP dikembalikan web server dalam format HTML, sehingga source code PHP tidak tampak di sisi browser.<br />
<em>(Modul Web Programming using PHP and MySQL [LePKom])</em></blockquote><br />
<h2>Menjalankan PHP di Ubuntu Linux</h2><br />
Sebelumnya kita membutuhkan program yang dibutuhkan untuk dapat menjalankan PHP di Linux yakni <strong>XAMPP</strong>. XAMPP meru­pakan sebuah pro­gram web server yang sudah san­gat lengkap karena dalam sekali install kita bisa men­da­p­atkan sebuah Apache Server, MySQL Data­base, dan tentu saja PHP. Download XAMPP <a href="http://www.apachefriends.org/en/xampp-linux.html" rel="nofollow">di sini</a>. Untuk instalasi XAMPP di Ubuntu&nbsp;ikuti langkah berikut :<br />
<ol><li>Mis­alkan Anda sim­pan file hasi download tadi di <em>Desk­top</em>, maka jalankan  per­in­tah berikut di ter­mi­nal :<br />
<span style="font-family: 'Courier New';">$ cd Desktop</span></li>
<li>Ekstrak <span class="caps">XAMPP</span> ke direk­tori /opt :<br />
<span style="font-family: 'Courier New';">$ sudo tar xvfz  xampp-linux-1.7.2.tar.gz –C&nbsp;/opt</span></li>
<li>Kemu­dian jalankan <span class="caps">XAMPP</span> den­gan per­in­tah berikut :<br />
<span style="font-family: 'Courier New';">$ sudo /opt/lampp/lampp start</span></li>
<li>Test apakah <span class="caps">XAMPP</span> sudah dapat bek­erja.<br />
Buka browser Mozilla Fire­fox Anda, dan ketikkan :<br />
<span style="font-family: 'Courier New';">http://localhost</span></li>
<li>Untuk menghen­tikan <span class="caps">XAMPP</span> gunakan per­in­tah berikut :<br />
<span style="font-family: 'Courier New';">$ sudo /opt/lampp/lampp stop</span></li>
</ol><br />
Untuk menulis koding PHP kita membutuhkan sebuah teks editor. Teks editor apa saja sebenarnya bisa dipakai. Namun saya merekomendasikan Anda untuk memakai <strong>Geany</strong>. Geany merupakan sebuah IDE yang ringan dan tidak boros memori.<br />
<br />
Untuk melakukan instalasi Geany di Ubuntu ketikkan perintah berikut di Terminal :<br />
<blockquote><span style="font-family: 'Courier New';">$ sudo apt-get install geany</span></blockquote><br />
Jika semua sudah siap, kita bisa memulai menulis program menggunakan PHP.<br />
<ul><li>Pertama buat sebuah folder di direktori <strong>/opt/lampp/htdocs/</strong> misal kita beri nama <strong>php</strong>:<br />
<span style="font-family: 'Courier New';">$ sudo mkdir /opt/lampp/htdocs/php</span></li>
<li>Buka Geany dalam mode super-user menggunakan perintah berikut :<br />
<span style="font-family: 'Courier New';">$ sudo geany</span></li>
<li>Pada Geany buka menu File &gt; New (with template) &gt; PHP source file. Tekan Ctrl + A, hapus semua kode, kemudian ketikkan kode sederhana seperti berikut :<br />
<blockquote>&lt;html&gt;<br />
&lt;head&gt;&lt;title&gt;Contoh program PHP&lt;/title&gt;&lt;/head&gt;<br />
&lt;body&gt;<br />
&lt;?php<br />
echo ("Ini adalah program PHP pertama saya.&lt;br/&gt;");<br />
echo ("Ternyata membuatnya mudah ya? ^_^.");<br />
?&gt;<br />
&lt;/body&gt;<br />
&lt;/html&gt;</blockquote><br />
</li>
<li>Keterangan :<br />
Kode di antara tag  <strong>&lt;?php</strong> dan <strong>?&gt;</strong> adalah kode PHP.<br />
Kode <strong>echo</strong> berarti perintah untuk mencetak kata yang berada di antara tanda petik.</li>
<li>Kemudian simpan file tersebut di direktori yang telah Anda buat sebelumnya, yakni di <strong>/opt/lampp/htdocs/php</strong>, misal dengan nama <strong>contoh.php</strong></li>
<li>Buka browser Mozilla Firefox dan jalankan program PHP tersebut dengan memasukkan URL berikut :<br />
<span style="font-family: 'Courier New';">http://localhost/php/contoh.php</span></li>
<li>Jika tulisan di antara tanda petik berhasil tercetak maka Anda sudah berhasil membuat sebuah program menggunakan PHP.</li>
</ul><br />
Website berbahasa Indonesia yang dapat Anda jadikan sebagai referensi untuk <strong>belajar PHP</strong>:<br />
<a href="http://www.klik-kanan.com/tutorial/php/index.shtml" rel="nofollow" target="_blank">Tutorial php untuk pemula / dasar-dasar php (dlm bahasa indonesia)</a><br />
<a href="http://phpug.or.id/category/tutorial/" rel="nofollow" target="_blank">PHP User Group Indonesia » Tutorial</a><br />
<a href="http://www.ilmuwebsite.com/belajar-php" rel="nofollow" target="_blank">Belajar PHP » IlmuWebsite</a><br />
<a href="http://ilmukomputer.org/category/pemrograman-php/" rel="nofollow" target="_blank">Pemrograman PHP : IlmuKomputer.com</a>
