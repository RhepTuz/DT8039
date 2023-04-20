- "Just as a vecor in $E_3$ can be expressed as a weighted sum of three orthogonal vectors, so can functions defined on a continuous space be expressed as a weighted sum of orthogonal basis functions with some coefficients."
	- An example of this is images on photographic papers or film. By layering each color upon eachother, a new complete image is created.


# 4.1 Functions as a Vector space

- Continuous functions are quantities that are studied in the framework of vector spaces.

- A major difference between arrays and the function spaces is that function spaces are abstract quantites that are continuous. 
	- An example of a continuous function defined on an ordinary plane is a a photograph. In that sense it is called a continuous image.
	- Its descrete version, a digital image, is defined on a set of points of the same 2D plane. 
	- The continuous photgraph can assume many more values because it is defined even between the set of points where the discrete image is undefined.

- In the case of $E_3$, we need get used to the idea that a function, e.g., $f(t)$, is a point in the function space. 
	- Image that the entire graph is a point among its likes in a function space.
	- When one hase a unique rule (a function), then one has a unique point (in a vector space of functions) that corresponds to taht function.


# 4.2 Addition and Scaling in Vector Spaces of Functions

- How to obtain a new "point" (function) by the rule scaling? *Function scaling*
	- This will yield a different function (rule) than the one we started with.
	- Since we are looking for a rule, we have to define it as such and assign a new function symbol to it, $g$: $$g=\alpha f$$
	- We know $g$ if we know a rule how to obtain its value when an argument is passed to it.
	- We know the rule for $f$, (this is $f(t)$), the rule to obtain the value of $g$ can be simply defined as to multiply the function value of $f$ at $t$ with the scalar $\alpha$: $$ g(t) = \alpha f(t)$$
- We also need a way to add two vectors in the function spaces. For this we use *function addition*.
	- *Function addition* is defined in a similar fashion: The new rule $h$, $$ h = f + g $$ is obtained by using the already known rules regarding $f$ and $g$: $$ h(t) = f(t)+g(t)$$

# 4.3 A scalar product for vector spaces of functions

- The scalar product of functions: $$ \langle f,g \rangle = \int{f^*g}$$
- 