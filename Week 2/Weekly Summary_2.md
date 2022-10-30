# Minggu 2
&nbsp;

## DOM

- ###  Pengertian
    Document Object Model (DOM?) adalah interface yang memungkinkan developer memanipulasi halaman web dari segi struktur, tampilan, dan kontennya.

- ### Fungsi
    Fungsi DOM adalah memanipulasi halaman website menjadi lebih dinamis dengan cara mengambil, mengubah, menambah, dan menghapus elemen HTML. DOM juga mengumpulkan data, fungsi, dan atribut milik elemen yang diakses yang kemudia digunakan untuk hal lain seperti Application Programming Interface (API).

- ### Mengambil Elemen HTML
    + ID
        Menggunakan method getElementByID(). contoh:
        ```
        var title = document.getElementByID('footer-title');
        ```
    + Class
        Menggunakan method getElementByClassName(). contoh:
        ```
        var items = document.getElementByClassName('list-items');
        ```
    + Nama Tag
        Menggunakan method getElementByTagName(). contoh:
        ```
        var listItems = document.getElementByTagName('li');
        ```
    + querySelector
        Menggunakan method querySelector. contoh:
        1. Mengambil elemen CSS dengan ID:
            ```
            var header = document.querySelector('#footer');
            ```
        2. Mengambil elemen CSS dengan class:
            ```
            var items = document.querySelector('.list-items');
            ```
        3. Mengambil elemen CSS dengan tag:
            ```
            var headings = document.querySelector('h2');
            ```
        4. Mengambil elemen CSS secara lebih spesifik:
            ```
            document.querySelector('h2.footer');
            ```
        5. Mengambil elemen CSS dengan querySelectorAll:
            ```
            var heading = document.querySelectorAll('h1.heading');
            ```
    
    - ### Mengubah Elemen HTML
        + Konten HTML
            Menggunakan properti innerHTML yang dapat dikombinasikan dengan methid getElementByID() atau getElementByTagName(). Contoh:
            ```
            document.getElementById(“#header”).innerHTML = “Hello World!”;
            atau
            document.getElementsByTagName("div").innerHTML = "<h2>Hello World!</h2>"
            ```
        
        + Style/tampilan
            Mengubah style elemen HTML maupun CSS perlu mengubah properti style terlebih dahulu.
            ```
            document.getElementById(id).style.property = new style
            ```
            Contoh:
            ```
            document.getElementsByTag(“h2”).style.borderBottom = “solid 5px #FFF”;
            ```
    
    - ### Menambah dan Menghapus Elemen 
        + Menambah Elemen
            Menggunakan method createElement(). Contoh:
            ```
            var div = document.createElement(‘div’);
            ```
        
        + Menghapus Elemen
            Memakai method removeChild(). Contoh:
            ```
            var elem = document.querySelector('#footer);
            elem.parentNode.removeChild(elem);
            ```

        + Mengganti Elemen
            Membuat elemen baru seperti ini:
            ```
            var div = document.querySelector('#div');
            var newDiv = document.createElement(‘div’);
            ```
            Kemudian, waktunya mengganti elemen di atas. Caranya dengan menulis script di bawah:
            ```
            newDiv.innerHTML = "Hello World2";
            div.parentNode.replaceChild(newDiv, div);
            ```
        
        + Menulis Ellemen Langsung ke HTML Output Stream
            Menggabungkan HTML dan JavaScript ke dalam satu baris kode. Nah, hal ini bisa dilakukan dengan method write() seperti di bawah:
            ```
            document.write(“<h2>Hello World!</h2><p>This is an example text!</p>”);
            ```
    - ### EventListener
        + Click
        + Blur
        + Form Submission