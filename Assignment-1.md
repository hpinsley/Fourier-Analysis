# This is Math #

$$ \int_0^1 x^2 dx = \frac{1}{3} $$

$$\hat{f}_n = C_n = \int_0^1e^{-2\pi i nt}f(t)dt$$
or equivalently
$$\hat{f}_n = C_n = \int_{-\frac{1}{2}}^{\frac{1}{2}}e^{-2\pi i nt}f(t)dt$$
Any interval of period 1 will work.  Note, however, if the period is not 1 the formula changes.
In particular, if the period is T, the formula becomes

$$\hat{f}_n = C_n = \frac{1}{T}\int_0^Te^{-2\pi in \left(\frac{1}{t}\right)}f(t)dt$$


# Rectangle Function #

The rectangle function has height 1 and width one and is centered at $y=0$.
Its definition is:

$x = 1$ when $|x|<\frac{1}{2}$
$x = 0$ when $|x|>=\frac{1}{2}$, so

$$
C_n = \int_{-\frac{1}{2}}^{\frac{1}{2}}e^{-2\pi i nt}\cdot 1dt
$$

This can be integrated directly
$$C_n = \left[\frac{-1}{2\pi in} e^{-2\pi int}\right]_{-\frac{1}{2}}^\frac{1}{2}$$

$$C_n = \frac{-1}{2\pi in}\left[e^{-2\pi int}\right]_{-\frac{1}{2}}^\frac{1}{2}$$
$$C_n = \frac{-1}{2\pi in}\left[e^{-2\pi in\frac{1}{2}} \me^{-2\pi in \frac{1}{2}} \right]$$
