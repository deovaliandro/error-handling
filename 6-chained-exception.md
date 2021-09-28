Exception berantai memungkinkan untuk menghubungkan dua exception, yaitu sebuah
exception menjelaskan penyebab exception yang lain.

Contoh kasusnya ketika terjadi exception `ArithmeticException` karena pembagian
dengan nol, namun kasus sebenarnya bukan pada pembagian dengan nol namun karena
input angka pembagi yang bermasalah (I/O error) sehingga dibutuhkan exception
lain yang menjelaskan kejadian tersebut karena `ArithmeticException` tidak akan
mengetahui penyebabnya, ia hanya mengetahui bahwa error karena pembagian nol.

Ada 2 constructor yang mendukung sistem exception berantai:

1. Throwable(Throwable cause)
2. Throwable(String str, Throwable cause)

Perbedaannya di nomor 2 memungkinkan kita menambahkan deskripsi tentang
exception yang terjadi, dalam String.