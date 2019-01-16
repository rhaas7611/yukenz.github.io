---
title: Cara Install OpenCL Driver di Linux Debian 8
tags: [Linux, Tutorial,CLI,Youtube,Tips and Trick]
thumbnail : https://upload.wikimedia.org/wikipedia/en/thumb/1/1c/OpenCL_Logo.svg/1200px-OpenCL_Logo.svg.png
---

Halo Teman-teman semuanya. Kali ini admin akan membuat Cara Install OpenCL Driver di Linux Debian 8.

![Cara Download Video di Youtube dengan CLI di Linux](https://upload.wikimedia.org/wikipedia/en/thumb/1/1c/OpenCL_Logo.svg/1200px-OpenCL_Logo.svg.png  "Cara Install OpenCL Driver di Linux Debian 8")

Banyak sekali orang yang membutuhkan fitur opencl ini. Salah satu kegunaannya adalah untuk membantu perenderan animasi pada software open source bernama blender.

OpenCL ini berfugsi untuk mengakselerasikan graphic video dan hardware untuk mempercepat kinerja suatu software.

Setiap GPU memiliki openCL Drivernya masing masing. Akan tetapi ada juga OpenCL Driver pihak ke tiga yang bisa digunakan untuk hardware yang berbeda.

Misalkan saja Nvidia pastinya akan membutuhkan driver nvidia-opencl-icd dan AMD akan membutuhkan driver amd-opencl-icd.

Misal saja jika Distro Linux kita hanya menyediakan paket driver OpenCL Untuk Nvidia sedangkan GPU kita adalah AMD. Tentu saja jika kita mengintall driver milik Nvidia untuk AMD maka driver tidak bisa berjalan.

Biasanya ini terjadi saat kita menggunakan distro lawas yang sudah EOL. Tapi untuk mengakali nya kita bisa menggunakan Driver OpenCL pihak ketiga. Yang tentunya OpenSource.

Disini beberapa driver yang admin ketahui adalah :
1. MESA
2. POCL
3. BEIGNET

Sesuai dengan judul admin memberikan perintah yang spesifik ke Debian 8. Berikut beberapa command untuk menginstall driver sesuai yang kalian butuhkan.

Harap diingat hanya 1 Drive yang boleh kalian install, Jika ingin ganti kalian harus menguninstallnya dahulu. Ada beberapa laporan di beberapa trit bahwa jika menginstall lebih dari 1 driver maka Xorg akan error dan tidak mau start. Alhasil kalian hanya stuck di mode CLI saja.

Khusus utuk debian 8 paket opencl-icd memiliki sub driver yang tidak bisa diinstal semuanya. Oleh karena itu saat kita mengetikan perintah dibawah ini:

{% highlight console %}
sudo apt-get install opencl-icd
{% endhighlight %}

Maka akan memunculkan Output :

{% highlight console %}
$ sudo apt-get install opencl-icd
[sudo] password for yuyun: 
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Package opencl-icd is a virtual package provided by:
  nvidia-legacy-340xx-opencl-icd 340.106-2~deb9u1~bpo8+1
  nvidia-legacy-304xx-opencl-icd 304.137-5~deb9u1~bpo8+1
  beignet-opencl-icd 1.3.0-3~bpo8+1
  nvidia-opencl-icd 340.106-1
  amd-opencl-icd 1:15.9-4~deb8u2
  pocl-opencl-icd 0.10-10
  mesa-opencl-icd 10.3.2-1+deb8u1
  beignet 0.9.3~really.0.8+dfsg-1
You should explicitly select one to install.

E: Package 'opencl-icd' has no installation candidate
{% endhighlight %}

Di situlah ada beberapa paket driver yang ada di repositori debian 8 yang bisa kita install. Karena gpu admin memakai AMD maka admin akan memilih menginstall amd-opencl-icd. Jika Nvidia pilih yang Nvidia. Install menggunakan perintah : 
{% highlight console %}
sudo apt-get install amd-opencl-icd
{% endhighlight %}

Jika kalian mengalami masalah error atau kalian lebih suka menggunakan driver pihak ketiga yang OpenSource kalian bisa menginstall pocl mesa atau beignet.

Oke sekian yang bisa admin sampaikan jika ada salah kata atau informasi admin mohon maaf. Jika mengalami kendala kalian bisa chat admin via WA ini nomor saya 085726074357. Sampai Jumpa di lain Post :D