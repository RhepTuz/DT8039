# 6.1 The Fourier Transform

- If $f$ is not a finite extension signal, we still would like to express it in terms of the complex exponentials basis via the synthesis Eq. (5.14), and the analysis Eq. (5.13). 
	- To allow this, we will express a part of such a funciton in a finite interval and then let this interval grow beyond all bounds. 
		- We start with the finite interval $[-T/2,T/2]$, and then let $T$ go to infinity.
	- Outside of $[-T/2,T/2]$, the synthesis delivers a repeated version of the synthesized function inside the interval.

	- $f_T =$ the function restricted to the finite interval
	- $$f = \lim_{T\rightarrow \infty}f_T$$
	- ![[Pasted image 20230425081227.png]]


- **Theorem 6.1 (FT).** Provided that the integral exist, the integral transform pair: 
	- Forward FT $$\mathcal{F}(f)(\omega)=F(\omega) =\frac{1}{2\pi}\int_{-\infty}^{\infty}{f(t)exp(-i\omega t)dt \tag{6.8}}$$
	- Inverse FT $$\mathcal{F}^{-1}(F)(\omega)=f(t) =\frac{1}{2\pi}\int_{-\infty}^{\infty}{F(\omega)exp(i\omega t)d\omega \tag{6.8}}$$Defines the Fourier transform (FT) and the Inverse Fourier transform, which relate a pair of complex-valued functions $f(t)$ and $F(\omega)$, both defined on the domain of the real axis. The function $F$ is called the Fourier Transform of the function $f$.

- **Lemma 6.1 Symmetry of FT).** If $$(f(t),F(\omega))$$is an FT pair, so is $$(F(\omega),f(-t))$$The conclusions and principles established assuming the forward direction is also valid in the inversr direction.

- **Theorem 6.2 (FC 2).** *There exists a set of scalars $f(t_m)$ that can synthesize a function $F(\omega)$ having the finite extension of $\Omega$,$$F(\omega)=\frac{1}{\Omega}\sum_m f(t_m)exp(-it_m \omega) \tag{6.12}$$where $$f(t_m)=\int^{\frac{\Omega}{2}}_{-\frac{\Omega}{2}}F(\omega)exp(it_m \omega) \tag{6.13}$$using $t_m=m \frac{2\pi}{\Omega}$*


# 6.2 Sampled Functions and the Fourier Transform

- Via theorem 5.2 it is established that there exists a unique set of values capable of reconstructing any $f(t)$ by means of complex exponentials, provided that $f$ has an extension $T$ that is finite.
- 