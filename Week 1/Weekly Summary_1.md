# Minggu 1
&nbsp;

## Unix Command Line

- ### Command line interface 
  <div align="justify">Shell yang berbasis teks.
  
  <br>
- ### Shell 
  <div align="justify">Program yang digunakan untuk berkomunikasi atau memberi instruksi kepada sistem.\
  
  <br>
- ### Terminal Emulator 
  <div align="justify">Aplikasi untuk mengakses CLI.
  
  <br>
- ### Filesystem
  <div align="justify">Mengatur bagaimana data disimpan di dalam sebuah sistem. Biasanya bentuknya akan seperti pohon seperti gambar di bawah ini. Directory paling atas disebut dengan root directory.

  <img src="picture\fileSystem-Tree.png" alt="drawing" width="300"/>

  <br>
- ### Terminal Basic
  + Navigation
    - Ls untuk melihat isi folder yang ada di perangkat komputer. Terdapat 3 jenis ls, yaitu: "ls-r" untuk membuat daftar file, "ls-a" untuk menampilkan seluruh data termasuk yang tersembunyi, dan ls-al untuk menampilkan data yang lebih detail lagi.
      ```
      ls
      ls-a
      ls-r
      ```
    - Clear / ctrl + I untuk membersihkan seluruh tampilan pada program yang sedang dioperasikan.
      ```
      clear
      ```

  + File Manipulation
    - Touch untuk membuat file kosong atau bisa juga untuk mengubah timestamp file atau folder.
      ```
      touch newFile.type
      ```
    - Cp (copy paste) untuk menyalin file/data dari satu temlat ke tempat lain.
      ```
      cp Source Destination
      ```
    - Mv untuk memindahkan file dari satu tempat ke temapt lain.
      ```
      mv Source Destination
      ```
    - Rm (remove) untuk menghapus file.
      ```
      rm fileName
      atau
      rm -r folder/directory name
      ```
      
  + Folder/Directory Manipulation
    - Mkdir utnuk membuat direktori baru.
      ```
      mkdir folder-name
      ```
    - Cd untuk membuka folder yang dituju.
      ```
      cd directory-path
      ```
    - Pwd untuk mengetahui direktori mana yang sedang kita jalankan.
      ```
      pwd
      ```

  + Text
    - Echo untuk menambahkan data dalam sebuah file.
      ```
      echo <text to print on terminal>
      ```
    - Cat untuk membuat, menggabungkan, dan mengkonversikan data yang ada.
      ```
      Membuat file baru : cat > nama folder yang ingin dibuat.
      Menggabungkan file: cat folder 1 2 3 (tergantung jumlahnya) > nama folder yang menggabungkan folder tadi.
      Konversi file     : cat nama file | tr A-E atau E-A (mengurutkan file berdasarkan alfabet)
      ``` 
    - Nano untuk editing teks yang dikelompokkan berdasarkan garis tertentu (veritkal atau horizontal).

    - Vim/code/sublime

  + Installing something<div align="justify">Berikut beberapa instalasi yang membantu.
    - Brew
    - Apt
    - Rpm

  + Untuk terminal basic lainnya dapat dilihat pada link berikut: [Perintah Linux](https://bit.ly/3UI1Y8E)

&nbsp;

## Git dan Github Dasar

- ### Git
  <div align="justify"> Alat yang digunakan untuk manajemen source code. Git juga open source Version Control System (VCS) yang digunakan untuk menangani berbagai project kecil atau besar secara gratis dan efisien. Got juga dapat melacak perubahan dalam source code yang memungkinkan developer saling bekerja sama.
  
  <br>
- ### Github
  <div align="justify"> Layanan hosting internet untuk pengembangan perangkat lunak dan distributed VCS menggunakan Git. Github juga menyediakan VCS terdistribusi dari Git plus kontrol akses, pelacakan bug, permintaan fitur perangkat lunak, manajemen tugas, integrasi berkelanjutan, dan wiki untuk setiap proyek.

  <br>
- ### Mengapa penting
  <div align="justify"> Dengan sistem yang terdistribusi ini, para programmer atau developer tidak harus terkoneksi ke repositori sentral dan bisa bekerja di mana saja dan kapan saja secara asinkron.
  
  <br>
- ### Cara Instal Git
  Mendownload ubuntu terlebih dahulu, lalu.
    ```
    $ sudo apt install git -y
    ```
  
  <br>
- ### Perintah Dasar Git
  | Perintah   | Digunakan untuk   |
  |------------|-------------------|
  |`git init`  | inisialisasi proyek. membuat hidden subfolder bernama `.git` <br>berisi struktur data yg diperlukan *version control* |
  |`git clone` | membuat salinan lokal proyek yang sudah dibuat secara remote. |
  |`git add`   | menambahkan file ke tahap staging (persiapan sebelum langkah berikutnya). |
  |`git commit`| menyimpan snapshot (perubahan terakhir yg sudah ter-staging) ke dalam history.|
  |`git status`| menampilkan status perubahan: untracked, modified, atau staged.|
  |`git branch`| menampilkan branches (cabang-cabang) yang sedang dikerjakan secara lokal.|
  |`git merge` | menggabungkan dua branch yang berbeda jadi satu. |
  |`git pull`  | memperbarui repositori lokal dengan versi remote paling baru. |
  |`git push`  | memperbarui repositori remote dengan versi lokal paling baru. |

  Daftar perintah lain bisa kamu akses di sini: [Perintah Dasar Git](https://git-scm.com/docs).

  <br>
- ### Penggunaan Git
  Buat direktori dan inisialisasi proyek git.
    ```terminal
    $ git init my-repo
    ```
  Masuk ke dalam direktori.
    ```terminal
    $ cd my-repo
    ```
  Buat file di dalam repositori.
    ```terminal
    $ touch README.md
    ```
  Tambahkan file tersebut ke area staging.
    ```terminal
    $ git add README.md
    ```
  Commit area staging.
    ```terminal
    $ git commit -m "add README to initial commit"
    ```
  Tambahkan url repositori yang telah kamu buat. Jika belum membuatnya, ikuti panduannya di sini: [Create a Repository](https://guides.github.com/activities/hello-world/#repository)
    ```terminal
    $ git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
    ```
    Push perubahan ke github.
    ```terminal
    $ git push --set-upstream origin master
    ```

&nbsp;

## HTML

- ### Pengertian
  Hypertext Markup Language (HTML) adalah kode yang digunakan untuk menyusun halaman web dan isinya. Misalnya, konten dapat disusun dalam satu set paragraf, daftar poin berpoin, atau menggunakan gambar dan tabel data.

  <br>
- ### Sifat
  Bersifat statis karena hanya bertugas menampilkan konten yang diminta oleh developer. Perlu diingat bahwa HTML bukan bahasa pemrograman, sehingga HTML tidak bisa dinamis mengolah data.

  <br>
- ### Tools
  + Browser (chrome, microsoft edge, dan lainnya)
  + Code editor (vscode, sublime, dan lainnya)

  <br>
- ### Dasar-dasar HTML
  + Struktur HTML
    ```
    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device=width, initial-scale=1.0">
      <title>Document</title>
    </head>
    <body>
      Hello World!
    </body>
    </html>
    ```
  + Anatomi HTML

    <img src="picture\anatomiHTML.jpg" alt="drawing" width="400"/><br>

  + Elemen HTML
    HTML elemen didefinisikan dengan:
    1. Opening tag,
    2. Content, dan
    3. Closing tag.
    
    
  + Atribut HTML
    Atribut adalah properties dari elemen HTML.

    <img src="picture\atributHTML.png" alt="drawing" width="400"/><br>

  + Komen HTML
    ```
    <body>
      <div>
        <!-- Ini adalah syntax comment HTML-->
      </div>
    </body>
    ```

  + Cara Menjalankan HTML
    Cara mudahnya adalah dengan menginstall ekstensi "Live Server" pada Visual Studio Code. Live server akan automatis mereload tampilan HTML.
  
  + Single dan Double HTML
    <br> -> single
    <p>Text</p> -> double
  
  + Layout Website
    Biasa terdiri dari:
    + Header
    + Navigation bar
    + Main content
    + Footer

    <img src="picture\html-layout.svg" alt="drawing" width="400"/><br>
  
- ### HTML Tag
    |    Tag     | Digunakan untuk   |
    |------------|-------------------|
    |`<!-- -->`  | Comment           |
    | `<!DOCTYPE>`| Tipe dokumen |
    | `<a>` | Hyperlink |
    | `<audio>`| Sound content |
    | `<b>` | Bold|
    | `<button>` | Clikable button |
    | `<div>` | Section in a document |
    | `<h1>` sampai `<h6>` | Headings |
    | `<img>` | Image|
    | `<link>` | Link|
    | `<nav>` | Navigation links|
    | `<p>` | Paragraph |
    | `<span>` | Section in a document|
    Untuk mengetahui lebih banyak lagi tag dapat lihat pada link berikut: [HTML Tags](https://www.w3schools.com/TAGS/default.asp)
  
&nbsp;

## CSS

- ### Pengertian
  CSS adalah bahasa komputer yang digunakan untuk menambahkan design ke suatu halaman website di internet agar terlihat lebih cantik/menarik. CSS adalah singkatan dari Cascading Style Sheets. Kita ibaratkan HTML adalah kerangka yang memberi sturuktur pada website, maka CSS adalah baju yang memberi warna dan layout pada website.

- ### Penggunaan CSS
  + Inline Styles (langsung pada atribut HTML)
    ```
    <p style="color:pink>Ini warna pink</p>
    ```
  
  + Internal CSS (dengan menambahkan tag `<style>` yang diletakkan di dalam elemen `<head>`)
    ```
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    body {
      background-color: bisque;
    }

    h1 {
      color: maroon;
      margin-left: 40px;
    } 
    </style>
    </head>
    <body>

    <h1>This is a heading</h1>
    <p>This is a paragraph.</p>

    </body>
    </html>
    ```
    Maka akan terlihat kayak gini:<br>
    <img src="picture\internalCSS.jpg" alt="drawing" width="400"/><br>
  
  + Eksternal CSS (menambahkan CSS dengan buat file CSS yang terpisah terus dikoneksikan dengan HTML)

    file index.html
    ```
    <!DOCTYPE html>
    <html>
    <head>
    <link rel="stylesheet" href="mystyle.css">
    </head>
    <body>

    <h1>This is a heading</h1>
    <p>This is a paragraph.</p>

    </body>
    </html>
    ```

    file mystyle.css
    ```
    body {
      background-color: lightblue;
    }

    h1 {
      color: navy;
      margin-left: 20px;
    }
    ```

    Maka akan terlihat kayak gini:<br>
    <img src="picture\externalCSS.jpg" alt="drawing" width="400"/><br>
  
&nbsp;

## Algortima & Pseudocode

  - ### Pengertian
    + Algoritma adalah deskripsi berupa step by step yang dibutuhkan untuk menyelesaikan suatu masalah.
    + Pseudocode adalah menuliskan algoritma dengan umumnya bahasa inggris sebelum kita implementasikan ke bahasa pemograman tertentu.
  
  - ### Contoh Algoritma Sederhana
    + Step 1: Start.<br>
    + Step 2: Declare variables num1, num2, and sum.<br>
    + Step 3: Read values num1 and num2.<br>
    + Step 4: Add num1 and num2 and assign the result to sum (sum<-num1+num2).<br>
    + Step 5: Display sum.<br>
    + Step 6: Stop.
  
  - ### Contoh Pseudocode
    ```
    STORE "width" with any value
    STORE "height" with any values
    STORE "area" without any value
    
    CALCULATE "width" times "height"
    SET "area" value with calculation result
    DISPLAY "area"
    ```

  - ### Pseudocode Berdasarkan Kondisi Masalah
    + Procedural (cara berpikir secara runtun).
    + Conditional (Dibutuhkan saat percabangan khusus).
      ```
      IF "score" < 70
        DO "learn more"
      ELSE
        DO "reward myself"
      DO "continue with life..."
      ```
    + Loopin (proses yang sama berulang-ulang)
      ```
      STORE "count" to 1
      
      WHILE "count" < 11
        DISPLAY "count"
        CALCULATE "count" mod 2
        STORE "remainder" to the result of calculation
        IF "remainder" equals to 0
          DISPLAY "EVEN"
        ELSE
          DISPLAY "ODD"
        ```
    + Recursive (algoritma yang memanggil methode/function di dalam sebuah function)  

&nbsp;

## Javascript

  - ### Pengertian
    Javascript adalah bahasa pemrogramana yang sangat powerful yang digunakan untuk logic pada sebuah website dan dapat membuat website menjadi interaktif dan dinamis.

  - ### Syntax dan Statement
    + Syntax bisa dianalogikan seperti vocab dan grammar pada bahasa pemrograman.
    + Contohnya: Alert(), prompt(), confirm().
  
  - ### Comments
    + Single comments
      ```
      // prints 5 to the console
      console.log(5);
      ```
      ```
      console.log(5); //print 5
      ```
    + Multiline comments
      ```
      /*
      This is all commented
      console.log(10);
      None of this is goin to run!
      console.log(99);
      */
  
  - ### Tipe Data dan Variabel
    + Tipe data: number, string, boolean, null, undefined, object.
    + Variabel: var, let, const.
  
  - ### Conditional (statement percabangan)
    + If statement
      ```
      let lapar = true;
      if (lapar){
        console.log('Yuk makan');
      }
      ```
    + If ... Else statement
      ```
      let lapar = false;
      if (lapar){
        console.log('Yuk makan'); // tidak ditampilkan statement ini
      } else{
        console.log('Tidak makan'); // ditampilkan statement ini
      }
      ```
    + If ... Else If statement
      ```
      let lampu = 'yellow';
      if (lampu === 'red'){
        console.log('stop');
      } else if (lampu === 'yellow'){
        console.log('slow down');
      } else if (lampu === 'green'){
        console.log('go');
      } else{
        console.log('caution, unknown');
      }
      ```
    + Switch case
      ```
      var buttonPushed = 1;
      switch(buttonPushed){
        case 1:
          {console.log('matikan tv!'); break;}
        case 2:
          {console.log('turunkan volume tv!'); break;}
        case 3:
          {console.log('tingkatkan volume tv!'); break;}
        case 4:
          {console.log('matikan suara tv!'); break;}
        default:
          {console.log('tidak terjadi apa-apa'); break;}
      }
      ```
    + Ternary operator (short syntax dari statement if...else)
      ```
      let isNowSale = true;
      isNowSale ? console.log('Lets shopping now') : console.log('shopping later');
      ```
  
  - ### Looping (perulangan)
    + Manual looping
    + For loop (tahu seberapa banyak nilai pasti untuk perulangannya)
      ```
      let angka = 1;
      for (angka; angka <= 10; angka++){
        console.log(angka);
      }
      ```
    + While loop (tidak tahu seberapa banyak nilai pasti untuk perulangannya)
      ```
      let angka = 1;
      while (angka <= 10){
        console.log(angka);
        angka++;
      }
      ```
    + Do while
    + Nested loop
  
  - ### Scope 
    + Blocks: code yang berada di dalam curly braces {}.
    + Global scope: code yang berada di luar curly braces {}.
    + Local scope: mendeklarasikan variabel di dalam blocks.

  - ### Function
    + Membuat function<br>
      <img src="picture\anatomiFunction.jpg" alt="drawing" width="350"/><br>
      <br>
    + Memanggil function<br>
      <img src="picture\memanggilFunction.jpg" alt="drawing" width="400"/><br>
      <br>
    + Parameter<br>
      <img src="picture\parameter.jpg" alt="drawing" width="400"/><br>
      <br>
    + Argument<br>
      <img src="picture\argument.jpg" alt="drawing" width="400"/><br>\
      <br>
    + Default parameters
    + Function helper
    + Arrow function
    + Short syntax function