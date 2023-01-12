# Section 1.1 Systems of Linear Equations
## 01-10-2023
* A linear equation in the variables $x_1, \dots, x_n$ is an equation that can be written in the form $$a_1x_1 + a_2x_2 + \cdots + a_nx_n = b$$where $b$ and the coefficients $a_1, \dots, a_n$ are real or complex numbers that are usually known in advance.

* A system of linear equations is a collection of one or more linear equations involving the same variables $x_1, \dots, x_n$.
* A solution of the system is a list $(S_1, S_2, \dots, S_n)$ of numbers that makes each equation a true statement when the value $S_1, \dots, S_n$ are substituted for $x_1, \dots, x_n$, respectively
* The set of all possible solutions is called the solution set of the linear system.
* Two linear systems are called equivalent if they have the same solution set.

* A system of linear equations has
	1) no solution
	2) exactly one solution
	3) infinitely many solutions
* A system of linear equations is said to be *consistent* if it has either one solution or finitely many solutions.
* A system of linear equations is said to be *inconsistent* if it has no solution.

**Example 1**: Solve the given system of equations
$$
\begin{align*}
	x_1 - 2x_2 + x_3 &= 0 \\
	2x_2 - 8x_3 &= 8\\
	-4x_1 + 5x_2 + 9x_3 &= -9	
\end{align*}
$$
Coefficient matrix
$$
\begin{bmatrix}
	1 & -2 & 1 & | & 0\\
	0 & 2 & -8 & | & 8\\
	-4 & 5 & 9 & | & -9
\end{bmatrix}
$$
Step 1: $4R_1 + R_3$
$$
\begin{bmatrix}
	1 & -2 & 1 & | & 0\\
	0 & 2 & -8 & | & 8\\
	0 & -3 & 13 & | & -9	
\end{bmatrix}
$$
Step 2: $\frac 12 R_2$
$$
\begin{bmatrix}
	1 & -2 & 1 & | & 0\\
	0 & 1 & -4 & | & 4\\
	0 & -3 & 13 & | & -9
\end{bmatrix}
$$
Step 3: $3R_2 + R_3$
$$
\begin{bmatrix}
	1 & -2 & 1 & | & 0\\
	0 & 1 & -4 & | & 4\\
	0 & 0 & 1 & | & 3\\
\end{bmatrix}
$$
$$
\begin{align*}
	x_1 - 2x_2 + x_3 &= 0 \\
	x_2 - 4x_3 &= 4 \\
	x_3 &= 3
\end{align*}
$$
$\boxed{x_1 = 29, x_2 = 16, x_3 = 3}$

**Example 2**:
$$
\begin{align*}
	x_1 - 2x_2 + x_3 &= 0\\
	2x_2 - 8x_3 &= 8\\
	5x_1 - 5x_3 &= 10
\end{align*}
$$
$$
\begin{align*}
&\begin{bmatrix}
	1 & -2 & 1 & | & 0\\
	0 & 2 & -8 & | & 8\\
	5 & 0 & -5 & | & 10
\end{bmatrix}\\
\sim&\begin{bmatrix}
	1 & -2 & 1 & | & 0\\
	0 & 1 & -4 & | & 4\\
	5 & 0 & -5 & | & 10
\end{bmatrix}\\
\sim&\begin{bmatrix}
	1 & -2 & 1 & | & 0\\
	0 & 1 & -4 & | & 4\\
	0 & 10 & -10 & | & 10
\end{bmatrix}\\
\sim&\begin{bmatrix}
	1 & -2 & 1 & | & 0\\
	0 & 1 & -4 & | & 4\\
	0 & 1 & -1 & | & 1
\end{bmatrix}\\
\sim&\begin{bmatrix}
	1 & -2 & 1 & | & 0\\
	0 & 1 & -4 & | & 4\\
	0 & 0 & 3 & | & -3 
\end{bmatrix}\\
\sim&\begin{bmatrix}
	1 & -2 & 1 & | & 0\\
	0 & 1 & -4 & | & 4\\
	0 & 0 & 1 & | & -1 
\end{bmatrix}
\end{align*}
$$
$x_3 = -1$, $x_2 - 4(-1) = 4 \Longrightarrow x_2 = 0$, $x_1 -2(0) + 1(-1) = 0 \Longrightarrow x_1 = 1$
$\boxed{x_1 = 1, x_2 = 0, x_3 = -1}$

*echelon form* vs *reduced echelon form*

**Example 3**:
$$
\begin{align*}
	x_1 - 3x_2 + 4x_3 &= -4\\
	3x_1 - 7x_2 + 7x_3 &= -8\\
	-4x_1 + 6x_2 + 2x_3 &= 4
\end{align*}
$$
$$
\begin{array}{cc}
&\begin{bmatrix}
	1 & -3 & 4 & | & -4\\
	3 & -7 & 7 & | & -8\\
	-4 & 6 & 2 & | & 4
\end{bmatrix} & R_2 - 3_1 \\
\sim &\begin{bmatrix}
	1 & -3 & 4 & | & -4\\
	0 & 2 & -5 & | & 4\\
	-4 & 6 & 2 & | & 4
\end{bmatrix} & \frac{R_2}{2}\\
\sim &\begin{bmatrix}
	1 & -3 & 4 & | & -4\\
	0 & 1 & -\frac 52 & | & 2\\
	-4 & 6 & 2 & | & 4
\end{bmatrix} & R_3 + 4R_1\\
\sim &\begin{bmatrix}
	1 & -3 & 4 & | & -4\\
	0 & 1 & -\frac 52 & | & 2\\
	0 & -6 & 18 & | & -12 
\end{bmatrix} & R_3 + 6R_2\\
\sim &\begin{bmatrix}
	1 & -3 & 4 & | & -4\\
	0 & 1 & -\frac 52 & | & 2\\
	0 & 0 & 3 & | & 0
\end{bmatrix} & \frac{R_3}{3}\\
\sim &\begin{bmatrix}
	1 & -3 & 4 & | & -4\\
	0 & 1 & -\frac 52 & | & 2\\
	0 & 0 & 1 & | & 0
\end{bmatrix}\\
\end{array}
$$
$\boxed{x_1 = 2, x_2 = 2, x_3 = 0}$

## 01-11-2023
##### Elementary Row Operations:
* Elementary row operations include the following:
	1) (Replacement) Replace one row by the sum of itself and a multiple of another row.
	2) Interchange two rows.
	3) (Scaling) Multiply all entries in a row by a nonzero constant.
 * Two matrices are called row equivalent if there is a sequence of elementary row operations that transform one matrix into the other.
 * It is important to note that row operations are reversible.
 * If the augmented matrices of two linear systems are row equivalent, then the two systems have the same solution set.
 * Two fundamental questions about a linear system are as follows:
	 1) Is the system consistent; that is, does at least one solution exist?
	 2) If a solution exists, is it the only one; that is the solution unique?

**Example 4**:
Determine  if the following system is consistent
$$
\begin{gather*}
	x_{2}-4x_{3}=8\\
	2x_{1}-3x_{2}+2x_{3}=1\\
	3x_{1}-8x_{2}+7x_{3}=1
\end{gather*}
$$
$$
\begin{bmatrix}
	0 & 1 & -4 & | & 8 \\
	2 & -3 & 2 & | & 1 \\
	5 & -8 & 7 & | & 1
\end{bmatrix}
$$
$$
\begin{bmatrix}
2 & -3 & 2 & 1 \\
0 & 1 & -4 & 8 \\
5 & -8 & 7 & 1
\end{bmatrix}
$$
$$
\begin{bmatrix}
2 & -3 & 2 & 1 \\
0 & 1 & -4 & 8 \\
0 & 0 & 0 & \frac 52
\end{bmatrix}
$$
$0 \neq \frac 52 \Longrightarrow$ system is inconsistent.

$$
\begin{gather*}
x_{1}-2x_{4}=-3\\
2x_{2}+2x_{3}=0\\
x_{3}+3x_{4}=1\\
-2x_{1}+3x_{2}+2x_{3}+x_{4}=5
\end{gather*}
$$

$$
\begin{array}{cc}
\begin{bmatrix}
1 & 0 & 0 & -2 & -3 \\
0 & 2 & 2 & 0 & 0 \\
0 & 0 & 1 & 3 & 1 \\
-2 & 3 & 2 & 1 & 5
\end{bmatrix} & \frac{R_{2}}{2} \\
\begin{bmatrix}
1 & 0 & 0 & -2 & -3 \\
0 & 1 & 1 & 0 & 0 \\
0 & 0 & 1 & 3 & 1 \\
-2 & 3 & 2 & 1 & 5
\end{bmatrix} & R_{4} = R_{4}+2R_{1}-3R_{2} \\
\begin{bmatrix}
1 & 0 & 0 & -2 & -3 \\
0 & 1 & 1 & 0 & 0 \\
0 & 0 & 1 & 3 & 1 \\
0 & 0 & -1 & -3 & -1
\end{bmatrix} & R_4 = R_4+R_{3} \\
\begin{bmatrix}
1 & 0 & 0 & -2 & -3 \\
0 & 1 & 1 & 0 & 0 \\
0 & 0 & 1 & 3 & 1 \\
0 & 0 & 0 & 0 & 0 
\end{bmatrix} & R_4 = R_4+R_{3} \\
\end{array}
$$ 
**Example**:
Determine the value of $h$ such that the matrix is the augmented matrix of a consistent linear system.
$$
\begin{bmatrix}
1 & 3 & -2 \\
-4 & h & 8
\end{bmatrix}
$$

$$
\begin{bmatrix}
1 & 3 & -2 \\
0 & h + 12 & 0
\end{bmatrix}
$$
$h + 12 = 0 \Longrightarrow \boxed{h = -12}$