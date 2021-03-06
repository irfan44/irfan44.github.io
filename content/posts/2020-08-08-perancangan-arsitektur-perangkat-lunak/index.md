---
title: Perancangan Arsitektur Perangkat Lunak
date: 2020-08-08
cover:
    image: "images/front.jpg"
    relative: true
tags: ["Arsitektur Perangkat Lunak"]
license: false
---

Perancangan perangkat lunak merupakan salah satu tahapan dari SDLC (Software Development Live Cycle) yang dilakukan setelah proses analisis. Perancangan PL (perangkat lunak) adalah sebuah proses yang menghasilkan suatu model yang dapat memenuhi kebutuhan perangkat lunak. Proses perancangan perangkat lunak itu sendiri dibagi menjadi dua bagian, yaitu desain arsitektur dan detailed design. Kali ini kita akan membahas tentang perancangan arsitektur perangkat lunak.
 
Perancangan arsitektur merupakan perancangan yang menjelaskan bagaimana perangkat lunak dalam komponen yang mendefinisikan hubungan antar komponen, arsitektur, dan pilar desain yang membantu mencapai persyaratan yang ditetapkan. Sedangkan arsitektur itu sendiri menurut Krafzig et al, 2004, Arsitektur perangkat lunak adalah pernyataan-pernyataan yang menggambarkan struktur teknis, batasan, ciri-ciri, dan antarmuka komponen perangkat lunak dan juga merupakan rancangan fisik sistem perangkat lunak tersebut. Perancangan arsitektur yang baik sangatlah penting karena akan memiliki pengaruh yang signifikan kepada sistem. 

Dalam perancangan arsitektur terdapat beberapa architectural style yaitu :

## 1. Data Centered Architecture
Data centered architecture bisa diartikan sebagain arsitektur yang berpusat pada suatu data, biasanya data tersebut terletak di dalam suatu penyimpanan data seperti file atau database yang sering diakses oleh komponen lainnya dimana komponen tersebut saling memperbarui, menambahkan, menghapus, dan merubah data yang terdapat didalam penyimpanan data tersebut. Dengan menggunakan arsitektur ini, kita dapat mengubah atau menambhakn komponen tanpa mempengaruhi kinerja dari komponen lain karena masing-masing komponen beroperasi secara individu. 

![Data Centered Architecture](./images/datacentered.jpg#center)

## 2. Data flow architecture
Arsitektur ini digunakan ketika data yang diinput akan diubah melalui proses computational hingga menjadi output. Dalam architecture ini terdapat beberapa komponen yang disebut filter dan fiter tersebut dihubungkan oleh pipes atau pipa yang menghubungkan data dari satu komponen ke komponen lainnya. Setiap filter bekerja secara independen dan tanpa perlu mengetahui apa yang dilakukan oleh fiilter lainnya. Filter itu sendiri bekerja dengan cara memasukan suatu input tertentu dan mengeluarkan input tersebut menjadi output tertentu yang kemudian diberikan kepada filter selan  jutnya. Ketika aliran data menjadi satu garis peubah, maka akan terbentuk batch sequential. Dalam batch sequential tersebut data yang dimasukan akan diaplikasikan kedalam komponen sequential (filter) dan mengubahnya. 

![Data Flow Architecture](./images/dataflow.png#center)

## 3. Call and Return Architecture
Ketika menggunakan arsitektur ini, kita dapat membuat perangkat lunak yang mudah untuk diubah dan di scale. Dalam arsitektur ini terdapat 2 sub style, yaitu main program/subprogram dan remote procedure. Main program/subprogram dan remote procedure ini memiliki perbedaan dimana main program memiliki satu program utama yang terhubung dengan program lainnya sedangkan remote procedure menyebarkan program utama tersebut kedalam serangkaian komputer dalam network.

![Main Program/Subprogram](./images/mainprogram.png#center)

## 4. Layered Architecture 
Layered architecture, seperti namanya, merupakan suatu jenis arsitektur yang memiliki layer atau lapisan-lapisan yang saling terhubung dari lapisan yang paling luar hingga yang paling dalam. Setiap layer dalam arsitektur ini memiliki fungsi yang saling mendukung layer atas atau bawahnya. Dalam arsitektur ini, jika kita ingin mengubah satu layer maka tidak ada efek yang besar terhadap layer lainnya. Mirip seperti arsitektur data flow yang dimana ketika ada filter/komponen yang harus diubah, tidak diperlukan untuk mengganti banyak komponen lainnya. 

![Layered Architecture](./images/layered.jpeg#center)

Selain yang telah dijelaskan diatas, masih banyak jenis arsitektur lainnya yang ada. Setiap jenis memiliki kelebihan dan kekurangannya masing-masing dan kita dapat memilih arsitektur mana yang akan digunakan sesuai dengan perangkat lunak apa yang akan kita buat.

---

### Referensi :
- Anggraini, Dian. 2020. Software Design Fundamental [Pdf document] 
- Krafzig et al. 2004. Enterprise SOA: Service-Oriented Architecture Best Practices. Pretnice Hall
- Pressman, R.S. and Maxim, B. 2014. Software Engineering: A Practitioner's Approach. McGraw-Hill.