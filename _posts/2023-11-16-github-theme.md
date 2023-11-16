---
title: "Jekyll theme & github.io domain hosting"
excerpt: Шинээр үүсгэх вебсайтаа үнэгүй Jekyll theme ашиглан гоё дизайнтай болгоцгооё. Мөнхүү hosting хийхдээ github.io домайн ашиглахын тулд Githup repo-д push хийж сурцгаая!
date: 2023-11-16
header:
    teaser: /assets/images/github_blog_3.png
toc: true
toc_label: "Table of contents"
toc_icon: "cog"
categories:
    - Github Blog Tutorial
tags:
    - [Tutorial, Blog]
---

## Оршил
Сайн байцгаана уу? Энэ блогоор *Jekyll theme* ашиглан вебсайтаа дизайнтай болгож сурна. Өмнө нь хэлсэнчлэн Jekyll нь html хэл ашиглахгүйгээр markdown хэл ашиглаад webpage хийж өгдөг(*static webpage generator*) билээ. Jekyll-д jekyll theme гэх олон төрлийн website template-ууд байх бөгөөд үнэтэй, үнэгүй сонголтуудтай байгаа билээ. Блог хөтлөхөд үнэгүй jekyll theme-үүдээс ашиглахад ямар ч асуудалгүй болохоор үнэгүй theme дотроос [minimal-mistakes](https://github.com/mmistakes/minimal-mistakes) ашиглан блогны вебсайтаа дизайн хийцгээнэ. Энэхүү tutorial-аар дараах зүйлсийг хийх болно.
- Github repository шинээр үүсгэх
- minimal-mistakes татах
- шаардлагатай gemfiles татах
- Github repo-д push хийх

## Github account үүсгэх

Github Pages-д блогоо байршуулахын тулд Github дээр өөрийн гэсэн account-тай байх хэрэгтэй. 
> Github нь git болон webpage hosting үйлчилгээг үнэгүй олгодог бөгөөд Github private account-ын тохиолдолд хязгааргүй repository ашиглах боломжтой.  

Git болон Github талаар ойлголт байхгүй бол [git series](https://nini-tech23.github.io/categories/#git-series)-аар дамжуулан шинэ Github account нээх болон git ашиглан файлуудаа хэрхэн commit & push хийхийг сураарай.

## minimal-mistakes татах

Minimal mistakes source кодыг энэхүү [линк](https://github.com/mmistakes/minimal-mistakes)-ээр ороод git clone command эсвэл download zip дээр дараад татах болно.

![cloning theme repo](/assets/images/minmis_clone.png)

Download zip ашиглан татсан тохиолдолд all files extract хийнэ. 

## шаардлагатай gemfiles татах
Дараа нь тухайн minimal-mistakes directory-руугаа шилжээд Ruby package manager болох **bundle** command ашиглаад хэрэгтэй minimal-mistakes theme-д хэрэгтэй gemfile-уудаа татна.

```shell
$ unzip minimal-mistakes
$ cd minimal-mistakes
$ bundle
Fetching gem metadata from https://rubygems.org/..........
Fetching gem metadata from https://rubygems.org/.
Resolving dependencies...
Using rake 10.5.0
...
Bundle complete! 3 Gemfile dependencies, 47 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
```

Setup бэлэн болсны дараа нь өмнө ашигласан command болох **bundle exec jekyll serve**-аар өөрийн локал компьютер дээр minimal-mistakes template ашигласан вебсайт хэрхэн харагдахыг шалгах боломжтой.

```shell
$ bundle exec jekyll serve
```

Зааврын дагуу амжилттай хийсэн тохиолдолд дараах линкээр http://127.0.0.1:4000/ ороход дараах байдлаар харагдах болно.

![design of minimal-mistake theme](/assets/images/minmis_look.png)

## Github repo-д push хийх

Түрүүг хүртэл өөрийн локал компьютер хаягаа ашиглан вебсайтаа hosting хийж байсан бол одоо Github Pages-ын **web hosting** ашиглан өөрийн вебпейжээ интернэтд байршуулахыг суръя. Эхлээд, Github дээр [username.github.io](http://username.github.io) форматын дагуу username-ын оронд өөрийн Github account username ашиглаад шинэ repository үүсгэнэ. Дээрхи repository үүсгэвэл дараах хаягыг [https://username.github.io](https://username.github.io/) өөрийн блог вебсайт хаягаар хэрэглэх боломжтой болно.

![blog repo push](/assets/images/blog_repo_push.png)

Шинэ Github repository үүсгэсний дараа өмнө нь локал компьютер дээр татаж авсан minimal-mistakes directory доторхи бүх файл болон folder-уудаа push хийнэ

Github remote repository-оо дараах коммандын дагуу локал directory-д холбож git commit & push command ашиглан бүх файл болон folder-уудаа upload хийнэ.

```shell
$ git init
$ git remote add origin https://github.com/username/username.github.io.git
$ git remote -v #check connection of remote repo
$ git add .
$ git commit -m "Uploaded minimal-mistakes theme"
$ git push -u origin main
```

Тэгээд, заавраа зөв дагаад хийсэн тохиолдолд дараах линкээр [https://username.github.io](https://username.github.io/) нэвтрэхэд дараах дэлгэц гарч ирэх ёстой.

![look of the website](/assets/images/minmis_look.png)

Ингээд, энэ удаагийн блогоор дамжуулан та бүхэн хамгийн түгээмэл хэрэглэгддэг амархан **Jekyll Theme minimal-mistakes**-ыг ашиглан интернэтд **github.io** домайн нэрээр өөрийн блог сайтаа бий болгож сурлаа. 
>Дараагийн блогоор анхны постоо оруулж сурцгаая!