---
title: Cara Download Video di Youtube dengan CLI di Linux
tags: [Linux, Tutorial,CLI,Youtube,Tips and Trick]
thumbnail : https://image.freepik.com/free-icon/youtube-logo_318-33597.jpg
---

Halo Teman-teman semuanya. Kali ini admin akan membuat tutorial Cara Download Video di Youtube dengan CLI di Linux.

![Cara Download Video di Youtube dengan CLI di Linux](https://image.freepik.com/free-icon/youtube-logo_318-33597.jpg  "Cara Download Video di Youtube dengan CLI di Linux")

Buat kalian yang pake leptop kentang kan kalo buka youtube pastinya lemot ya kaya leptop admin hehehe.

Jadi kalian bisa download videonya terus disimpen di hardisk. Tapi admin ada salah satu trik dan kalian bisa mempraktekannya jika kalian pengguna linux dan CLIers sejati.

Disininanti kita aka menggunakan aplikasi CLI yang bernama youtube-dl. Dengan youtube-dl ini kita bisa mendownload video di youtube hanya dengan menggunkan terminal linux dan tentunya koneksi internet.

Untuk bahannya sangat simple. Yaitu binari yotube-dl dan Python2.7. Biasanya disetiap distro(bukan mini) python 2.7 sudah otomatis terinstall.

Untuk meninstall binari youtube-dl di linux kalian bisa menggunakan perintah dibawah ini

{% highlight console %}
sudo wget https://yt-dl.org/downloads/latest/youtube-dl -O /usr/local/bin/youtube-dl
{% endhighlight %}

{% highlight console %}
sudo chmod a+x /usr/local/bin/youtube-dl
{% endhighlight %}

Setelah itu kalian coba test menggunakan perintah youtube-dl dan nanti akan keluar informasi binari dan lainnya.

Untuk mendownload video dari youtube kalian hanya perlu menyediakan link nya saja. Link bisa didapatkan di URL bar saat kalian mem play sebuah video di youtube.

Setelah mendapatkan linknya gunakan perintah

{% highlight console %}
youtube-dl -F URL
{% endhighlight %}

maka nanti akan keluar beberapa output nomor di baris paling depan. Pilhlah yang berstatus best.

Setelah itu ketikan

{% highlight console %}
youtube-dl -f CODE URL
{% endhighlight %}

Tunggu beberapa saat, tergantung bandwith kalian. Kemudian nanti file nya akan tersimpan di direktori dimana kalian mengetikan itu di terminal. Jika tidak yakin ketikan pwd di terminal

Jika kalian ingin mendownload mp3 nya saja. Maka ketikan perintah dibawah ini

{% highlight console %}
youtube-dl -x --audio-format mp3 URL
{% endhighlight %}

Oke semoga tutorial Cara Download Video di Youtube dengan CLI di Linux diatas bermanfaat. Keep calm and CrootZ :D
