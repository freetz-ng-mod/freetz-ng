# PREREQUISITES: Installation der benötigten Pakete
Eine einfache Möglichkeit die benötigten Pakete zu installieren besteht darin, diesen Code per Copy and Paste auf der Konsole auszuführen!

### Distribution ermitteln
Wenn man vergessen hat welche Linux Version installiert ist kann dies so prüfen:

 - Linux Distribution:
```
$ hostnamectl status
  Operating System: Fedora 33 (Thirty Three)
	    Kernel: Linux 5.10.15-200.fc33.x86_64
```

 - Ubuntu Version:
```
$ lsb_release -d
Description:    Ubuntu 14.04.6 LTS
```

 - Maschinen Typ: `i686` bei 32-Bit x86 und `x86_64` bei 64-Bit x86:
```
$ uname -m
aarch64
```

### Fedora

 - System updaten:
```
sudo dnf -y update && sudo systemctl daemon-reload
```

 - Fedora 33 64-Bit:
```
sudo dnf -y groupinstall "Development Tools" "Development Libraries"
sudo dnf -y install zlib-devel.i686 libstdc++-devel.i686 openssl xz bc unar inkscape ImageMagick subversion ccache gcc gcc-c++ binutils autoconf automake libtool make bzip2 ncurses-devel ncurses-term zlib-devel flex bison patch texinfo gettext pkgconfig ecj perl perl-String-CRC32 wget glib2-devel git libacl-devel libattr-devel libcap-devel ncurses-devel.i686 glibc-devel.i686 libgcc.i686
```

 - Falls auf dem folgenden System ein 64-Bit Linux installiert ist wird zusätzlich benötigt:
```
sudo yum -y install ncurses-devel.i686 glibc-devel.i686 libgcc.i686
```

 - Fedora ~20 32-Bit:
```
sudo yum -y install ImageMagick subversion gcc gcc-c++ binutils autoconf automake libtool make bzip2 ncurses-devel zlib-devel flex bison patch texinfo gettext pkgconfig ecj perl perl-String-CRC32 wget glib2-devel git libacl-devel libattr-devel libcap-devel
```

### Ubuntu

Zum Umstellen auf eine deutsch Tastaturbelegung: `sudo locale-gen de_DE` und `sudo dpkg-reconfigure console-data` ausführen,
siehe [LocaleConf](https://help.ubuntu.com/community/LocaleConf)


 - System updaten:
```
sudo apt-get -y update
sudo apt-get -y upgrade
sudo apt-get -y dist-upgrade
```

 - Ubuntu 20 64-Bit:
```
sudo apt -y install lib32z1-dev unar inkscape imagemagick subversion git bc wget sudo ccache gcc g++ binutils autoconf automake autopoint libtool-bin make bzip2 libncurses5-dev libreadline-dev zlib1g-dev flex bison patch texinfo tofrodos gettext pkg-config ecj fastjar perl libstring-crc32-perl ruby gawk python libusb-dev unzip intltool libacl1-dev libcap-dev libc6-dev-i386 lib32ncurses5-dev gcc-multilib lib32stdc++6 libglib2.0-dev 
```

 - Ubuntu 16 64-Bit:
```
sudo apt -y install imagemagick subversion git bc wget sudo gcc g++ binutils autoconf automake autopoint libtool-bin make bzip2 libncurses5-dev libreadline-dev zlib1g-dev flex bison patch texinfo tofrodos gettext pkg-config ecj fastjar realpath perl libstring-crc32-perl ruby ruby1.9 gawk python libusb-dev unzip intltool libacl1-dev libcap-dev libc6-dev-i386 lib32ncurses5-dev gcc-multilib lib32stdc++6 libglib2.0-dev
```

 - Ubuntu 15 64-Bit:
```
sudo apt-get -y install imagemagick subversion git gcc g++ binutils autoconf automake autopoint libtool-bin make bzip2 libncurses5-dev libreadline-dev zlib1g-dev flex bison patch texinfo tofrodos gettext pkg-config ecj fastjar realpath perl libstring-crc32-perl ruby ruby1.8 gawk python libusb-dev unzip intltool libacl1-dev libcap-dev libc6-dev-i386 lib32ncurses5-dev gcc-multilib lib32stdc++6 libglib2.0-dev
```

 - Falls auf den folgenden Systemen ein 64-Bit Linux installiert ist wird zusätzlich benötigt:
```
sudo apt-get -y install libc6-dev-i386 lib32ncurses5-dev gcc-multilib lib32stdc++6
```

 - Ubuntu 15 32-Bit / Debian 8: Zusätzlich zu Ubuntu 13/14 32-Bit wird benötigt:
```
sudo apt-get -y install libtool-bin
```

 - Ubuntu 13/14 32-Bit:
```
sudo apt-get -y install graphicsmagick subversion gcc g++ binutils autoconf automake automake1.9 libtool make bzip2 libncurses5-dev libreadline-dev zlib1g-dev flex bison patch texinfo tofrodos gettext pkg-config ecj fastjar realpath perl libstring-crc32-perl ruby ruby1.8 gawk python libusb-dev unzip intltool libacl1-dev libcap-dev
```

 - Ubuntu 9/10/11/12 32-Bit:
```
sudo apt-get -y install imagemagick subversion gcc g++ bzip2 binutils automake patch autoconf libtool pkg-config make libncurses5-dev libreadline-dev zlib1g-dev flex bison patch texinfo tofrodos gettext pkg-config ecj fastjar realpath perl libstring-crc32-perl ruby ruby1.8 gawk python libusb-dev unzip intltool libglib2.0-dev xz-utils git-core libacl1-dev libattr1-dev libcap-dev
```

 - Ubuntu 9.04 32-Bit (kein automake 1.8, "ecj" statt "ecj-bootstrap"):
```
sudo apt-get -y install imagemagick subversion gcc g++ binutils autoconf automake automake1.9 libtool make bzip2 libncurses5-dev libreadline-dev zlib1g-dev flex bison patch texinfo tofrodos gettext pkg-config jikes ecj fastjar realpath perl libstring-crc32-perl ruby ruby1.8 gawk python libusb-dev unzip intltool libglib2.0-dev xz-utils git-core libacl1-dev libattr1-dev libcap-dev
```

