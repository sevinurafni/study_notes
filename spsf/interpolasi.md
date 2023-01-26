### Interpolasi

Berbeda dengan regresi yang telag memiliki model terlebih dahulu dan juga terdapat lebih dari satu titik dengan nilai berbeda, pada interpolasi model atau fungsi yang dihasilkan harus melewati semua tiitk data sehingga tidak boleh terdapat lebih dari satu data dengan nilai variabel bebas yang sama

Interpolasi kedua pendekatan ini diberikan pada gambar berikut. 
 <p align="center">
 	<img src=img/inter1.jpg>
 </p>
 
 
### Interpolasi Linier
 
Terdapat f(x) yang akan diperoleh melalui interpolaso linier untuk $\forall \, x \in [0,1]$ atau $0 \leq x \leq 1$, di mana telah diperoleh data
 
	$y_0 = f(0)$
	$y_1 = f(1)$			...(1)
 
sehingga bila dapat ditentukan $f(x)$, harus selalu memenuhi persamaan (1).
<p align="center">
	<img src="img/inter2.jpg" alt="Raspberry pi" style="width:20%; border:0;">
</p>

untuk $x=0$ -> $f(0)=y_0$ yang dapat diperoleh dari garis - - -  berbentuk
	$(1-x)y_0$ 	(2)
	
dan untuk $x=1$ -> $f(1)=y_1$ diperoleh garis ++++
	$xy_1$		(3)

Dengan demikian dapat diteruskan $f(x)$ melalui penjumlahan Persamaan (2) dan (3)
	$f(x) = (1-x)y_0 + xy_1$	(4)

yang memenuhi 
	$f(0) = (1-0)y_0 + 0. y_1 = y_0$	(5)
dan
	$f(1) = (1-1)y_0 + 1. y_1 = y_1$	(6)

Sehingga persamaan (4) dapat diterima(?)

#### Untuk selang bukan $[0,1]$
Persamaan (4) dapat dibuat lebih umum dari selang $[0,1]$ menjadi $[x_i, x_(i+1)]$ sehingga berlaku untuk selang yang diinginkan,
<p align="center">
	<img src="img/inter3.jpg" alt="Raspberry pi" style="width:20%; border:0;">
</p>

Proses untuk membuat persamaan (4) menjadi lebih umum dilakukan dengan mencari variabel pengganti yang memenuhi $[0,1]$ untuk $[x_i, x_(i+1)]$ yang dalam hal ini dapat digunakan

	$$a{x_i} = \dfrac{x-x_i}{x_{i+1} - x_i} $$	(5)
yang akan memiliki
	$a(x_i) = 0$ dan $a(x_{i+1}  = 1$
	
Dengan dengan demikian persamaan (4) dapat dituliskan kembali menjadi
 ![insert persamaan 6]
 
merupakan persamaan yang dicari dari
	$f(x_i) = y_i*1 + y_{i+1} * 0 = y_i$	
	$f(x_{i+1}) = y_i*0 + y_{i+1} * 1 = y_{i+1}$
terlah terpenuhi

#### Bila terdapat n data

Untuk n buah data akan terbentuk $(n-1)$ selang di mana Persamaan (6) berlaku.
Untuk saat ini bebas selang digunakan tetap 
	$h = x_{i+1} - x_i$ (7)
Sehingga selang ke-i dapat diperoleh melalui
 ![insert persamaan 8]
 dengan ⌊ ⌋ $\lfloor x$ merupakan fungsi floor, eg
 	⌊7.5⌋ = 7
 	⌊ -2.5 ⌋ = -3
 
 Pemanfaatan persamaan (8) dan (7) akan menghasilkan interpolasi linier untuk n buah data.  
 
 
 ### Polinomial interpolasi Lagrange
 
 Interpolasi linier yang diberikan pada persamaan (6) dapat diperluas menjadi bentuk polinomial dengan memperhitungkan tidak hanya kedua titik data yang mengapit $x$ tetapi juga semua data yang diberikan.
 
 Dari persamaan (6) terlihat bahwa pengali dari suatu nilai $y_i$ adalah fungsi yang merupakan rasio dari sebuah x yang ditinjau terhadap data lain terhadap sebuah data lain dengan $x_i$
 	(x-x_i)/(x_j - x_i) 	(9)
 dengan j tidak sama dengan i
 
 untuk interpolasi tiga buah titik data dapat dituliskan 
  ![insert contoh]
  
 
