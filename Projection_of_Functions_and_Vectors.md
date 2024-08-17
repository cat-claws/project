
# Projection of Functions and Vectors

## 1. Introduction to Function Projection

Projecting one function onto another typically refers to finding the best approximation of one function (say \( f(x) \)) in the space spanned by another function (or set of functions). This is often done by minimizing the difference (error) between the two functions in some normed space.

### 1.1 Inner Product Space

The inner product of two functions \( f(x) \) and \( g(x) \) is often written as:
\[
\langle f, g \rangle = \int_{a}^{b} f(x) g(x) \, dx
\]
where \( [a, b] \) is the interval over which the functions are defined.

### 1.2 Projection of a Function

If you want to project a function \( f(x) \) onto another function \( g(x) \), you typically find a scalar \( c \) such that:
\[
P(f) = c \cdot g(x)
\]
where \( P(f) \) is the projection of \( f(x) \) onto \( g(x) \).

The coefficient \( c \) is determined by:
\[
c = \frac{\langle f, g \rangle}{\langle g, g \rangle}
\]
This formula gives the scalar that, when multiplied by \( g(x) \), gives the projection of \( f(x) \) onto \( g(x) \).

### 1.3 Example: Projecting \( f(x) = x^2 \) onto \( g(x) = x \) over the interval \( [0, 1] \)

1. Compute the inner products:
\[
\langle f, g \rangle = \int_{0}^{1} x^2 \cdot x \, dx = \int_{0}^{1} x^3 \, dx = \frac{1}{4}
\]
\[
\langle g, g \rangle = \int_{0}^{1} x \cdot x \, dx = \int_{0}^{1} x^2 \, dx = \frac{1}{3}
\]

2. Compute the coefficient \( c \):
\[
c = \frac{\langle f, g \rangle}{\langle g, g \rangle} = \frac{\frac{1}{4}}{\frac{1}{3}} = \frac{3}{4}
\]

3. The projection is:
\[
P(f) = \frac{3}{4} \cdot x
\]

### 1.4 Example: Projecting \( f(x, y) = x + y \) onto \( g(x, y) = x - y \) over the unit square \( [0, 1] \times [0, 1] \)

1. **Original Function**: \( f(x, y) = x + y \)

2. **Projection onto the \( xy \)-plane**: Fix \( z = 0 \) and reduce the function to:
\[
f_{xy\text{-plane}}(x, y) = x + y
\]

3. **Further Simplification: Projection onto the x-axis**: Fix \( y = 0 \):
\[
f_{x\text{-axis}}(x) = x
\]

## 2. Projection onto a Specific Dimension

For discrete vectors, projecting onto specific dimensions involves selecting components along the chosen axes, reducing the dimensionality. This concept is extended to functions by fixing some variables.

### 2.1 Example: Projecting a 3D Vector onto a 2D Plane

Consider a 3D vector \( \mathbf{v} = [v_1, v_2, v_3] \) and you want to project it onto the \( xy \)-plane:

1. **Original Vector**: \( \mathbf{v} = [v_1, v_2, v_3] \)

2. **Projection onto \( xy \)-plane**: Ignore the \( z \)-component:
\[
\mathbf{v}_{xy} = [v_1, v_2]
\]

### 2.2 Example: Projecting a 4D Vector onto a 2D Subspace

Consider a 4D vector \( \mathbf{v} = [v_1, v_2, v_3, v_4] \) and project it onto the subspace spanned by the first and third axes:

1. **Original Vector**: \( \mathbf{v} = [v_1, v_2, v_3, v_4] \)

2. **Projection onto the subspace spanned by the first and third axes**:
\[
\mathbf{v}_{13} = [v_1, v_3]
\]

## 3. Projection of a Function onto a Subspace Defined by Multiple Axes

When projecting a function onto a subspace defined by multiple axes, the function is typically simplified by reducing the number of variables it depends on.

### 3.1 Example: Simplifying a Function by Projection

Consider the 3D function \( f(x, y, z) = x^2 + 2xy + y^2 + z^2 \).

1. **Original Function**:
\[
f(x, y, z) = x^2 + 2xy + y^2 + z^2
\]

2. **Projection onto the \( xy \)-plane**:
\[
f_{xy\text{-plane}}(x, y) = x^2 + 2xy + y^2
\]

3. **Further Simplification: Projection onto the x-axis**:
\[
f_{x\text{-axis}}(x) = x^2
\]

By projecting onto the \( xy \)-plane and further onto the \( x \)-axis, the function is simplified from a 3D function to a 2D function and then to a 1D function.
