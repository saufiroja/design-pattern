# Introduction To OOP

## Basic Of OOP

Object Oriented programming adalah sebuah paradigma yang didasarkan dengan konsep membungkus potongan-potongan data, dan perilaku yang terkait dengan datanya
ke dalam sebuah unit yang disebut `object`, yang dibangun dari sekumpulan `blueprint` yang disebut `class` oleh programmer.

- Object, Class

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

- Class hierarchies

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

## Relationship Between Objects
