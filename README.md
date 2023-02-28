# PLONK Arithmetisation Assignment

Calculate polynomials used in PLONK Arithmetisation. Fill in the values in this markdown to complete the assignment

The polynomial used in this assignment is: $$x^3 + x == 2$$

## Gates

Complete the gates below, the first one is completed for you

### Gate 1

$$x_1 * x_1 = x_2$$

### Gate 2

$$x_2 * x_1 = x_3$$

### Gate 3

$$x_1 + x_3 = x_4$$

### Gate 4

$$x_4 = 2$$

## Assignments

Complete the assignment vectors, let $x_1 = 1$

$$\vec{a} = [1,1,1,2]$$

$$\vec{b} = [1,1,1,0]$$

$$\vec{c} = [1,1,2,0]$$

## Selectors

Fill in the below table for the values of $q_L$, $q_R$, $q_O$, $q_M$ and $q_C$, satisfying the equation: 

$$q_L * a + q_R * b + q_O * c + q_M * a*b + q_C = 0$$


|$q_L$|$q_R$|$q_O$|$q_M$|$q_C$|
|-----|-----|-----|-----|-----|
|  0  |  0  |  -1 |  1  |  0  |
|  0  |  0  |  -1 |  1  |  0  |
|  1  |  1  |  -1 |  0  |  0  |
|  1  |  0  |  0  |  0  |  -2 |

## Domain

We will use the base field of $\mathbb{F_{17}}$ and the domain consisting of roots of unity

Fourth roots of unity in $\mathbb{F_{17}}$:
$$H: {1, 4, 16, 13}$$

## Cosets

$$k_1 = 2$$

$$k_2 = 3$$

$$k_{1}H: {2, 8, 15, 9}$$

$$k_{2}H: {3, 12, 14, 5}$$

## Interpolating Polynomials

$$f_a(x) = 16x^3 + 4x^2 + 1x + 14$$

$$f_b(x) = x^3 + 13x^2 + 16x + 5$$

$$f_c(x) = 5x^3 + 9x^2 + 3x + 1$$

$$q_{L}(x) = 3x^3 + 0x^2 + 5x + 9$$

$$q_{R}(x) = 4x^3 + 13x^2 + 4x + 13$$

$$q_{O}(x) = 16x^3 + 4x^2 + 1x + 12$$

$$q_{M}(x) = 14x^3 + 0x^2 + 12x + 9$$

$$q_{c}(x) = 2x^3 + 9x^2 + 15x + 8$$

## Copy Constraints

| LHS | RHS | Domain of LHS | Domain of RHS |
|-----|-----|---------------|---------------|
|$a_1$|$b_1$|       1       |       2       |
|$a_2$|$c_1$|       4       |       3       |
|$a_3$|$b_1$|       16      |       2       |
|$a_4$|$c_3$|       13      |       14      |
|$b_1$|$a_1$|       2       |       1       |
|$b_2$|$a_1$|       8       |       1       |
|$b_3$|$c_2$|       15      |       12      |
|$b_4$|$b_4$|       9       |       9       |
|$c_1$|$a_2$|       3       |       4       |
|$c_2$|$b_3$|       12      |       15      |
|$c_3$|$a_4$|       14      |       13      |
|$c_4$|$c_4$|       5       |       5       |

## Copy Constraints Polynomials

$$S_{{\sigma}_1} = 6x^3 + x^2 + 11x + 1$$

$$S_{{\sigma}_2} = 2x^3 + 5x^2 + x + 10$$

$$S_{{\sigma}_3} = 12x^3 + 12x^2 + 9x + 5$$
