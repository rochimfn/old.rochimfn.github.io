---
layout: post
title:  "Memasang Openjdk 11 di Ubuntu 18.04"
date:   2019-07-24 06:06:38 +0700
categories: [java,ubuntu]
---

Openjdk merupakan set tools dasar untuk pengembangan aplikasi berbasis java. Untuk memasangnya di OS Ubuntu caranya sangat mudah karena Openjdk 11 sudah tersedia di repository utama Ubuntu 18.04.

Pertama lakukan `apt update` untuk memastikan Ubuntu telah memiliki daftar paket terbaru dari repository

{% highlight shell %}
sudo apt update
{% endhighlight %}

Gunakan perintah berikut untuk mengetahui openjdk versi berapa saja yang tersedia di repository Ubuntu Bionic

{% highlight shell %}
apt-cache search openjdk
{% endhighlight %}
[![SS Openjdk 1](../../assets/openjdk-1.png)](../../assets/openjdk-1.png)

Untuk memasang Openjdk versi 11 gunakan perintah

{% highlight shell %}
sudo apt install openjdk-11-jdk
{% endhighlight %}

Terakhir pastikan `java` dan `javac` memiliki angka versi yang sama

{% highlight shell %}
javac --version
java --version
{% endhighlight %}
[![SS Openjdk 2](../../assets/openjdk-2.png)](../../assets/openjdk-2.png)

Selesai.
