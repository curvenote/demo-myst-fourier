# Fourier Series are Beautiful

+++ { "part": "abstract" }
Fourier series are powerful function and signal representation, capable of representing
any periodic bandlimited signal. Understanding the representation can be tricky, but is
greatly helped by visualising individual components of the series, which is what we'll do
here.

+++

## The Fourier Series

Citing <a href="https://en.wikipedia.org/wiki/Fourier_series">Wikipedia</a>: A Fourier
series is a periodic function composed of harmonically related sinusoids comined by a
weighted summation. With appropriate weights, one cycle (or period) of the summation can
be made to approximate as arbitrary function in that interval, or the entire function if
it itself is periodic.

The fourier series representation of a function (Exponential Form) is given by:

$$x_{T}(t)=\sum_{n=-\infty}^{\infty} c_{n} e^{j n \omega_{0} t}$$

Where:

- $\omega_{0}$ is the fundamental frequency
- $n$ is an integer representing the harmonics of $\omega_{0}$
- $c_n$ are the coefficients of the infinite series

## Approximating Functions with Fourier Series

Any periodic bandlimited function can be approximated by a Fourier Series expansion. Explore some of these using the playground below.

## Square Waves

Let's start with an informative example - representing a Square Wave by it's fourier
series, this is an interesting example, as how can smooth sinusoids approximate a function
containing discrete steps?

The coefficients of the fourier series for the square wave are given by the following
expression, each coefficient $c_n$ determining the contribution of a sinusoid at the given
frequency $n\omega_{0}$.

$$c_n = \frac{A}{\pi n} \sin \left(n \omega_{0} \frac{T_{p}}{2}\right)$$

## The Composite Signal

Given the value of $\omega_{0}$ is X, $T_p$ is X and $A$ is Y the first ($N$) will produce a function approximating the square as shown below.

So it turns out that we need quite a lot of components to approximate the square wave well, try setting the current value of $N=$ X to the maximum of 100. The number of components has a significant impact of the final signal and we would need the full infiite series in order to converge to a true square wave with instantaneous value changes.

The parameter $A$ controls amplitude and has no influence on the structure of the approximation, try changing it to see, A: X.

The parameters $\omega_{0}$ (X) and $T_p$ (X) have the greatest influence on the waveform shape, controlling the periodicity, duty cycle and rate convergence of the representation to the target waveform. try adjustuing these in tandem so see how the waveform is affected.

```{figure} #fig-fourier-playground
:placeholder: playground.png
```
