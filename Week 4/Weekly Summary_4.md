## **Asynchronous - Fetch**

## **Git dan Github Lanjutan**

Github dibuat untuk berkolaborasi bersama developer lain. Untuk berkolaborasi di satu repositori, para developer dapat membuat branchnya masing-masing.

- cara membuat branch

```
git branch branch-name
```

- berganti branch

```
git checkout branch-name
```

- menampilkan seluruh list branch yang ada

```
git branch
```

- menghapus branch

```
git branch -d branch-name
```

setelah masing-masing memiliki branch, branch tersebut dapat disatukan (merge) dengan mengajukan **pull request**. maka nantinya ketua tim akan memeriksa codingan yg akan dimerge dan (apabila tidak terjadi konflik) menerima pull request.

## **Responsive**

Responsive -> memungkinkan website **dapat diakses pada device apapun** dan **tampilannya masih bagus**.

Cara membuat sebuah website menjadi responsive:

### 1. viewport

viewport -> area website yg dapat diakses oleh user.

### 2. membuat gambar menjadi responsive menggunakan max-width

caranya adalah dengan memberikan properti **max-width** pada cssnya.

```css
img {
  max-width: 100%;
}
```

### 3. css relative units

absolute length:

- cm
- mm
- in
- px
- pt
- pc

relative length:

- em
- ex
- ch
- rem
- vw
- vh
- vmin
- vmax
- %

### 4. media query

media query digunakan utk membuat beberapa style tergantung pada jenis device.

cara menggunakannya adalah:

```css
@media not|only mediatype and (mediafeature and|or|not mediafeature) {
  /* code css */
}
```

breakpoint -> batas angka yang sudah ditentukan agar styling berubah

## **Bootstrap**

Bootstrap merupakan CSS Framework yang membantu developer dalam membuat website lebih cepat dan sudah otomatis responsive.

cara menggunakan bootstrap:

- pemasangan bootstrap
  ada beberapa cara, namun yang lebih mudah adalah menggunakan CDN.

- mengcopy code dari bootstrap ke file HTML
