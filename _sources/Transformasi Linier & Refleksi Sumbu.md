---
title: Transformasi Linier & Refleksi Sumbu

---

### Transformasi Linier
##### Pengertian
Transformasi linier adalah pemetaan (fungsi) dari satu ruang vektor ke ruang vektor lain yang mempertahankan operasi penjumlahan dan perkalian skalar.
Bentuk umum:
$T: \mathbb{R}^n \to \mathbb{R}^m$

##### Syarat Transformasi Linier
Sebuah fungsi $T (v)$adalah transformasi linier jika untuk semua vektor $u,v$ dan skalar *c*,berlaku:

1. Penjumlahan vektor:
$T(u+v)=T(u)+T(v)$

2. Perkalian skalar:
$T(c v)=cT(v)$
Kalau kedua syarat di atas terpenuhi, maka 𝑇 adalah transformasi linier.

##### Tugas 1  Membuktikan bahwa $T(v1,v2)=(v1+v2,v1)$ adalah transformasi Linier

##### Jawaban
Transformasi $T(v1,v2)=(v1+v2,v1)$ didefinisikan sebagai:
$T(v1,v2)=(v1+v2,v1)$

Misalkan:

${u} = (u_1, u_2), \quad \mathbf{v} = (v_1, v_2)$

1. Cek Penjumlahan:

\begin{align*}
T(\mathbf{u} + \mathbf{v}) &= T((u_1 + v_1, u_2 + v_2)) \\
&= ((u_1 + v_1) + (u_2 + v_2), u_1 + v_1) \\
&= (u_1 + v_1 + u_2 + v_2, u_1 + v_1)
\end{align*}

Sementara itu:

$T(\mathbf{u}) = (u_1 + u_2, u_1), \quad T(\mathbf{v}) = (v_1 + v_2, v_1)$

$T(\mathbf{u}) + T(\mathbf{v}) = (u_1 + u_2 + v_1 + v_2, u_1 + v_1)$

Karena:

$ T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})$

2. Cek Perkalian Skalar:

\begin{align*}
T(c\mathbf{v}) &= T(cv_1, cv_2) \\
&= (cv_1 + cv_2, cv_1) \\
&= c(v_1 + v_2, v_1) \\
&= cT(\mathbf{v})
\end{align*}

3. Kesimpulan
Karena kedua sifat di atas dipenuhi, maka:

$T(v_1, v_2) = (v_1 + v_2, v_1) \text{ adalah transformasi linier.}$


##### Tugas 2  cari matriks rotasi,refleksi,shear,scala


1. Reflection about the x-axis
Matriks transformasi:


$\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}$


Contoh titik:

$
(2, 3) \rightarrow (2, -3) 
$

Gambar GeoGebra:

<iframe scrolling="no" title="Gambar 1" src="https://www.geogebra.org/material/iframe/id/xhfraxhe/width/1272/height/594/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="1272px" height="594px" style="border:0px;"> </iframe>



2. Reflection about the y-axis
Matriks transformasi:


$\begin{bmatrix}
-1 & 0 \\
0 & 1
\end{bmatrix}$


Contoh titik:

$
(3, 2) \rightarrow (-3, 2) 
$

Gambar GeoGebra:

<iframe scrolling="no" title="Gambar 2" src="https://www.geogebra.org/material/iframe/id/jxtushsj/width/630/height/586/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="630px" height="586px" style="border:0px;"> </iframe>


3. Reflection about the line $y = x$
Matriks transformasi:



$\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}$



Contoh titik:

$
(5, 7) \rightarrow (7, 5) 
$

Gambar GeoGebra:

<iframe scrolling="no" title="Gambar 3" src="https://www.geogebra.org/material/iframe/id/xwmzkx6q/width/630/height/586/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="630px" height="586px" style="border:0px;"> </iframe>


4. Reflection about the line $y = -x$
Matriks transformasi:


$\begin{bmatrix}
0 & -1 \\
-1 & 0
\end{bmatrix}$


Contoh titik:

$
(3, 1) \rightarrow (-1, -3) 
$

Gambar GeoGebra:

<iframe scrolling="no" title="Gambar 4" src="https://www.geogebra.org/material/iframe/id/r9ujtmxc/width/630/height/586/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="630px" height="586px" style="border:0px;"> </iframe>



5. Reflection about the origin
Matriks transformasi:


$\begin{bmatrix}
-1 & 0 \\
0 & -1
\end{bmatrix}$


Contoh titik:

$
(6, -3) \rightarrow (-6, 3) 
$

Gambar Geogebra:

<iframe scrolling="no" title="Gambar 5" src="https://www.geogebra.org/material/iframe/id/rpcufcnz/width/630/height/586/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="630px" height="586px" style="border:0px;"> </iframe>


##### Refleksi Sumbu X=2

```python=
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

# Titik-titik objek asli (misalnya, segitiga 3D)
points = np.array([
    [2, 3, 1],
    [1, 4, 3],
    [4, 2, 1]
]).T  # bentuknya 3xN

# Matriks refleksi terhadap bidang x = 0
reflection_matrix = np.array([
    [-1, 0, 0],
    [ 0, 1, 0],
    [ 0, 0, 1]
])

# Langkah-langkah untuk refleksi terhadap bidang x = 2:
# 1. Translasi ke kiri sejauh 2 satuan (x -= 2)
translated_points = points.copy()
translated_points[0] -= 2

# 2. Refleksi terhadap bidang x = 0
reflected_translated = reflection_matrix @ translated_points

# 3. Translasi kembali ke kanan sejauh 2 satuan (x += 2)
reflected_points = reflected_translated.copy()
reflected_points[0] += 2

# Buat plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

# Gambar objek asli (biru)
ax.plot(points[0], points[1], points[2], 'bo-', label='Asli')

# Gambar objek setelah refleksi (merah)
ax.plot(reflected_points[0], reflected_points[1], reflected_points[2], 'ro-', label='Refleksi')

# Tambahkan bidang bantu di x = 2
x_plane = np.full((2, 2), 2)  # bidang x = 2
y_plane, z_plane = np.meshgrid(np.linspace(0, 3, 2), np.linspace(0, 3, 2))
ax.plot_surface(x_plane, y_plane, z_plane, alpha=0.2, color='gray')

# Set aspek dan label
ax.set_xlabel('X')
ax.set_ylabel('Y')
ax.set_zlabel('Z')
ax.set_title('Refleksi terhadap bidang x = 2')
ax.legend()
ax.set_box_aspect([1,1,1])  # aspek rasio 1:1:1

plt.show()
```
![image](https://hackmd.io/_uploads/SyeTegffel.png)


##### Refleksi Sumbu y=2

```python=
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

# Titik-titik objek asli (misalnya, segitiga 3D)
points = np.array([
    [1, 1, 1],
    [2, 1, 1],
    [1.5, 2, 1]
]).T  # bentuknya 3xN

# Matriks refleksi terhadap bidang y = 0
reflection_matrix = np.array([
    [1,  0, 0],
    [0, -1, 0],
    [0,  0, 1]
])

# Langkah-langkah untuk refleksi terhadap bidang y = 2:
# 1. Translasi ke bawah sejauh 2 satuan (y -= 2)
translated_points = points.copy()
translated_points[1] -= 2

# 2. Refleksi terhadap bidang y = 0
reflected_translated = reflection_matrix @ translated_points

# 3. Translasi kembali ke atas sejauh 2 satuan (y += 2)
reflected_points = reflected_translated.copy()
reflected_points[1] += 2

# Buat plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

# Gambar objek asli (biru)
ax.plot(points[0], points[1], points[2], 'bo-', label='Asli')

# Gambar objek setelah refleksi (merah)
ax.plot(reflected_points[0], reflected_points[1], reflected_points[2], 'ro-', label='Refleksi')

# Tambahkan bidang bantu di y = 2
y_plane = np.full((2, 2), 2)  # bidang y = 2
x_plane, z_plane = np.meshgrid(np.linspace(0, 3, 2), np.linspace(0, 3, 2))
ax.plot_surface(x_plane, y_plane, z_plane, alpha=0.2, color='gray')

# Set aspek dan label
ax.set_xlabel('X')
ax.set_ylabel('Y')
ax.set_zlabel('Z')
ax.set_title('Refleksi terhadap bidang y = 2')
ax.legend()
ax.set_box_aspect([1,1,1])  # aspek rasio 1:1:1

plt.show()
```

![image](https://hackmd.io/_uploads/Hkl-blffee.png)


##### Refleksi Sumbu y=x

```python=
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

# Titik-titik objek asli (misalnya, segitiga 3D)
points = np.array([
    [1, 4, 2],
    [2, 3, 4],
    [3, 2, 1]
]).T  # bentuknya 3xN

# Matriks refleksi terhadap bidang y = x
reflection_matrix = np.array([
    [0, 1, 0],
    [1, 0, 0],
    [0, 0, 1]
])

# Lakukan refleksi
reflected_points = reflection_matrix @ points

# Buat plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

# Gambar objek asli (biru)
ax.plot(points[0], points[1], points[2], 'bo-', label='Asli')

# Gambar objek setelah refleksi (merah)
ax.plot(reflected_points[0], reflected_points[1], reflected_points[2], 'ro-', label='Refleksi')

# Tambahkan bidang bantu y = x di bidang z = 0–3
x_vals, y_vals = np.meshgrid(np.linspace(0, 3, 2), np.linspace(0, 3, 2))
z_vals = np.zeros_like(x_vals)
ax.plot_surface(x_vals, y_vals, z_vals, alpha=0.1, color='gray')

# Tambahkan garis bantu bidang y = x (di z = 0)
ax.plot([0, 3], [0, 3], [0, 0], 'k--', label='Bidang y = x (z=0)')

# Set aspek dan label
ax.set_xlabel('X')
ax.set_ylabel('Y')
ax.set_zlabel('Z')
ax.set_title('Refleksi terhadap bidang y = x')
ax.legend()
ax.set_box_aspect([1,1,1])  # aspek rasio 1:1:1

plt.show()
```

![image](https://hackmd.io/_uploads/rJkrWefMlx.png)
