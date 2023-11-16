---
title: "Github блог хөтөлж эхлэх бэлтгэл (set up)"
excerpt: "Github Pages хийхэд шаардлагатай программууд татан set up хийгээд туршилт маягаар жишиг блог оруулж үзэцгээе!"
date: 2023-11-07
header:
  teaser: /assets/images/github_blog_2.png
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
categories:
  - Github Blog Tutorial
tags:
  - [Blog, Tutorial]
---

## Оршил 
Сайн байцгаана уу? Энэхүү блогоор Github Pages дээр блогоо хөтөлж эхлэхэд бэлдэцгээе. Доорхи жагсаалт дахь зүйлсийг зааврын дагуу хийхэд л болно.
- Ruby татах
- Shell command ашиглаад jekyll болон bundler татах

Миний компьютер Windows system боловч unix-like environment комманд ашиглах боломжтой Git Bash interface ашиглан дараах заавруудыг бичсэн болно.
Тэгээд сүүлд нь бэлтгэл ажил бүрэн эсэхийг шалгах зорилгоор ямар ч агуулгагүй хоосон вебсайт туршилтаар хамтдаа хийх болно. 

## Ruby татах (Microsoft OS)
Эхлээд, өөрийн локал компьютер дээрээ Ruby хэмээх программ татах хэрэгтэй. 
> Ruby нь python эсвэл R-тай адилхан нэгэн төрлийн программийн хэл бөгөөд хэрэглэхэд хялбар болон бүтээмжтэй гэсэн давуу талтай. Ихэвчлэн веб хөгжүүлэлтэнд ихээхэн ашиглагддаг.

Энэхүү [линк](https://www.ruby-lang.org/en/downloads/)-ээр ороод татах боломжтой. Дараах shell command ашиглан шалгахад амжилттай татагдсан тохиолдолд Ruby version-ыг харуулах болно.
```shell
$ ruby -v
```

## Jekyll болон bundler татах
Дараа нь command shell дээр дараах command ашиглаад Jekyll болон bundler программуудыг татна.  
> Bundler нь Ruby-гийн package manager буюу dependency management хийж өгдөг tool билээ. Jekyll нь markdown файлыг html-руу хувирган хялбар байдлаар хөдөлгүүнгүй вебсайт үүсгэж өгдөг үүсгүүр программ. 

Зөв татсан эсэхээ түүнчлэн command shell дээрээ jekyll -v болон bundler -v гээд шалгах боломжтой.

```shell
$ gem install jekyll bundler
$ jekyll -v
$ bundler -v
```

## Туршилт блог үүсгэх

Блог үүсгэхэд шаардлагатай setup-аа амжилттай дуусгасан бол Jekyll хэрэглээд HelloBlog гэсэн homepage шинээр хийж үзье. Дараах `jekyll new HelloBlog` гэсэн комманд уншуулахад myHome гэсэн directory дотор шинэ HelloBlog гэсэн folder үүсэх бөгөөд түүн дотор шинэ Jekyll сайт татагдах болно.
```shell
$ jekyll new HelloBlog
Running bundle install in /home/myHome/HelloBlog...
  Bundler: Fetching gem metadata from https://rubygems.org/............
...
  Bundler: Bundle complete! 4 Gemfile dependencies, 29 gems now installed.
  Bundler: Use `bundle show [gemname]` to see where a bundled gem is installed.
New jekyll site installed in /home/myHome/HelloBlog.
```
Дараа нь шинэ сайт ямар харагдахыг шалгахын тулд HelloBlog гэсэн folder-руу шилжээд **bundle exec jekyll serve** гэсэн комманд ашиглан вебсайтыг интернэтэд hosting (байршуулах) болно. 

```shell
$ cd HelloBlog
$ bundle exec jekyll serve
Configuration file: /home/myHome/HelloBlog/_config.yml
            Source: /home/myHome/HelloBlog
       Destination: /home/myHome/HelloBlog/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
       Jekyll Feed: Generating feed for posts
                    done in 0.616 seconds.
 Auto-regeneration: enabled for '/home/myHome/HelloBlog'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

Web browser дээрээ дараах хаягыг http://127.0.0.1:4000/ хайж үзвэл дараах байдлаар jekyll-ын олгодог блогны үндсэн харагдах байдал гарж ирнэ.

![Welcome to Jekyll](/assets/images/welcome_jekyll.png)

127.0.0.1 хаяг нь computer network дотор өөрийн компьютерийн хаягийг илэрхийлж байгаа болохоор дээрхи блогыг бичсэн компьютероос л нэвтрэх боломжтой. Өөр компьютероос орохын тулд дараах коммандыг уншуулаад орох боломжтой

```shell
$ bundle exec jekyll serve -H 192.168.0.8
```

>Үр дүнд өөр төхөөрөмжөөс дараах хаягаар (http://192.168.0.8:4000/) дээрхи үүсгэсэн блогт нэвтрэх боломжтой.

Өнөөдрийн блогоор дамжуулан та бүхэндээ jekyll-ын provide хийж байгаа үндсэн блогыг үүсгэх болон хэрэгтэй программуудыг татахыг суралцлаа. Дараа блогоор илүү гоё template-ууд ашиглах болон блогоо web hosting domain ашиглаад интернэтд байршуулахыг суръя.