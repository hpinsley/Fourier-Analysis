# Useful Formulas #

## Euler's formula ##

$
e^{i\theta} = cos(\theta) + i sin(\theta)
$

## Fourier Coefficients ##

$\hat{f}_n = C_n = \int_0^1e^{-2\pi i nt}f(t)dt$

or equivalently

$\hat{f}_n = C_n = \int_{-\frac{1}{2}}^{\frac{1}{2}}e^{-2\pi i nt}f(t)dt$

Any interval of period 1 will work.  **Note, however, if the period is not 1 the formula changes.**
In particular, if the period is T, the formula becomes

$\hat{f}_n = C_n = \frac{1}{T}\int_0^Te^{-2\pi in \left(\frac{t}{T}\right)}f(t)dt$


## Question 1 ##
Let $f(t)$ be a function of period $T = 2$ with $f(t) = t^2$
if $0 ≤ t < 2$

(a) **Find the Fourier series coefficients**, $C_n$, of $f(t)=t^2$ 
Given that the period is 2, the formula for $C_n$ is:

$C_n = \frac{1}{T}\int_0^Te^{-2\pi in \left(\frac{t}{T}\right)}f(t)dt$

$C_n = \frac{1}{2}\int_0^2e^{-2\pi in \left(\frac{t}{2}\right)}t^2dt$

$C_n = \frac{1}{2}\int_0^2e^{-\pi in t}t^2dt$

We will solve this by integration by parts.

Let:
 - $u = t^2$
 - $du = 2tdt$
 - $dv = e^{-\pi in t}dt$
 - $v = {\frac{-1}{\pi i n}}e^{-\pi in t}$

Then this becomes:

$
C_n = \frac{1}{2} \left( {
\left[t^2 \cdot {\frac{-1}{\pi i n}}e^{-\pi i n t} \right]_0^2 - 
\int_0^2{{\frac{-1}{\pi i n}}e^{-\pi i n t} 2t dt}
}
\right )
$

Simplifying we get:

$ C_n = \frac{1}{2} \left( {
{\frac{-4}{\pi i n}}e^{-2\pi i n}  + 2 
\int_0^2{{\frac{1}{\pi i n}}e^{-\pi i n t} t dt}
}
\right )
$

Note that $e^{-2\pi n} = 1$ for integer n by Euler's formula leaving

$
C_n = \frac{1}{2} \left( {
{\frac{-4}{\pi i n}} + \frac{2}{\pi i n} 
\int_0^2{t e^{-\pi i n t} dt}
}
\right )
$

Integration by parts again:

Let:
 - $u = t$
 - $du = dt$
 - $dv = e^{-\pi in t}dt$
 - $v = {\frac{-1}{\pi i n}}e^{-\pi in t}$

C_n = $\frac{1}{2} \left( {
{\frac{-4}{\pi i n}} + \frac{2}{\pi i n} 
\left(
    \left[
        t
        {\frac{-1}{\pi i n}}e^{-\pi in t}
        \right]_0^2 
    - \int_0^2 {\frac{-1}{\pi i n}}e^{-\pi in t}dt
\right)
}
\right )
$

First evaluating the square brackets

$
C_n = \frac{1}{2} \left( {
{\frac{-4}{\pi i n}} + \frac{2}{\pi i n} 
\left(
    {\frac{-2}{\pi i n}}e^{-2\pi in}
    - \int_0^2 {\frac{-1}{\pi i n}}e^{-\pi in t}dt
\right)
}
\right )
$

Note that by Euler's formula:

$
e^{i\theta} = cos(\theta) + i sin(\theta)
$

Here $\theta$ is $-2\pi n$, therefore:

$
e^{-2\pi in} = cos(-2\pi n) + i sin(-2\pi n)
$

Since n is an integer, the angle is 0 and this evaluates to 1 and we can simplify to:

$
C_n = \frac{1}{2} \left( {
{\frac{-4}{\pi i n}} + \frac{2}{\pi i n} 
\left(
    {\frac{-2}{\pi i n}}
    - 
    \int_0^2 {\frac{-1}{\pi i n}}e^{-\pi in t}dt
\right)
}
\right )
$

The final integral can be evaluated directly leaving:

$
C_n = \frac{1}{2} \left( {
{\frac{-4}{\pi i n}} + \frac{2}{\pi i n} 
\left(
    {\frac{-2}{\pi i n}}       
    - 
    \left[
        \frac{-1}{\pi^2n^2}e^{-\pi i n t}
    \right]_0^2
\right)
}
\right )
$

The evaluation of the integral from 0 to 2 here is zero.

C_n = $
\frac{1}{2} \left( {
{\frac{-4}{\pi i n}} + \frac{2}{\pi i n} 
\left(
    {\frac{-2}{\pi i n}}       
\right)
}
\right )
$

C_n = $
\frac{1}{2} \left( {
{\frac{-4}{\pi i n}} + \frac{4}{\pi^2 n^2} 
}
\right )
$

Normalizing the complex number:

C_n = $
\frac{1}{2} \left( {
{\frac{4i}{\pi n}} + \frac{4}{\pi^2 n^2} 
}
\right )
$

Diving through

$
C_n = \left( {
{\frac{2i}{\pi n}} + \frac{2}{\pi^2 n^2} 
}
\right )
$

$
C_n = \left( {
{\frac{2i \pi n}{\pi^2 n^2}} + \frac{2}{\pi^2 n^2} 
}
\right )
$

$
C_n = \left( {
{\frac{2i \pi n + 2}{\pi^2 n^2}} 
}
\right )
$

$
C_n = {\frac{2\left(i \pi n + 1\right)}{\pi^2 n^2}} 
$

$
C_n = {\frac{2\left(1 + i \pi n \right)}{\pi^2 n^2}} 
$

Note the problem for $C_0$.  However, this is the $C_0$ is the average value of the function on the interval.  That is:

$
f_{avg} = \frac{1}{T}\int_{Interval\space T} f(t)dt
$

Given that $T = 2$

$
C_0  =\frac{1}{2} \int_0^2 t^2dt
$

$
C_0  =\frac{1}{2} 
\left[
    \frac{1}{3} t^3
\right]_0^2
$

$
C_0  =\frac{1}{2} 
\left[
    \frac{1}{3} t^3
\right]_0^2
$

$
C_0  =\frac{4}{3}
$

Therefore, the final fourier series is given by:

$
f(t) = \frac{4}{3} + \sum_{n=1}^\infty
\frac{2\left(1 + i \pi n \right)}{\pi^2 n^2}e^{2\pi i n t}
$

$
f(t) = \frac{4}{3} + \sum_{n=1}^\infty
\frac{2\left(1 + i \pi n \right)}{\pi^2 n^2}\left(\cos(2\pi n t) + i \sin(2\pi n t) \right)
$

$
f(t) = \frac{4}{3} + \frac{2}{\pi^2}\sum_{n=1}^\infty
\frac{\left(1 + i \pi n \right)}{n^2}\left(\cos(2\pi n t) + i \sin(2\pi n t) \right)
$

$
f(t) = \frac{4}{3} + \frac{2}{\pi^2}\sum_{n=1}^\infty
{\left(\frac{1}{n^2} + \frac{\pi}{n}i\right)}\left(\cos(2\pi n t) + i \sin(2\pi n t) \right)
$

Let's multiply out the terms and separate the real from the imaginary parts.

$$
f(t) = \frac{4}{3} + \frac{2}{\pi^2}\sum_{n=1}^\infty
\left[
\left(\frac{cos(2\pi n t)}{n^2}
- \frac{\pi sin(2\pi n t)}{n}\right)
+
\left(
\frac{sin(2\pi n t)}{n}
+
\frac{\pi cos(2\pi n t)}{n2}
\right)
i
\right]
$$

