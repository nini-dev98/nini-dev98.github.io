---
title: "Command Line Interfaces (CLIs) танилцуулга & bash setup (Windows)"
excerpt: 
date: 2023-11-03
header: 
    teaser: /assets/inages/gitbash.png
toc: true
toc_label: Table of Contents
toc_icon: cog
categories: 
    - Command Line
tags:
    - [bash syntax, OS]
---
## Command Line interfaces (CLIs) танилцуулга
CLIs бол компьютерийн үйлдлийн системийн текстэн харилцах хэсэг юм. Энэхүү хэсэг нь хэрэглэгчээс комманд хүлээн авч компьютерийн үйлдлийн системд дамжуулан коммандын дагуу үйлдэл гүйцэтгэж өгдөг. Үүнийг ашиглан компьютерийн файл системийг өөрчлөх болон зохицуулах боломжтой. Өөрөөр хэлбэл шинэ файл үүсгэх, файлуудын агуулгыг өөрчлөх, файл устгах гэх мэт.
## Bash программ
Mac болон Linux гэх Unix систем дээр **Bash** хэмээх интерфэйс (CLI) ашигладаг бол Windows системийн хувьд өөр **Command prompt** хэмээх программтай. Bash болон Command prompt-д хэрэглэгдэх syntax болон коммандууд өөр бөгөөд хамгийн өргөн ашиглагддаг нь Bash билээ. Тиймээс Windows хэрэглэгч байсан ч гэсэн Git Bash татаад Unix OS interface ашиглаж байгаа юм шиг хэрэглэх нь илүү зүгээр.

> Command line хэрэглэхийн хамгийн том давуу тал бол өргөн хэрэглэгддэг коммандуудыг автоматуулж цаг хэмнэх болон энгийн коммандууд ашиглан хэцүү ажлуудыг хийж гүйцэгтэх юм.

## Windows дээр Git Bash татах болон setup хийх
Windows дээр Bash хэрэглэхийн тулд Git Bash хэмээх программ татах хэрэгтэй. Git Bash нь зөвхөн Linux CLI олгохоос гадна дараагийн блогуудаар тайлбарлах **Git**-ыг ч бас ашиглах боломжтой программ юм. 
1. <span style="background-color: #e0e0e0; color: green;">Энэхүү [Git Bash татах линк](https://gitforwindows.org/)-ээр орон dowload дээр дарах</span>
![download_1](/assets/images/gitbash_download.png)
2. <span style="background-color: #e0e0e0; color: green;">Татсан .exe файлаа зааврын дагуу *next* дээр даран *finish* хүртэл уншуулах. Бүх тохиргоог default дээр байлгах</span>
![download_2](/assets/images/gitbash_download_2.webp)
3. <span style="background-color: #e0e0e0; color: green;">Start menu-гаас Git Bash хайгаад интерфэйсээ нээх</span>
![download_3](/assets/images/gitbash_download_3.png)
4. <span style="background-color: #e0e0e0; color: green;">Шинэ Git Bash нээх болгонд дараах байдлаар home directory (~ тэмдэглээгээр тэмдэглэгддэг)-д нээгдэж эхлэх болно.</span>
![download_4](/assets/images/gitbash_download_4.png)

Энэхүү linux CLI болох Git Bash setup маань дууслаа. Дараагийн блогоор хэрхэн CLI дээр хамгийн өргөн хэрэглэгддэг коммандуудыг сурцгаая.

