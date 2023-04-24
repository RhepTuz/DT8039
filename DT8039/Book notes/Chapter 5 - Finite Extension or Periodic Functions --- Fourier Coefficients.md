
This section will make use of Hilbert spaces being a vector space in which a scalar product is defined.

# 5.1 The Finite Extension Functions Versus Periodic Functions

- We define the *finite extension functions* and the *periodic functions* as follows: 
	- **Definition 5.1.** A function $f$ is a finite extension FE function if there exisits a finite real constant $T$ such that $$t\notin [-\frac{T}{2},\frac{T}{2}] \implies f(t) = 0$$
	- A function $f$ is a periodic function if there is a positive constant $T$, called a period, such that $f(x) = f(x+nT)$ for all integers $n$.

- Some examples of finite extension signals are:
	- A sound recording in which there is a time when the sugnal starts and another when it stops.
	- A video recording which has, additionally a space limitation representing the screen size.
	- An (analog) photograph, which has a boundary outside of which there is no image.

- A periodic signal is a signal that repeats copies of itself in a basic interval that is given by a fixed interval $T$. 

- A periodic and a FE signal are two sides of a coin. One could cut up a periodic signal to make an FE signal and one could patch together an FE signal to make a periodic signal.

- The arguments of periodic functions are often measured in angles. This can be achieved by stretching or shinking the argument of the periodic function $f(t)$ to yield $t' = \frac{2\pi}{T}t$. 
	- Using $\omega_1 = \frac{2\pi}{T}$, $t'$ can be rewritten to $t' = \omega_1t$
	- This makes it so that $t'$ obtains values in $[0,2\pi]$ when $t$ is assigned values in $[0,T]$.

- **Theorem 5.1.** The space of periodic function that share tha same period is a hilbert space with the scalar product: $$\langle f,g \rangle = \int^\frac{T}{2}_\frac{-T}{2} f^*g $$


# 5.2 Fourier Coefficients (FC)

- Since there exists many different types of orthogonal functions that are periodic, one speaks of *orthogonal function families*.
	- One very useful familiy is the *complex exponentials:* $$\psi_m(t) = exp(i\omega_mt)$$ where $$\omega_m=m\frac{2\pi}{T}\text{ and, } m=0, \pm1, \pm2, \pm3,\cdots $$
	- For each $\omega_m$, we have a different member of the same family. The function family is then: $$ \{\psi_m\}_m = \{\cdots, e^{-i2\omega_1t},e^{-i2\omega_2t},e^{-i2\omega_3t},\cdots\}$$
	- This is also called the *Fourier basis*, because the set acts as a basis for function spaces and defines the Fourier transform.

- Since complex expinentials are orthogonal and we know their norms, any function $f$ that has a limited extension $T$ can be reconstructed by by means of them as: $$ f(t) = \sum_m c_m exp(i\omega_mt)$$ where $c_m$ are complex-valued scalars.
- $$c_n = \frac{1}{T}\int^\frac{T}{2}_\frac{-T}{2} f(t)exp(-i\omega_nt)dt$$ $c_n$ are the *projection coeffiecients* of f on the Fourier basis
	- They are known as the *Fourier coefficients (FCs)*.

- **Theorem 5.2 (FC 1)**. There exisis a set of scalars $F(\omega_m)$ which can syntheize a function $f(t)$ having the finite extension $T$, $$ F(\omega_m) = \frac{1}{2\pi}\int^\frac{T}{2}_\frac{-T}{2}f(t)exp(-i\omega_mt) dt \text{ (Analysis)} \tag{5.13}$$ such that $$ f(t) = \frac{2\pi}{T}\sum_mF(\omega_m)exp(i\omega_mt)\text{ (Synthesis)} \tag{5.14}$$ using $\omega_m = m\frac{2\pi}{T}$ and $m = 0, \pm1, \pm2, \pm3, \cdots$.



# 5.3 (Parseval-Plancherel) Conservation of the scalar product

- We consider a scalar product between two members of our Hilbert space of periodic functions, $f=\frac{2\pi}{T} \sum_m F(\omega_m)\psi_m$ and $g = \frac{2\pi}{T} \sum_m G(\omega_m)\psi_m$: $$\langle f,g \rangle = \frac{(2\pi)^2}{T}\sum F^*(\omega_m)G(\omega_m)$$
	- To obtain the above eq. the order of summation and integration (of the scalar product) is changed. This is allowed for all functions $f$ and $g$ that are physically realizable.

- The set of the discrete Fourier coefficients $$ \{F(\omega_m)\}_m = (\cdots F(\omega_{-2}),F(\omega_{-1}),F(\omega_{0}),F(\omega_{1}),F(\omega_{2}),\cdots)$$

- **Theorem 5.3 (Parseval-Plancherel FC).** The scalar products are conserved under the FC transform $$ \langle f, g \rangle = \frac{(2\pi)^2}{T} \langle \{F(\omega_m)\}_m, \{G(\omega_n)\}_n \rangle$$ As a special case, we obtain the conservation of the norms (Energies). $$ \|f\|^2 = \frac{(2\pi)^2}{T} \sum_m|F(\omega_m)|^2 = \frac{(2\pi)^2}{T}\|\{F(\omega_m)\}_m\|^2$$
- It can be shown that the function series Eq. (5.14) always converges for the functions $f$ that we are interested in (physically realizable functions that have finite extension) so that the sum on the right side always produces the function value on the left side at all points $t$ (*strong convergence,* or *pointwise convergence*).
	- This fact implies that the Fourier coefficients constitue a decreasing sequence: $$ \lim_{m\rightarrow \infty} F(\omega_m)=0$$ This allows one to truncate the sum in Eq. (5.14) after a finite number of terms without much harm to the original signal.
		- This trick is often used in image enhancement or image compression, since the high-index Fourier coefficients correspond to complex exponentials (sinusoids) with high spactial frequencies that are likey to be noise.


# 5.4 Hermitian Symmetry of the Fourier Coeffients

- The Fourier series equations in Eqs. (5.13) and Eq. (5.14) are also valid for function $f$ that are complex-valued, since our scalar product can cope with complex functions from the beginning.
- The signals of the real world are real yet the Fourier coefficients of real signals as well as complex signals are complex-valued.
	- Since there is so much more information in a complex signal than in a real signal, there must be some redundancy in the Fourier coefficients of the real signal.

- A real signal is the complex conjugate of itself since the imaginary part is zero, $$f=f^*$$The Fourier series reconstruction of the signal $f$ yields $$f(t) =\sum_mF(\omega_m)exp(im\omega_1t)$$so that its complex conjugate becomes $$f(t)^* =\sum_mF^*(\omega_m)exp(-im\omega_1t)$$Replacing the index $m$ with $-m$, we obtain $$f(t)^* =\sum_{m=\infty}^{-\infty}F^*(\omega_{-m})exp(im\omega_1t)$$In doing so, the order of summation is reversed, i.e., $m$ runs now from postive to negative integers. Summing in one direction or the other does not change the total sum, so we are allowed to reverse the direction of the summation back to the conventional direction: $$f(t)^* =\sum_{m=-\infty}^\infty F(\omega_{-m})exp(im\omega_1t)$$Accordingly, the Fourier coefficients of $f^*$ will fulfill $$f^* = \{F^*(\omega_m)\}_m$$Now using $f=f^*$ from earlier yields $f=f^*$ to the effect that $$F(\omega_m) = F^*(\omega_{-m})$$
	- This property of the FCs, which is only valid for real functions $f$, is called *Hermitian symmetry*. 
	- Because of this, the Fourier coefficients of a real signal contains redundancy.
	- If we know a coefficient, say $F(\omega_{17}) = 0.5 + i0.3$, then the mirroered coefficient is locked to its conjugate, i.e., $F(\omega_{-17}) = 0.5-i0.3$. 
- **Theorem 5.4.** The Fourier coefficients of a real signal have Hermitian symmetry: $$F(\omega_m)=F^*(\omega_{-m})$$so that the real and imaginary parts of their FCs are even and odd, respectively, whereas their magnitudes are even.
