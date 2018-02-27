# Deep Learning on Raspberry Pi

## Session 01

Welcome to the first session of the course ['Deep Learning on Raspberry Pi'](../README.md).

In this session, we will first setup the Raspberry Pi computing platform. And then after a small introduction to the scripting language Python, we will revisit a few basic concepts of linear algebra, while also familiarizing ourselves with Numpy, a Python package used for scientific computing. Then we will familiarize ourselves with a few basic concepts of symbolic computation. At the end of this session, there will be a few exercises which will further help understanding the concepts introduced.

In this session, we will revisit the basic concepts of linear algebra. Then, after a small introduction to the scripting language Python, we will familiarize ourselves with Numpy, a Python package used for scientific computing. Then we will familiarize ourselves with a few basics of symbolic computation. At the end of this session, there will be a few exercises which will further help understanding the concepts introduced.

### Setting up Raspberry Pi


### Brief Introduction to Python



### Linear Algebra

This section will only provide a brief introduction to linear algebra. For those of you unfamiliar with the concepts of linear algebra, it is strongly recommended that you spend some time with a text book or a complete course on linear algebra. A strongly recommended text book would be [Introduction to Linear Algbera](math.mit.edu/~gs/linearalgebra/) by Gilbert Strang.

Those of you who are well familiar with linear algebra may skip the following two sub sections, where we formally define the concept of a vector space and an inner product space.

#### Vector Space
A vector space $V$, over the set of real numbers $\mathbb{R}$, is a set equipped with two operations, addition `+` and multiplication `.`, subject to the conditions,
1. The set is closed under the addition operator, i.e. for any $\vec{l}, \vec{m} \in V$, $\vec{l} + \vec{m} \in V$.
2. The addition operation is commutative, i.e. for any $\vec{l}, \vec{l} \in V$, $\vec{l} + \vec{m} = \vec{m} + \vec{l}$.
3. The addition operation is associative, i.e. for any $\vec{l}, \vec{m}, \vec{n} \in V$, $(\vec{l} + \vec{m}) + \vec{n} = \vec{l} + (\vec{m} + \vec{n})$.
4. There exists a zero vector $\vec{0} \in V$, which is the identity element of addition, i.e. for any $\vec{l} \in V$, $\vec{l} + \vec{0} = \vec{l}$.
5. There should exist an inverse for every element in the set, i.e. for any $\vec{l} \in V$, there exists a $\vec{m} \in V$ such that $\vec{l} + \vec{m} = \vec{0}$.
6. The set is closed under the multiplication operation with any real valued scalar, i.e. for any $\vec{l} \in V$ and $r\in \mathbb{R}$, $r.\vec{l} \in V$.
7. The multiplication operation is distributive with the addition operator, i.e. for any $r, s \in \mathbb{R}$ and $\vec{l}, \vec{m} \in V$, $(r + s).\vec{l} = r.\vec{l} + s.\vec{l}$ and $r.(\vec{l} + \vec{m}) = r.\vec{l} + r.\vec{m}$.
8. The multiplication operation is compatible with the scalar multiplication operation, i.e. for any $r, s \in \mathbb{R}$ and any $\vec{l} \in V$, $r.(s.\vec{l}) = (rs).\vec{l}$.
9. There exists an identity element of scalar multiplication, i.e. for any $\vec{l} \in V$, $1.\vec{l} = \vec{l}$.

#### Inner Product Space
An Inner Product Space is a vector space $V$ with an inner product operation, which is a mapping $\langle\cdot, \cdot\rangle: V \times V \to \mathbb{R}$. Note that the range can either be $\mathbb{R}$ or $\mathbb{C}$, but we will only consider the case for $\mathbb{R}$ here. The inner product should satisfy the following properties.
1. $\langle \vec{l}, \vec{m} \rangle = \langle \vec{m}, \vec{l} \rangle$ for any $\vec{l}, \vec{m} \in V$.
2. $\langle r.\vec{l}, \vec{m} \rangle = r\langle \vec{l}, \vec{m} \rangle$ and $\langle \vec{l} + \vec{m}, \vec{n} \rangle = \langle \vec{l}, \vec{n} \rangle + \langle \vec{m}, \vec{n} \rangle$, for any $r\in \mathbb{r}$ and $\vec{l}, \vec{m}, \vec{n} \in V$.
3. $\langle \vec{l}, \vec{l}\rangle > 0$ for any $\vec{l} \in V$ and $\langle \vec{l}, \vec{l}\rangle = 0 \iff \vec{l} = \vec{0}$.

#### Vectors, matrices and tensors
###### Vectors
A particular inner product space of interest is the real coordinate space of n dimensions $\mathbb{R}^n$. A standard element of the $\mathbb{R}^n$ space can be written as $\mathbf{X} = (x_1, x_2, \dots , x_n)$, where $x_1, x_2, \dots , x_n \in \mathbb{R}$. Elements of this space go by the term `vector`, which are basically 1 dimensional arrays, i.e. an ordered finite list of numbers. The elements of a vector are the values of the array, while the size of a vector is the number of elements in the array.

#### Vectors in $\mathbb{R}^n$ space
A particular inner product space of interest is the real coordinate space of n dimensions $\mathbb{R}^n$. A standard element of the $\mathbb{R}^n$ space can be written as $\mathbf{X} = (x_1, x_2, \dots , x_n)$, where $x_1, x_2, \dots , x_n \in \mathbb{R}$. Elements of this space go by the term `vector`, which are basically 1 dimensional arrays, i.e. an ordered finite list of numbers. The elements of a vector are the values of the array, while the size of a vector is the number of elements in the array.

#### Matrices
