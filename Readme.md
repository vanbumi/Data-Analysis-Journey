# Readme

---


---


### Join

```
left = canadian_youtube.set_index(['title', 'trending_date'])
right = british_youtube.set_index(['title', 'trending_date'])

left.join(right, lsuffix='_CAN', rsuffix='_UK')
```

**Keterangan**
```
left = canadian_youtube.set_index(['title', 'trending_date']):
```

Baris ini mengambil DataFrame canadian_youtube dan mengatur kolom title dan trending_date sebagai indeks. Dengan menggunakan set_index(), kita dapat mengakses data dengan lebih mudah berdasarkan kombinasi dari kedua kolom tersebut. Hasilnya disimpan dalam variabel left.
```
right = british_youtube.set_index(['title', 'trending_date']):
```

Baris ini mirip dengan baris sebelumnya, tetapi untuk DataFrame british_youtube. Kolom title dan trending_date juga diatur sebagai indeks, dan hasilnya disimpan dalam variabel right.

```
left.join(right, lsuffix='_CAN', rsuffix='_UK'):
```

Baris ini melakukan operasi join antara DataFrame left dan right. Metode `join(`) digunakan untuk menggabungkan dua DataFrame berdasarkan indeks mereka.

Parameter `lsuffix='_CAN' dan rsuffix='_UK'` digunakan untuk menambahkan akhiran pada kolom yang memiliki nama yang sama di kedua DataFrame. Ini mencegah konflik nama kolom setelah penggabungan. Misalnya, jika ada kolom yang sama di kedua DataFrame, kolom dari left akan diberi akhiran `_CAN`, dan kolom dari right akan diberi akhiran `_UK`.

Secara keseluruhan, kode ini bertujuan untuk menggabungkan data dari dua DataFrame (satu untuk YouTube Kanada dan satu untuk YouTube Inggris) berdasarkan kombinasi title dan trending_date, sambil memastikan bahwa kolom yang memiliki nama yang sama dapat dibedakan dengan akhiran yang sesuai.


