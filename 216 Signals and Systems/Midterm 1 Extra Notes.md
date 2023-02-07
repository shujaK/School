$$\text{Shuja Khwaja}$$
## Period 
$T=\frac{2\pi}{\omega _{0}}$
$\omega_{0}=2\pi f_{0}=\frac{2\pi}{T_{0}}$
## Periodicity of Multiple Signals
$\frac{T_{1}}{T_{2}} = \frac{k}{l} \:\: where \:\: k,l\: \in \mathbb{Z}$

$T_{0} = LCM(T_{1}, T_{2}, ...)$
$LCM(\frac{a_1}{b_1}, \frac{a_2}{b_2}, ..., \frac{a_n}{b_n}) = \frac{LCM(a_1, a_2, ..., a_n)}{GCD(b_1, b_2, ..., b_n)}$

## Support
- Smallest closed set where signal is non-zero,
- Include boundaries and ignore simple intersections
$supp(x) = [0,1] \cup[2,\infty)$

## Even and Odd
$x_{even}(t) = \frac{1}{2}(x(t)+x(-t))$
$x_{odd}(t) = \frac{1}{2}(x(t)-x(-t))$

## Special Signals
 **Unit Step**: CT ≈ DT

$$u(t)=\left\{\begin{matrix}1 \:\;t\geq 0
\\ 0 \:\;t< 0
\end{matrix}\right.$$

**Impulse**: CT is derived from integral
$$\delta[n]=\left\{\begin{matrix}1 \:\;n= 0
\\ 0 \:\;t\neq 0
\end{matrix}\right.$$
**Sifting**:
$x(t)\delta(t-t_{0})=x(t_{0})\delta(t-t_{0})$
$\therefore \int_{-\infty}^{\infty}x(t)\delta(t-t_{0})\; dt=x(t_{0})$

## Sinusoids
$\omega_{0}=2\pi f_{0}=\frac{2\pi}{N_{0}}$
DT: $e^{jwn}$ is periodic $N_{0}$ if $\omega$ is an integer multiple of $\frac{2\pi}{N}$

**Frequency Periodicity**:
$e^{j\omega n} = e^{j\omega n+2\pi}$
$e^{j\pi n}= (-1)^n$

**Theorem 2.3**:
$$\text{Let}\; N_{0} \in \mathbb{Z}_{\geq1} \;\text{be a desired period. There are exactly}\; N_{0} \;\text{distinct DT} \newline \text{complex exponential signals of period} N_{0} \; \text{given by}$$
$$\phi _{k}[n]=e^{jk\omega _{0}n}, \;\;\;\;k\in \begin{Bmatrix}
0,1,...,N_{0}-1
\end{Bmatrix}$$

## CT Fourier Series
**Existence**:
$$\text{If}\ x\ \text{has finite action,}\ x\in L_{1}^{per}\newline \text{then}\ \alpha _{k}\ \text{are well defined and}\newline \lim_{k\to \pm \infty} |\alpha _k| = 0
$$

**Convergence**:
$$\text{Let}\ e_k = \hat{x}_k - x \ \text{be the error of approximation of } x \ \newline \hat{x}\ \text{converges to} \ x\ \newline
\text{i. pointwise if} \ \lim_{k \to \infty} e_k(t_0) = 0,\; t_0 \ \text{is the point of interest} \newline
\text{ii. uniformly if}\lim_{k \to \infty} ||e_k||_{\infty} = 0,\;\; \text{amplitude of error goes to 0}\newline
\text{iii. in energy if}\lim_{k \to \infty} ||e_k||_{2} = 0,\;\; \text{energy of error goes to 0}
$$

i. if $x$ has finite action and $\frac{d}{dt}x$ is cont. at $t_o$, then $\hat{x}$ converges to $x$
	OR if there is is a finite discontinuity (left and right limits exist) $\hat{x}$ converges to the midpoint of the discontinuities, *Gibbs Phenomenon*

ii. if $x$ has finite action and $\frac{d}{dt}x$ is cont. everywhere, then $\hat{x}$ converges to $x$ uniformly

iii. if $x$ has finite energy, $x \in L_2^{per}$
1. 	$\hat{x}$ converges to $x$ in energy
2. 	$\begin{Bmatrix}\alpha _k \end{Bmatrix}$ have finite energy, $\alpha \in l_2^{per}$
3. 	the signal and coefficients satisfy *Parsevals Relation*: 
$$\frac{1}{T_0}||x||_2^2 = ||\alpha||_2^2$$
$$\frac{1}{T_0} \int _0 ^ {T_0} |x(t)|^2\ dt = \sum^\infty _{k=-\infty} |\alpha _k|^2\newline \text{energy of}\ x\ = \text{energy of} \ \alpha _k\newline \ \text{scaled by period}\$$
