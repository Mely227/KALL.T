---
title: Matriks Linier

---

##### Matriks Invers
Matriks Invers adalah matriks yang jika dikalikan dengan matrikd aslinya menghasilkan matriks identitas.jika $A$ adalah matriks persegi berukuran $n x n$,maka invers dari $A$, yang dinotasikan sebagai $A^1$,memenuhi persamaan berikut:
$A x A^1=A^1 x A = I$

* Tugas Matriks Invers (1,0,0)
1. Langkah 1 membuat 3 persamaan variabel

$$
\begin{cases}  
4x_1 + 3x_2 - 2x_3 = 4 \\  
-5x_1 + 6x_2 + x_3 = -5 \\  
3x_1 - 2x_2 - 4x_3 = 3  
\end{cases}
$$

2. Langkah 2 ubah persamaan menjadi matriks

$$
A =
\begin{bmatrix}  
4 & 3 & -2 \\  
-5 & 6 & 1 \\  
3 & -2 & -4  
\end{bmatrix}
$$

$$
X =
\begin{bmatrix}  
x_1 \\  
x_2 \\  
X_3  
\end{bmatrix}
$$

$$
B =
\begin{bmatrix}  
4 \\  
-5 \\  
3  
\end{bmatrix}
$$

3. Langkah 3 Mencari invers $A^-1$
dengan Rumus:

$$
A^{-1} \times B =
\begin{bmatrix}
1 \\
0 \\
0
\end{bmatrix}
$$

4. Langkah 4 Menghitung Matriks Invers $A^1$

Selanjutnya untuk mencari $X$,kita menggunakan metode matriks invers,yaitu:

$$
X = A^{-1}B 
$$

Mencari invers dari matriks A yaitu dengan metode adjoin dan determinan atau redukasi baris.Hasil dari matriks A yaitu:

$$
A^{-1} =
\begin{bmatrix}  
\frac{6}{19} & \frac{-3}{19} & \frac{2}{19} \\  
\frac{5}{19} & \frac{4}{19} & \frac{1}{19} \\  
\frac{3}{19} & \frac{-2}{19} & \frac{-9}{19}  
\end{bmatrix}
$$

5. Langkah 5 Menghitung $X = A^{-1}B$
selanjutnya hitung satu persatu dengan yang $B$

$$
X =
\begin{bmatrix}  
\frac{6}{19} & \frac{-3}{19} & \frac{2}{19} \\  
\frac{5}{19} & \frac{4}{19} & \frac{1}{19} \\  
\frac{3}{19} & \frac{-2}{19} & \frac{-9}{19}  
\end{bmatrix}
\begin{bmatrix}  
4 \\  
-5 \\  
3  
\end{bmatrix}
$$

Hitung satu per satu:

$$
x_1 = \left( \frac{6}{19} \times 4 \right) + \left( \frac{-3}{19} \times (-5) \right) + \left( \frac{2}{19} \times 3 \right)
$$

$$
= \frac{24}{19} + \frac{15}{19} + \frac{6}{19} = \frac{45}{19} = 1
$$

$$
x_2 = \left( \frac{5}{19} \times 4 \right) + \left( \frac{4}{19} \times (-5) \right) + \left( \frac{1}{19} \times 3 \right)
$$

$$
= \frac{20}{19} - \frac{20}{19} + \frac{3}{19} = 0
$$

$$
x_3 = \left( \frac{3}{19} \times 4 \right) + \left( \frac{-2}{19} \times (-5) \right) + \left( \frac{-9}{19} \times 3 \right)
$$

$$
= \frac{12}{19} + \frac{10}{19} - \frac{27}{19} = 0
$$

###### 6 Maka solusi akhirnya 
hasilnya adalah:

$$
X =
\begin{bmatrix}  
1 \\  
0 \\  
0  
\end{bmatrix}
$$

sehingga hasilnya:

$$
x_1 = 1, \quad x_2 = 0, \quad x_3 = 0
$$


