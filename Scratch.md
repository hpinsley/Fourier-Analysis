# Useful Formulas #

## Euler's formula ##

$
e^{i\theta} = cos(\theta) + i sin(\theta)
$

$
sin(\theta) = \frac{e^{i\theta} - e^{-i\theta}}{2i}
$

$
cos(\theta) = \frac{e^{i\theta} + e^{-i\theta}}{2}
$

## Fourier Coefficients ##

$\hat{f}_n = C_n = \int_0^1e^{-2\pi i nt}f(t)dt$

or equivalently

$\hat{f}_n = C_n = \int_{-\frac{1}{2}}^{\frac{1}{2}}e^{-2\pi i nt}f(t)dt$

Any interval of period 1 will work.  **Note, however, if the period is not 1 the formula changes.**
In particular, if the period is T, the formula becomes

$\hat{f}_n = C_n = \frac{1}{T}\int_0^Te^{-2\pi in \left(\frac{t}{T}\right)}f(t)dt$


# Gausian Fun #

Find:
$$\int_{-\infty}^{\infty}e^{-\pi x^2}dx$$

Given that:
$$\int_{-\infty}^{\infty}e^{-x^2}dx = \sqrt{\pi}$$

Let $u = \sqrt{\pi}x$

$u^2 =\pi x^2$

$du = \sqrt{\pi}dx$

$dx = \frac{du}{\sqrt{\pi}}$


$$
\int_{-\infty}^{\infty}e^{-\pi x^2}dx =

\int_{-\infty}^{\infty}e^{-u^2}\frac{du}{\sqrt{\pi}} =

\frac{1}{\sqrt{\pi}}\int_{-\infty}^{\infty}e^{-x^2}dx = \frac{{\sqrt{\pi}}}{{\sqrt{\pi}}} = 1
$$





