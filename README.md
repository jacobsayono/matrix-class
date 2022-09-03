# Matrix-Class
## A set of class methods used for common matrix operations

### Addition / Subtraction
Matrix addition and subtraction is an element by element operation. Two matrices must have the same dimensions in order to be added or subtracted.

$$\mathbf{A} + \mathbf{B} = \begin{bmatrix}
a_{11} & a_{12}  & \dots  & a_{1n}\\ 
a_{21} & a_{22}  & \dots &a_{2n} \\ 
\vdots & \vdots & \ddots  & \vdots \\ 
a_{m1} & a_{m2}  & \dots  & a_{mn}
\end{bmatrix} + \begin{bmatrix}
b_{11} & b_{12}  & \dots  & b_{1n}\\ 
b_{21} & b_{22}  & \dots &b_{2n} \\ 
\vdots & \vdots  & \ddots  & \vdots \\ 
b_{m1} & b_{m2}  &  \dots & b_{mn}
\end{bmatrix}$$

$$= \begin{bmatrix}
a_{11}+b_{11} & a_{12}+b_{12}  & \dots  & a_{1n}+b_{1n}\\ 
a_{21}+b_{21} & a_{22}+b_{22}  & \dots & a_{2n}+b_{2n} \\ 
\vdots & \vdots  & \ddots  & \vdots \\ 
a_{m1}+b_{m1} & a_{m2}+b_{m2}  &  \dots & a_{mn}+b_{mn}
\end{bmatrix}$$

### Scalar Multiplication
When multiplying a matrix $\mathbf{A}$ by a scalar $c$, all of the entries in $\mathbf{A}$ are multiplied by $c$:

$$c\mathbf{A} = c \begin{bmatrix}a_{11} & a_{12}  & \dots  & a_{1n}\\ 
a_{21} & a_{22}  & \dots &a_{2n} \\ 
\vdots & \vdots & \ddots  & \vdots \\ 
a_{m1} & a_{m2}  & \dots  & a_{mn}
\end{bmatrix} = \begin{bmatrix} ca_{11} & ca_{12}  & \dots  & ca_{1n}\\ 
ca_{21} & ca_{22}  & \dots &ca_{2n} \\ 
\vdots & \vdots & \ddots  & \vdots \\ 
ca_{m1} & ca_{m2}  & \dots  & ca_{mn}\end{bmatrix}$$

### Matrix Multiplication
Multiplication of Matrix $\mathbf{A}$ with matrix $\mathbf{B}$ is only possible if the width of $\mathbf{A}$ is equal to the height of $\mathbf{B}$

If $\mathbf{A}$ is an $m \times n$ matrix and $\mathbf{B}$ is an $n \times p$ matrix, their product $\mathbf{AB}$ is an $m \times p$ matrix.

When multiplying two matrices, we can calculate the value of the element at row $i$ and column $j$ with the following equation:

$$(\mathbf{AB})_{ij} = \sum_{k=1}^n a_{ik}b_{kj}$$

### Transpose
The transpose of a matrix $\mathbf{A}$ is given by $\mathbf{A^T}$ and can be thought of in several ways:

* The **rows** of $\mathbf{A^T}$ are the **columns** of $\mathbf{A}$.
* The **columns** of $\mathbf{A^T}$ are the **rows** of $\mathbf{A}$.

Mathematically, the element at row $i$ and column $j$ of the transpose is given by:

$$[\mathbf{A^T}]_{ij} = [\mathbf{A}]_{ji}$$

### Trace
The trace of an $n\times n$ square matrix $\mathbf{A}$ is the sum of the elements on the **main diagonal** of the matrix. 

$$\text{tr}\left(\mathbf{A}\right) = \sum_{i=1}^n a_{ii} = a_{11} + a_{22} + \dots + a_{nn}$$

### Determinant
The determinant is a useful value when describing a matrix. It can be denoted in one of three ways:

1. $\text{det } \left(\mathbf{A}\right)$
2. $\text{det } \mathbf{A}$
3. $|\mathbf{A}|$

**1x1 Matrices**

The determinant of a $1\times1$ matrix is just the value of the matrice's only element. For example if $\mathbf{A} = \begin{vmatrix}4\end{vmatrix}$, then the determinant of $\mathbf{A}$ is given by:

$$\begin{vmatrix}\mathbf{A}\end{vmatrix} = 4$$

**2x2 Matrices**

The determinant of a $2\times2$ matrix is given by:

$$\begin{vmatrix}\mathbf{A}\end{vmatrix} = \begin{vmatrix}
a & b \\
c & d \end{vmatrix} = ad - bc
$$

**Larger Matrices**

If you are interested in learning more you should look at the Wikipedia article: [Determinant](https://en.wikipedia.org/wiki/Determinant).

### Inverse
The inverse of a matrix $\mathbf{A}$ is given by $\mathbf{A^{-1}}$

A matrix $\mathbf{A}$ is **invertible** if there exists a matrix $\mathbf{B}$ such that the product of $\mathbf{A}$ and $\mathbf{B}$ is the **identity matrix** $\mathbf{I}$:

$$\mathbf{AB} = \mathbf{BA} = \mathbf{I}$$

**1x1 Matrices**

For a $1\times1$ matrix with a single element with value $a$, the inverse is simlpy $\frac{1}{a}$

**2x2 Matrices**

The inverse of a $2\times 2$ matrix is given by the following equation:

$$\mathbf{A}^{-1} = \frac{1}{\text{det }\mathbf{A}} \left[\left(\text{tr } \mathbf{A}\right) \mathbf{I} - \mathbf{A}\right]$$


**Larger Matrices**

If you are interested in learning more you should look at the Wikipedia article [Invertible Matrix](https://en.wikipedia.org/wiki/Invertible_matrix).
