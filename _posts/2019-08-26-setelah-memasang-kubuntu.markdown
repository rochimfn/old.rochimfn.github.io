---
layout: post
title:  "Hal yang dilakukan setelah memasang Ubuntu 18.04 Bionix beaver"
date:   2019-08-26 19:09:03 +0700
categories: ubuntu
---
[![Screenshot Kubuntu 18.04](../../assets/ssafterinstall.png)](../../assets/ssafterinstall.png)


Ubuntu merupakan distribusi GNU/Linux yang sangat populer. Selain karena sistemnya yang sangat stabil dan dukungan software yang lebih baik dibandingkan distribusi lainnya, Ubuntu juga ramah kepada pengguna baru dengan OS yang bisa digunakan secara langsung setelah dipasang karena memiliki banyak software preinstalled. Namun tidak semua orang membutuhkan(juga menyukai) software - software itu sehingga memilih Ubuntu dengan opsi penginstalan minimal, yaitu Ubuntu yang "hanya" disertai Desktop Environment, program essensial (misal web browser).

Hal - hal yang perlu dilakukan setelah memasang Ubuntu (minimal install)
* #### Update system
System perlu diperbarui terutama untuk mendapatkan patch keamanan terbaru
{% highlight shell %}
sudo apt update -y
sudo apt upgrade -y
{% endhighlight %}
* #### Memasang bash completion
Bash completion memudahkan asistensi pengetikan pada shell bash dengan fitur autocompletenya. Cara penggunaannya cukup tekan tombol `tab` setelah mengetikkan beberapa huruf awal perintah.
{% highlight shell %}
sudo apt install bash-completion
{% endhighlight %}
* #### Memasang codec multimedia
Codec diperlukan dalam pemutaran berbagai file multimedia
{% highlight shell %}
sudo apt install ubuntu-restricted-extras
{% endhighlight %}
* #### Memasang aplikasi pilihan dari repository bawaaan
{% highlight shell %}
sudo apt mpv audacious vim vlc telegram-desktop
{% endhighlight %}
>**mpv :** Program pemutar video yang sederhana dan ringan

>**audacious:** Program pemutar audio yang sangat populer

>**vim :** Program text editor yang berjalan di terminal

>**vlc :** Program pemutar video yang kaya fitur

>**telegram :** Program layanan chat berbasis cloud

* #### Memasang xdman
xdman merupakan program download manager yang gratis dan powerfull.
Download file tar.gz di [http://xdman.sourceforge.net/]()
{% highlight shell %}
tar xvzf Downloads/xdm*.tar.xz
cd xdm*
sudo ./install.sh
{% endhighlight %}
>pasang ekstensi browser monitoring di tiap browser

* #### Memasang Google Chrome
Google Chrome salah satu web browser terbaik yang ada
Download file .deb di [https://www.google.com/chrome/index.html]()
pasang dengan
{% highlight shell %}
sudo dpkg -i Downloads/google*deb
sudo apt -f install
{% endhighlight %}

* #### Memasang spotify client
Spotify merupakan penyedia layanan streaming musik dan podcast yang sangan populer
{% highlight shell %}
curl -sS https://download.spotify.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb http://repository.spotify.com stable non-free" | sudo tee /etc/apt/sources.list.d/spotify.list
sudo apt-get update && sudo apt-get install spotify-client
{% endhighlight %}

* #### Memasang tlp
tlp merupakan progam yang sangat umum digunakan untuk menghemat penggunaan baterai

{% highlight shell %}
sudo apt install tlp tlp-rdw
sudo tlp start
{% endhighlight %}

* #### Memasang program untuk developer
>**Git
{% highlight shell %}
sudo apt install git
{% endhighlight %}
>**Visual Studio Code**
Download file .deb di [https://code.visualstudio.com/Download]()
pasang dengan 
{% highlight shell %}
sudo dpkg -i Downloads/code*deb
sudo apt -f install
{% endhighlight %}
>**Sublime text 3** (via snap)
{% highlight shell %}
sudo snap install sublime-text --classic
{% endhighlight %}
>**Openjdk-11**
{% highlight shell %}
sudo apt install openjdk-11-jdk
{% endhighlight %}
>**Eclipse** (via snap)
{% highlight shell %}
sudo snap install --classic
{% endhighlight %}
>**nodejs & npm**
Tutorial: [https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/]()

### Selesai
