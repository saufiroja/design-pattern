# Introduction To OOP

Pemrograman Berorientasi Objek (Object-Oriented Programming atau disingkat OOP) adalah paradigma pemrograman yang berfokus pada penggunaan objek-objek sebagai unit utama untuk merancang dan mengembangkan perangkat lunak. Paradigma ini memungkinkan pengorganisasian kode yang lebih terstruktur dan modular dengan cara menggabungkan data (atribut) dan fungsi (metode) ke dalam objek-objek yang mewakili entitas-entitas dalam dunia nyata. </br>

## Basic Of OOP

Object Oriented programming adalah sebuah paradigma yang didasarkan dengan konsep membungkus potongan-potongan data, dan perilaku yang terkait dengan datanya
ke dalam sebuah unit yang disebut `object`, yang dibangun dari sekumpulan `blueprint` yang disebut `class` oleh programmer.

### Object, Class

- Apakah kalian suka kucing? Kucing adalah sebuah `object`, dan kucing juga adalah sebuah `class`.</br>
  Kucing adalah sebuah `object` karena kucing memiliki atribut-atribut seperti `nama, warna, dan lain-lain`. </br>
  Kucing juga adalah sebuah `class` karena kucing adalah sebuah `blueprint` yang digunakan untuk membuat `object` kucing.
  Dalam `OOP`, object adalah sebuah instance dari sebuah `class`. Sebuah `class` dapat memiliki banyak object, dan setiap object memiliki atribut-atribut yang berbeda-beda.</br>
  Sebagai contoh, kucing memiliki atribut `nama, warna, dan lain-lain`. </br>
  Kucing yang berwarna hitam, dan kucing yang berwarna putih adalah dua object yang berbeda, namun keduanya adalah object dari class kucing.

  |   kucing   |        Kucing        |
  | :--------: | :------------------: |
  |   Field    |        Method        |
  |  (+) Name  |     (+) Breath()     |
  | (+) Gender |    (+) Eat(food)     |
  |  (+) Age   |   (+) Sleep(hours)   |
  | (+) Color  | (+) Run(destination) |

  Katakanlan kita memiliki seekor kucing bernama `kitten`, `kitten` disini adalah sebuah object dari class `Kucing`. </br>
  Setiap kucing memiliki attribute standar seperti `nama, warna, dan lain-lain`. </br>
  Setiap kucing juga memiliki method atau perilaku standar seperti `breath, eat, sleep, dan lain-lain`. </br>
  Secara kolektif, attribute dan method dari sebuah class disebut sebagai `field` dan `method`. </br>
  Contoh:

  | John as Kucing | Lucy as Kucing  |
  | :------------: | :-------------: |
  |  name = john   |   name = lucy   |
  | gender = male  | gender = female |
  |    age = 2     |     age = 1     |
  | color = black  |  color = white  |

  Bisa kita lihat bahwa `john` dan `lucy` adalah dua object yang berbeda, namun keduanya adalah object dari class `Kucing`. </br>
  Perbedaan antara `john` dan `lucy` adalah pada atribut-atributnya, `john` memiliki atribut `name = john`, sedangkan `lucy` memiliki atribut `name = lucy`. </br>
  Jadi, `class` adalah sebuah `blueprint` yang digunakan untuk membuat `object`. </br>

### Class hierarchies

- Semuanya terlihat baik-baik saja ketika memiliki 1 `class`, tetapi real program memiliki lebih dari 1 `class`.</br>
  Beberapa dari `class` ini mungkin di organisir dalam sebuah `hierarchy` atau `tree`. </br>
  Sebagai contoh, kita memiliki `class` `Kucing`, `Anjing`. </br>
  Ketiga `class` ini adalah `subclass` dari `class` `Hewan`. </br>
  Karena `Kucing`, `Anjing` adalah `subclass` dari `class` `Hewan`, maka `Kucing`, `Anjing` akan memiliki atribut dan method yang memiliki banyak kesamaan. </br>
  Sebagai `parent class`, seperti yang baru saja kita definisikan, maka `Hewan` bisa disebut dengan `superclass` dari `subclass` `Kucing`, `Anjing`. </br>
  Karena `subclass` mewarisi status dan perilaku dari `superclass`, maka hanya mendefinisikan atribut dan method yang berbeda dari `superclass` saja. </br>
  Contohnya seperti di `class` `Kucing` akan memiliki method `meow()`, sedangkan `class` `Anjing` akan memiliki method `bark()`. </br>

  |   Animal   |        Animal        |
  | :--------: | :------------------: |
  |   Field    |        Method        |
  |  (+) Name  |     (+) Breath()     |
  | (+) Gender |    (+) Eat(food)     |
  |  (+) Age   |   (+) Sleep(hours)   |
  | (+) Color  | (+) Run(destination) |

  |      Kucing       |        Anjing        |
  | :---------------: | :------------------: |
  |       Field       |        Field         |
  | (-) isNasty: bool | (+)bestFriend: Human |
  |      Method       |        Method        |
  |    (+) Meow()     |      (+) Bark()      |

  Dalam contoh diatas, kita bisa melihat bahwa `class` `Kucing` dan `Anjing` adalah `subclass` dari `class` `Animal`. </br>
  Dalam Asumsi diatas kita memiliki persyaratan bisnis terkait, kita dapat melangkah lebih jauh dan mengekstrak `class` jauh lebih umum lagi. </br>
  Seperti dalam organisasi Makhluk Hidup yang akan menjadi `superclass` dari `class` `Animal` dan `class` `Plant`. </br>
  Contoh seperti itu disebut dengan `class hierarchies` atau `class tree`. </br>

  ```
  - Makhluk Hidup (Superclass)
      - Animal (Subclass)
          - Kucing (Subclass)
          - Anjing (Subclass)
      - Plant (Subclass)
          - Pohon (Subclass)
          - Rumput (Subclass)
  ```

  Subclass dapat mengganti atau menambahkan perilaku dari superclass. Subclass dapat sepenuhnya mengganti perilaku default dari superclass, atau subclass dapat menambahkan perilaku baru ke superclass. </br>

## Pillars of OOP

Pilar Dasar dari OOP adalah:

### Abstraction

- Sebagian besar waktu ketika kamu membuat program dengan `OOP`, kamu membuat object berdasarkan object dunia nyata </br>
  Namun, kamu tidak perlu membuat object yang sama persis dengan object dunia nyata. </br>
  Tetapi, kamu hanya perlu membuat object yang memiliki atribut dan method yang nyata dalam konteks program yang kamu buat. </br>
  Sebagai contoh, sebuah class `pesawat` mungkin bisa ada di keduanya seperti `flight simulator` dan `flight booking app`. </br>
  Tetapi dalam konteks `flight simulator`, kamu hanya perlu membuat atribut dan method yang berkaitan dengan `flight simulator` saja. </br>
  Sedangkan dalam konteks `flight booking app`, kamu hanya mempedulikan tentang kursi dan peta yang mana kursi yang tersedia dan yang tidak. </br>

  |    Pesawat     |      Pesawat       |
  | :------------: | :----------------: |
  |     Field      |       Field        |
  |   (-) speed    |     (-) seats      |
  |  (-) altitude  |                    |
  | (-) rollAngle  |                    |
  | (-) pitchAngle |                    |
  |  (-) yawAngle  |                    |
  |     Method     |       Method       |
  |    (+)fly()    | (+) reserveSeats() |

  Abstraction adalah sebuah model dari object dunia nyata yang hanya menampilkan atribut dan method yang relevan dengan konteks program yang kamu buat. </br>

### Encapsulation

- Untuk menjalankan sebuah mobil, kamu hanya membutuhkan untuk menekan sebuah tombol.
  Kamu tidak perlu menyambungkan kabel dibawah mesih dll untuk memulai siklus tenaga mesin.
  Detail seperti itu disembunyikan dari kamu, dan kamu hanya perlu menekan sebuah tombol.
  Kamu hanya memiliki interface yang sederhana untuk mengoperasikan mobil.
  Ini menggambarkan bagaimana setiap object yang memiliki interface public dari suatu object, terbuka untuk interaksi dengan object lain.
- Encapsulation adalah kemampuan sebuah object untuk menyembunyikan bagian state dan perilaku dari object lain, dia hanya mengekspose limit interface ke seluruh program </br>
- Mengenkapsulasi sebuah object berarti menjadikannya `private` dan hanya bisa diakses oleh method yang ada di dalam class tersebut.
  Ada method yang lebih sedikit untuk membatasi yang disebut `protected` yang membuat anggota dari sebuah `class` hanya bisa diakses oleh `subclass` tersebut. </br>
- Interface dan abtrak class dari sebagian besar bahasa pemrograman didasarkan pada konsep `encapsulation` dan `abstraction`.
  Dalam `OOP` modern, mekanisme interface (biasanya dideclare dengan kata kunci interface atau protokol) yang mendefinisikan kontrak interaksi antara object.
  Itulah salah satu alasan mengapa interface hanya peduli dengan perilku object, dan mengapa kamu tidak dapat mendeklarasikan field di dalam interface. </br>
- Bayangkan kamu memiliki interface `FlyingTransport` dengan sebuah method `fly(origin, destination, passengers)`.
  Ketika mendesain `air transportaion simulator`, kamu dapat membatasi class `airport` untuk hanya dengan object yang mengimplementasikan interface `FlyingTransport`.
  Setelah itu, kamu dapat yakin bahwa object apapun yang dioperasikan oleh `airport`, apakah itu `airplane, helicopter, atau DomesticatedGryphon` yang aneh akan memiliki method `fly(origin, destination, passengers)`. </br>

- Contoh:

  |     Class Name      |                    Description                     |
  | :-----------------: | :------------------------------------------------: |
  |       Airport       |        (+) accept(vehicle: FlyingTransport)        |
  |   FlyingTransport   | fly(origin, destination, passengers) --> Interface |
  |     Helicopter      |      (+) fly(origin, destination, passengers)      |
  |      Airplane       |      (+) fly(origin, destination, passengers)      |
  | DomesticatedGryphon |      (+) fly(origin, destination, passengers)      |

  Kamu dapat mengubah implementasi method `fly` di class dengan cara apapun yang kamu inginkan, tetapi kamu tidak dapat mengubah signature method `fly` di interface `FlyingTransport`. </br>

### Inheritance

### Polymorphism

## Relationship Between Objects
