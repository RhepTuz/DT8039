- The difference $\pmb{u}-\pmb{v}$ is a vector if both vectors belong to the same vector space.
- The distance between $\pmb{u}$ and $\pmb{v}$ is defined as $||\pmb{u}-\pmb{v}||$

- There are two other properties that a norm must have before it can properly be called a norm:
	- When a vector is scaled by a scalar, its norm must scale with the magnitude of the scalar.
	- The vector space must yield the triangle inequality under the norm, i.e., the shortest distance between two points is the norm of the vector joining them.

- Summarized *norm properties*:
	- Nonnegativity: $0 \le ||\pmb{u}||$
	- Nullness: $||\pmb{u}|| = 0\leftrightarrow ||\pmb{u}|| =0$ 0
	- Scaling: $||\alpha\pmb{u}|| = |\alpha|||\pmb{u}||$
	- Triangle inequality: $||\pmb{u}+\pmb{v}|| \le ||\pmb{u}||+||\pmb{v}||$


## 3.4 Scalar products
- The *scalar product* is used to measure the "angles" between vectors in vector spaces.

- To be called a scalar product, the operator must obey the scalar prouct rules:
	- $\langle \pmb{u} , \pmb{v}\rangle = \langle\pmb{v,u}\rangle^*$ 
	- $\langle \alpha\pmb{u} , \pmb{v}\rangle = \alpha^*\langle\pmb{u,v}\rangle$
	- $\langle \pmb{u+v} , \pmb{z}\rangle = \langle\pmb{u,z}\rangle + \langle\pmb{v,z}\rangle$
	- $\langle \pmb{u} , \pmb{u}\rangle > 0$ if $\pmb{u}\ne 0$ and $\langle\pmb{u,u}\rangle = 0$ iff $\pmb{u} = 0$

- The last relationship offers a natural way of producing a norm for a vector spac having a scalar product:
	- $||\pmb{u}|| = \sqrt{\langle \pmb{u,u}\rangle}$ 
- This can in turn be used to express the distance of two vectors with scalar products:
	- $||\pmb{u - v}||^2 = \langle \pmb{u - v}, \pmb{u - v}\rangle$


- **Definition 3.2.** *A vector space which has a scalar prodcut defined in itslef is called a Hilbert Space*

- **Lemma 3.1.** A scalar product for vectors $\pmb{u,v} \in C_N$, i.e., vectors with complex elements having the same finite dimension, yields: $$\langle \pmb{u,v} \rangle = \sum_{i} \pmb{u}(i)^*\pmb{v}(i)$$
	- Where $^*$ is the complex conjugate and $\pmb{u}(i),\pmb{v}(i)$ are the elements of $\pmb{u},\pmb{v}$.
	- This is the dot product between two vectors.


## 3.5 Orthogonal Expansion

- **Definition 3.3.** Two vectors are orthogonal if their scalar product vanishes. $$\langle\pmb{u,v}\rangle=0$$

- How do we find the coordinates of a point $\pmb{x}$ if we have three orthogonal vectors $\pmb{e}_1,\pmb{e}_2,\pmb{e}_3$ that we use as a basis?
	- We use the *projection* operation.
	- The operator measures the "orthogonal shadow" of the vector representing the point on the three basis vectors.
	- Mathematically, we write the vector $\pmb{x}$ as if we knew its coordinates or coefficients, $c_1,c_2,$ and $c_3$ in the basis $\{\pmb{e_i}\}$ 