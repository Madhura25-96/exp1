###  Theory 
In this section, we shall provide some essential theory related to Part-1 of Experiment-1

We shall discuss the following topics:
- Introduction to Finite Fields and Binary Arithmetic.
- Vector space spanned by the given set of vectors.

#### Introduction to Finite Fields and Binary Arithmetic

This section will introduce preliminaries about finite fields and binary arithmetic
that are relevant to Experiment-1. For a detailed discussion of the topics, please refer
Chapter 2 of [1] and Chapter 1 of [2]. For all the experiments considered in this virtual
lab, we consider the vectors and matrices that are defined over a finite field. In order
to define a finite field, we need to first define a “binary operation”, which is provided
next.

**Definition 1** _(Binary operation): Let F be a set of elements. A binary  operation ⋆ is
a rule that assigns to each pair of  elements a , b ∈ F a uniquely defined third element
c = a ⋆ b ∈ F._


For example, consider the set of real numbers, denoted by R. It can be verified
that the addition operation defined for real numbers is a binary operation. In order to
define a field, consider a set F on which two binary operations called addition (+) and
multiplication (·) are defined. For the given {F , + , .}, definition of the field is given below.


**Definition 2** _(Field):{F,+,·}is said to be a field if satisfies the following axioms:_

- Associativity of (+) and (·) : Elements a, b, c ∈  satisfy a + (b + c) = (a + b) + c
    and a · ( b ·c ) = ( a · b )· c.
- Commutativity of (+) and (.):  Elements a, b, c ∈ F  satisfy a  +  b  =  b  +  a and
    a  ·  b  =  b  ·  a.
- Distributivity of multiplication over addition: Elements a, b, c ∈ F  satisfy a · ( b +
    c) = (a · b ) + (a · c).
- Additive identity: There exist an element 0 ∈ F such that a + 0 = a.
- Multiplicative identity: There exist an element 1 ∈ Fsuch that a · 1 = a and 1 ≠ 0 .
- Additive inverses: For every a ∈ F, there exists an element in F, denoted by −a,
    called the additive inverse of a, such that a + (−a) = 0.
- Multiplicative inverses: For every a ≠ 0 ∈ F, there exists an element in F, denoted
    by a<sup>-1</sup> or 1 /a, called the multiplicative inverse of a, such that a·a<sup>-1</sup> = 1.
It can be verified that the set of real numbers R along with the addition and multiplication defined over 
real numbers is a field. Let us now consider an example of a field with finite number of elements. Consider a set F<sub>2</sub> = {0 ,1 } with the addition and
multiplication operations for  any a, b ∈ F<sub>2</sub> defined as Equation (1)


 $$\begin{pmatrix}
 0 + 0 = 0\\  
 0 + 1 = 1\\                         
 1 + 0 = 1\\   
 1 + 1 = 0\end{pmatrix} 
 \space
 \space
 \space
 \space
 \begin{pmatrix}
 0 . 0 = 0\\
 0 . 1 = 0\\
 1 . 0 = 0\\
 1 · 1 = 1
 \end{pmatrix}$$         
 
                                                  
#### 

It can be verified that the set F<sub>2</sub> along with the addition and multiplication operations
defined in Eq. (1) is a finite field, since it satisfies the axioms of Definition 2. Such a field
with finite number of elements is called as a finite field. For most of the experiments
in this virtual lab, we will focus on the binary field  F<sub>2</sub> = { 0 , 1 }. We shall study more
about finite fields in Experiment-6.
Except for Experiments 6 and 7, we will consider vectors and matrices defined over
the binary field F<sub>2</sub> . Vectors are denoted by boldface letters and the components of
a vector are denoted by lower case letters, e.g. the components of a  vector **v** ∈  F<sub>2</sub><sup>n</sup> .
are denoted by **V** =  [v<sub>1</sub>  v<sub>2</sub>  … v<sub>n</sub> ] , where each v<sub>i</sub> ∈ F<sub>2</sub> for i= 1, 2 ,... , n. Vectors can either be considered as row vectors or columns vectors.  Matrices are denoted by upper-case letters, e.g.
consider a matrix  M ∈  F<sub>2</sub><sup>m x n </sup> with m rows and n columns.
The component of the matrix M corresponding to  the i<sup>th</sup> row and j<sup>th</sup> column,
for 1 ≤ i ≤ m and 1 ≤ j ≤ n, is denoted by  M<sub>ij </sub>.
1 ≤ j ≤ n, is denoted by  M<sub>ij </sub>.


We shall next define addition and multiplication operations for vectors and matrices
that are defined over F<sub>2</sub> :

- Addition of two vectors : The addition of two vectors v ,w ∈ F<sub>2</sub><sup>n</sup> consists of addition
    of their respective components defined according to Eq. (1), i.e.,  Equation (2) :-

$$\mathbf{v + w} =  \begin{pmatrix}
                    v_{1}  \\
                    v_{2}  \\
                    .   \\
                    v_{n}  \end{pmatrix}
                    \space
                    \space
                    +
                    \space
                    \space
                    \begin{pmatrix}
                    w_{1}  \\
                    w_{2}  \\
                    .   \\
                    w_{n}  \end{pmatrix}
                    \space
                    \space
                    =
                    \space
                    \space
                    \begin{pmatrix}
                    v_{1} + w_{1}  \\
                    v_{2} + w_{2}  \\
                    .        \\
                    v_{n} + w_{n}  \end{pmatrix}$$
                    
                    
        



- Multiplication of a vector by a scalar: For a vector v ∈ F<sub>2</sub><sup>n</sup> and a scalar a ∈ F<sub>2</sub> ,
    a . v is given by  Equation (3)
    
$$\mathbf{a . v}  =  a . 
                     \begin{pmatrix}
                      v_{1}  \\
                      v_{2}  \\
                      .   \\
                      v_{n}   
                      \end{pmatrix}
                      \space
                      \space
                      =
                      \space
                      \space
                      \begin{pmatrix}
                       a . v_{1} \\
                       a . v_{2} \\
                         .    \\
                       a . v_{n} 
                       \end{pmatrix}$$
                      
        
where the operation a·v<sub>i</sub> for i = 1, 2 ,... , n is performed according to Eq. (1).
- Multiplication of a vector and a matrix: For a vector v ∈ F<sub>2</sub><sup>n</sup> and a matrix M ∈ F<sub>2</sub><sup>n x m </sup> , v . M is given by 

$$\mathbf { v . M }  =  \begin{pmatrix} v_{1} &  v_{2}  &  .  & v_{n} \end{pmatrix} 
                        \space
                        \begin{pmatrix} M_{11} & M_{12} &  .  & M_{1m} \\
                                        M_{21} & M_{22} &  .  & M_{2m} \end{pmatrix}
                        =
                        \begin{pmatrix} v_{1}.M_{11} & + & v_{2}.M_{12} & + & . & + & v_{n}.M_{1m} \\
                                        v_{1}.M_{21} & + & v_{2}.M_{22} & + & . & + & v_{n}.M_{2m} \\
                                                   . \\
                                        v_{1}.M_{n1} & + & v_{2}.M_{n2} & + & . & + & v_{n}.M_{nm} \end{pmatrix}$$

where note that each component wise addition and multiplication is performed according to Eq. (1).

#### Vector space spanned by the given set of vectors

Towards defining the vector space spanned by the given set of vectors, we first define
linear combination of the given set of vectors and scalars.

**Definition 3** _(Linear combination): The linear combination of the given set of vectors
v<sub>1</sub> ,v<sub>2</sub> ,... ,v<sub>m</sub> ∈ F<sub>2</sub><sup>n</sup> and the corresponding set of scalars a<sub>1</sub> ,a<sub>2</sub> ,... ,a<sub>m</sub> ∈ F<sub>2</sub> is defined
as a vector v obtained as_

v = a<sub>1</sub>v<sub>1</sub> + a<sub>2</sub>v<sub>2</sub> +.. .+ a<sub>m</sub>v<sub>m</sub>.


For example, the linear combination of v<sub>1</sub> = [1 1 0], v<sub>2</sub> = [0 1 0] ,v<sub>3</sub> = [1 1 1] ∈ F<sub>2</sub><sup>3</sup> and the corresponding set of scalars a<sub>1</sub> = 0, a<sub>2</sub> = 1, a<sub>3</sub> = 0 ∈ F<sub>2</sub> is equal to [0 1 0].We shall next provide the definition of a vector space spanned by
the given set of vectors.

**Definition 4** _(Vector space spanned the given set of vectors): The vector space V
spanned by the vectors v<sub>1</sub> ,v<sub>2</sub> ,... ,v<sub>m</sub> ∈ F<sub>2</sub><sup>n</sup> is defined as_

V= { v ∈F<sub>2</sub><sup>n</sup>|v = a<sub>1</sub>v<sub>1</sub> + a<sub>2</sub>v<sub>2</sub> +.. .+ a<sub>m</sub>v<sub>m</sub> for some scalars a<sub>1</sub> ,a<sub>2</sub> ,... , a<sub>m</sub> ∈ F<sub>2</sub>}.
This vector space V is also called as the span of the vectors v 1 ,v 2 ,... ,vm, denoted by V = span{v<sub>1</sub> ,v<sub>2</sub> ,... ,v<sub>m</sub>}.
  For example, the vector space spanned by the vectors v<sub>1</sub> =[ 1 0 1], v<sub>2</sub> = [ 0 0 1] and v<sub>3</sub> = [ 0 1 0] is given by
  
$$\mathbf{V} =  span\begin{pmatrix}
                v_{1} & , & v_{2} & , & v_{3}
                \end{pmatrix}
                \space
                \space
                =
                \space
                \space
                \begin{pmatrix}
                0 \\
                0 \\
                0 \\
                \end{pmatrix}
                \space
                ,
                \space
                \begin{pmatrix}
                1 \\
                0 \\
                0 \\
                \end{pmatrix}
                \space
                 ,
                \space
                \begin{pmatrix}
                0 \\
                1 \\
                0 \\
                \end{pmatrix}
                \space
                 ,
                \space
                \begin{pmatrix}
                0 \\
                0 \\
                1 \\
                \end{pmatrix}
                \space
                ,
                \space
                \begin{pmatrix}
                1 \\
                0 \\
                1 \\
                \end{pmatrix}
                \space
                ,
                \space
                \begin{pmatrix}
                1 \\
                1\\
                0\\
                \end{pmatrix}
                \space
                 ,
                \space
                \begin{pmatrix}
                0\\
                1\\
                1\\
                \end{pmatrix}
                \space
                ,
                \space
                \begin{pmatrix}
                1\\
                1\\
                1\\
                \end{pmatrix}$$


  Note that V = F<sub>2</sub><sup>3</sup> since it consists of all possible vectors in F<sub>2</sub><sup>3</sup>. However note that this need not be the case always. For example, span{v<sub>1</sub> ,v<sub>2</sub> } ̸= F<sub>2</sub><sup>3 </sup>.We shall next define a subspace of a vector space.

**Definition 5**_(Subspace): A subspace of a vector space is a nonempty subset that satisfies the requirements for a vector space._

For the example mentioned above, span {v<sub>1</sub>,v<sub>2</sub>}is a subspace of span{v<sub>1</sub>,v<sub>2</sub>,v<sub>3</sub>}.

**Definition 6** _(Linear independence): A given set of vectors v<sub>1</sub>,v<sub>2</sub> ,... ,v<sub>m</sub> ∈ F<sub>2</sub><sup>n</sup> are
said to be independent if and only if a<sub>1</sub>v<sub>1</sub> + a<sub>2</sub>v<sub>2</sub> +.. .+a<sub>m</sub>v<sub>m</sub> = 0 can happen only when a<sub>1</sub> = a<sub>2</sub> =. .= a<sub>m</sub>= 0._

For example, it can be verified that the vectors v<sub>1</sub> =[1 0 1], v<sub>2</sub> =[0 0 1] and v<sub>3</sub> = [0 1 0] are linearly independent since a<sub>1</sub>v<sub>1</sub> + a<sub>2</sub>v<sub>2</sub>+ a<sub>3</sub>v<sub>3</sub> gives an all-zero vector only when we choose a<sub>1</sub> = a<sub>2</sub> = a<sub>3</sub>= 0. Whereas the vectors v<sub>1</sub> = [1 0 1], v<sub>2</sub>=[0 0 1] and v<sub>3</sub>= [1 0 0] are linearly dependent since v<sub>1</sub> + v<sub>2</sub> + v<sub>3</sub>=0. 
