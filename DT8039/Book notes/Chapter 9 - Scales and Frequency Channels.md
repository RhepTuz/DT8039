- Blurring a function by a linear filter is equivalent to suppressing high-frequency components of its spectrum.
- Having void information at high frequencies suggests in turn that there might be a redundancy in the representation which can be avoided.
	- This observation can be utilized in several ways:
		- The amount of data representing an image can be reduced, e.g., image compression
		- The image can be efficiently filtered to contain only certain frequency components, e.g., recognition of image contents.
		- The image can be resized, e.g., user interfaces and animation


# 9.1 Spectral effects of Down- and Up-Sampling



- Both up- and down-sampling can be achieved via contiuous reconstruction as follows:
	- Confine $F$ to the basic period around the origin. This operation has the purpose to hinder $F$ from being periodic if $F$ is not periodic but limited, then $f$ is continuous. This is achieved by mulitplying $F$ with a suitable characteristic function, $\mathcal{X}_\mathcal{D}(\omega)$. Such a multiplication is equivalent to a convolution in the spatial domain, leading to a reconstruction of the continuous signal from its sampled signals: $$f(t) \sum_m{f(t_m)\mu_0(t-t_m)} \tag{9.1}$$where $\mu_0 = \mathcal{F}^-1(\mathcal{X}_\mathcal{D})$.
	- Resample the continuous signal at the desired rate, which at all circumstances should be done with a finer step size than what the highest frequency of the signal content allows (Nyquist theorem). Effectivaly, this sampling of Eq. (9.1) amounts to, sampling the interpolation function at the desired points. The equation itself becomes an ordinary discrete scalar product between the filter samples and the old function samples, $f(t_m)$: $$f(t'_n)=\sum_m{f(t_m)\mu_0(t'_n-t_m)}\tag{9.3}$$

## Down-sampling 

- We want to down-sample a given signal $f(mT_0)$ with an integer factor of $\mathcal{K}$ by destroying destroying as little information as possible. To do this, we follow the procedure above:
	- We reconstruct the continuous signal $f(t)$ and obtain $$f(t)=\sum_mf(mT_0)\mu_0(t-mT_0)$$where $\mu_0$ is the interpolation function, the effective width of which is inversely proportional to $\Omega_0$. The highest frequency content of the signal is $\frac{\Omega}{2}$ and the grid is a regular grid given by $t_m = mT_0$ where $T_0 = \frac{2\pi}{\Omega_0}$. 
	- 