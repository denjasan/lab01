## Laboratory work I

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [ ] 1. Ознакомиться со ссылками учебного материала
- [ ] 2. Выполнить инструкцию учебного материала
- [ ] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Tutorial

```bash
$ export GITHUB_USERNAME=<имя_пользователя>
$ export GIST_TOKEN=<сохраненный_токен>
$ alias edit=<nano|vi|vim|subl>
```

```sh
$ mkdir -p ${GITHUB_USERNAME}/workspace
$ cd ${GITHUB_USERNAME}/workspace
$ pwd
$ cd ..
$ pwd
```

```sh
$ mkdir -p workspace/tasks/
$ mkdir -p workspace/projects/
$ mkdir -p workspace/reports/
$ cd workspace
```

```sh
# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
$ tar -xf node-v6.11.5-linux-x64.tar.xz
$ rm -rf node-v6.11.5-linux-x64.tar.xz
$ mv node-v6.11.5-linux-x64 node
```

```sh
$ ls node/bin
$ echo ${PATH}
$ export PATH=${PATH}:`pwd`/node/bin
$ echo ${PATH}
$ mkdir scripts
$ cat > scripts/activate<<EOF
export PATH=\${PATH}:`pwd`/node/bin
EOF
$ source scripts/activate
```

```sh
$ gem install gist
```

```sh
$ (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)
```

## Report

```sh
$ export LAB_NUMBER=01
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gist REPORT.md
```

## Links

### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix))
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix))
- [cd](https://en.wikipedia.org/wiki/Cd_(command))
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix))
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix))
- [echo](https://en.wikipedia.org/wiki/Echo_(command))
- [env](https://en.wikipedia.org/wiki/Env_(shell))
- [ex](https://en.wikipedia.org/wiki/Ex_(editor))
- [file](https://en.wikipedia.org/wiki/File_(command))
- [find](https://en.wikipedia.org/wiki/Find)
- [ls](https://en.wikipedia.org/wiki/Ls)
- [man](https://en.wikipedia.org/wiki/Man_page)
- [mkdir](https://en.wikipedia.org/wiki/Mkdir)
- [mv](https://en.wikipedia.org/wiki/Mv)
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix))
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix))
- [pwd](https://en.wikipedia.org/wiki/Pwd)
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix))
- [sed](https://en.wikipedia.org/wiki/Sed)
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix))

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru)
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)
- [npm](https://docs.npmjs.com)

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details)
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf)
- [clang](https://clang.llvm.org)
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html)
- [make](https://en.wikipedia.org/wiki/Make_(software))
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html)
- [openssl](https://www.openssl.org)
- [nano](https://www.nano-editor.org)
- [tree](https://linux.die.net/man/1/tree)
- [vim](http://www.vim.org)

## Homework

1. Скачайте библиотеку *boost* с помощью утилиты **wget**. Адрес для скачивания `https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`.
<img width="816" alt="Pasted Graphic" src="https://user-images.githubusercontent.com/55495317/156125141-c266c227-d0a5-498e-ad85-ee8515686045.png">

2. Разархивируйте скаченный файл в директорию `~/boost_1_69_0`
<img width="498" alt="boost 1 69 0boost" src="https://user-images.githubusercontent.com/55495317/156186236-b46ff7fb-029c-46b7-b41a-ba8530209f1f.png">
<img width="439" alt="boost_1_69_0toolsquickbooktestxml_escape-1_5 gold-html" src="https://user-images.githubusercontent.com/55495317/156186244-ca632cbf-a5a6-4211-bbc3-4153184bc273.png">

3. Подсчитайте количество файлов в директории `~/boost_1_69_0` **не включая** вложенные директории.
<img width="377" alt="Pasted Graphic 3" src="https://user-images.githubusercontent.com/55495317/156186263-f8e4afc3-3430-42dc-82e5-b85fcd572f5e.png">

4. Подсчитайте количество файлов в директории `~/boost_1_69_0` **включая** вложенные директории.
<img width="322" alt="denjasan@man boost 1_69_0  ls -1" src="https://user-images.githubusercontent.com/55495317/156186281-29b6355d-e8ab-4c09-9aa9-992eb4a6d7bc.png">

5. Подсчитайте количество заголовочных файлов, файлов с расширением `.cpp`, сколько остальных файлов (не заголовочных и не `.cpp`).
<img width="513" alt="denjasan@man boost_1_69_0  1s -1" src="https://user-images.githubusercontent.com/55495317/156186302-d3502bc5-a5f6-4f67-af27-2efea8424c81.png">

6. Найдите полный пусть до файла `any.hpp` внутри библиотеки *boost*.
<img width="562" alt="UsersdenjasanTiNPboost_1_69_0boostfusionalgorithmqueryany hpp" src="https://user-images.githubusercontent.com/55495317/156186327-aa94381e-d7eb-4a90-ab52-7a39e1161e48.png">

7. Выведите в консоль все файлы, где упоминается последовательность `boost::asio`.
<img width="740" alt="Pasted Graphic 7" src="https://user-images.githubusercontent.com/55495317/156186331-ea29a79d-519b-4b4a-8cea-780f78cfdaab.png">

8. Скомпилирутйе *boost*. Можно воспользоваться [инструкцией](https://www.boost.org/doc/libs/1_61_0/more/getting_started/unix-variants.html#or-build-custom-
<img width="651" alt="Building Boost  Build engine with toolset darwin  toolsbuildsrcenginebin macosxarmb2" src="https://user-images.githubusercontent.com/55495317/156186351-5a5e8fda-c1f5-4aab-a1ae-69f6975b3573.png">

9. Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию `~/boost-libs`.
ncdu ~/boost-libs      
<img width="364" alt="denjasan@man boost_1_69_0  mv  ~boost-libs" src="https://user-images.githubusercontent.com/55495317/156186923-e7b15392-b8ad-4011-96bb-35a5fcc64460.png">


10. Подсчитайте сколько занимает дискового пространства каждый файл в этой директории.
<img width="738" alt="Pasted Graphic 10" src="https://user-images.githubusercontent.com/55495317/156186941-5c361762-fc8e-40a6-a147-e63674dbf8bc.png">

11. Найдите *топ10* самых "тяжёлых".
<img width="649" alt="11M Usersdenjasanboost-libslibsmathdocmath pdf" src="https://user-images.githubusercontent.com/55495317/156186960-8f3a17d2-74e7-4379-aee1-23f802e9d785.png">



```
Copyright (c) 2015-2021 The ISC Authors
```
