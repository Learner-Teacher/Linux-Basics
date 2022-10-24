# Linux Basics

[![DarkWeb](image/darkweb.png)](https://t.me/DarkWeb_o0o)

*Click <img src="image/star.png" width="18" height="18" align="absmiddle" title="Star" /> if you like the project. Pull Request are highly appreciated.*

<br/>

## Table of Contents

* [User Information](#1-foydalanuvchi-haqida-malumot)
* [File and Directory Commands](#-2-file-and-directory-commands)
* [File Permissions](#-3-file-permissions)
* [Networking](#-4-networking)
* [Installing Packages](#-5-installing-packages)
* [Disk Usage](#-6-disk-usage)
* [System and Hardware Information](#-7-system-and-hardware-information)
* [Search Files](#-8-search-files)
* [SSH](#-9-ssh)
* [Vi Editor](#-10-vi-editor)
* [Bash Script](#-11-bash-script)


# 1. Foydalanuvchi haqida ma'lumot

* **who** U hozirda tizimga kirgan foydalanuvchi haqida ma'lumot olish uchun ishlatiladi. Hech qanday variant yoki argument keltirmasangiz, buyruq tizimga kirgan har bir foydalanuvchi uchun quyidagi ma'lumotlarni ko'rsatadi.

    1. Foydalanuvchining login nomi
    2. Foydalanuvchi terminali
    3. Kirish sanasi va vaqti
    4. Foydalanuvchining masofaviy xost nomi

```js
$ who
admin    tty2         2022-02-10 01:36 (tty2)
root     pts/1        2022-02-15 00:29 (10.190.95.154)
```
* **whoami**: Bu tizimning foydalanuvchi nomini ko'rsatadi

```js
$ whoami
Abdulvoris Urolov
```
* **id**: Bu foydalanuvchi identifikatori (haqiqiy va samarali foydalanuvchi va guruh identifikatorlari) ma'lumotlarini ko'rsatadi.

```js
$ id
uid=1000(sj) gid=1000(sj) groups=1000(sj),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),120(lpadmin),131(lxd),132(sambashare)
```

* **group**: Bu buyruq foydalanuvchi tegishli bo'lgan barcha guruhlarni ko'rsatish uchun ishlatiladi.
  
```js
$ group
sj: sj, adm, cdrom, sudo, dip, plugdev, lpadmin, lxd, sambashare
```
* **users**: Hozirda tizimga kirgan barcha foydalanuvchilarning foydalanuvchi nomlarini ko'rsatadi.

```js
$ users
root
```

* **grep**: Bu tizim hisoblari faylidan ma'lum bir foydalanuvchi haqida ma'lumot topish uchun kuchli naqsh qidirish vositasi: /etc/passwd.

```js
$ grep -i sj /etc/passwd
sj:x:1000:1000:sj,,,:/home/sj:/bin/bash
```

* **W Command**:  Bu (W) hozirda tizimga kirgan foydalanuvchilar va har bir foydalanuvchi nima qilayotgani haqidagi ma'lumotlarni ko'rsatadigan buyruq qatori yordam dasturidir.

```js
w [OPTIONS] [USER]
Example:
w
 18:45:04 up  2:09,  1 user,  load average: 0.09, 0.07, 0.02
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT
sj       :0       :0               01:27   ?xdm?   1:14   0.01s /usr/lib/gdm3/g
```
* **last yoki lastb**: tizimga oxirgi marta kirgan foydalanuvchilar ro'yxatini ko'rsatadi. Siz ularning login va xost nomi ma'lumotlarini ko'rsatish uchun foydalanuvchi nomlarini yuborishingiz mumkin.

```js
last [options] [username...] [tty...]

Example:

root     pts/1        xx.xxx.xx.xxx    Tue Feb 15 00:29   still logged in
root     pts/2        xx.xxx.xx.xxx    Mon Feb 14 03:45 - 06:59  (03:13)
root     pts/1        xx.xxx.xx.xxx    Mon Feb 14 01:21 - 04:35  (03:13)
root     pts/1        xx.xxx.xx.xxx    Sun Feb 13 21:28 - 00:43  (03:15)
root     pts/1        xx.xxx.xx.xxx    Sun Feb 13 09:46 - 10:20  (00:33)
root     pts/1        xx.xxx.xx.xxx    Sat Feb 12 21:30 - 23:44  (02:13)
root     pts/1        xx.xxx.xx.xxx    Sat Feb 12 11:15 - 11:56  (00:40)
root     pts/1        xx.xxx.xx.xxx    Sat Feb 12 11:08 - 11:15  (00:06)
root     pts/1        xx.xxx.xx.xxx    Sat Feb 12 02:06 - 05:19  (03:12)
```

* **lastlog**: Buyruq lastlogbarcha foydalanuvchilarning yoki ma'lum bir foydalanuvchining so'nggi kirish ma'lumotlarini topish uchun ishlatiladi.

```js
$ lastlog

Username         Port     From             Latest
root             pts/1    xx.xxx.xx.xxx    Tue Feb 15 00:29:27 -0500 2022
daemon                                     **Never logged in**
bin                                        **Never logged in**
sys                                        **Never logged in**
sync                                       **Never logged in**
games                                      **Never logged in**
man                                        **Never logged in**
lp                                         **Never logged in**
mail                                       **Never logged in**
news                                       **Never logged in**
```

<div align="right">
  <b><a href="#table-of-contents">↥ mundarijaga qaytish</a></b>
</div>