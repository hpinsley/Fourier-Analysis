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

$$C_n = \frac{-1}{2\pi in}\left[e^{-\pi in}-e^{\pi in}\right]$$

If you multiply the **-1** through you get:

$$C_n = \frac{1}{2\pi in}\left[e^{\pi in}-e^{-\pi in}\right]$$

Regrouping terms, it becomes:

$$C_n = \frac{1}{2\pi in}\left[e^{\pi in}-e^{-\pi in}\right]$$

$$C_n = \frac{1}{\pi n}\left[\frac{e^{\pi in}-e^{-\pi in}}{2i} \right]$$

And by trigonometric identity this is:

$$C_n = \frac{1}{\pi n}\left[sin(\pi n) \right]$$

$$C_n = \frac{sin(\pi n)}{\pi n}$$

Why isn't this always zero??  The notes do not do an example of a do this with a Fourier series but instead use a Fourier transform.  And there too, they run into an issue that is solved by scaling?  This looks a lot like the **sinc** function...




