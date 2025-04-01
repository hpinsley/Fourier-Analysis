# Useful Formulas #

## Euler's formula ##

$$
e^{i\theta} = cos(\theta) + i sin(\theta)
$$

## Fourier Coefficients ##

$$\hat{f}_n = C_n = \int_0^1e^{-2\pi i nt}f(t)dt$$
or equivalently
$$\hat{f}_n = C_n = \int_{-\frac{1}{2}}^{\frac{1}{2}}e^{-2\pi i nt}f(t)dt$$
Any interval of period 1 will work.  **Note, however, if the period is not 1 the formula changes.**
In particular, if the period is T, the formula becomes

$$\hat{f}_n = C_n = \frac{1}{T}\int_0^Te^{-2\pi in \left(\frac{1}{t}\right)}f(t)dt$$


## Question 1 ##
Let $f(t)$ be a function of period $T = 2$ with $f(t) = t^2$
if $0 ≤ t < 2$

(a) Find the Fourier series coefficients, $C_n$, of $f(t)$.

Given that the period is 2, the formula for $C_n$ is:

$$C_n = \frac{1}{T}\int_0^Te^{-2\pi in \left(\frac{t}{T}\right)}f(t)dt$$

$$C_n = \frac{1}{2}\int_0^2e^{-2\pi in \left(\frac{t}{2}\right)}t^2dt$$

$$C_n = \frac{1}{2}\int_0^2e^{-\pi in t}t^2dt$$

We will solve this by integratoin by parts.

Let:
 - $u = t^2$
 - $du = 2tdt$
 - $dv = e^{-\pi in t}$
 - $v = {\frac{-1}{\pi n t}}e^{-\pi in t}$

Then this becomes:

$$
\frac{1}{2} \cdot \left( {
\left[t^2 \cdot {\frac{-1}{\pi n t}}e^{-\pi in t} \right]_0^2 - 
\int_0^2{{\frac{-1}{\pi n t}}e^{-\pi in t} \cdot 2t dt}
}
\right )

$$

