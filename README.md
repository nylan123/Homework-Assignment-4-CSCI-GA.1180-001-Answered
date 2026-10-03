# Homework-Assignment-4-CSCI-GA.1180-001-Answered
Email: jarviscodinghub@gmail.com

https://jarviscodinghub.com/product/homework-assignment-4-csci-ga-1180-001-answered/

Exercise 4.1. Consider the linear least-squares problem of minimizing kb − Axk
2
2
, where A is a nonzero
m × n matrix with rank(A) = n, and b is nonzero.
(a) If the optimal residual b − Ax is zero and the optimal x is nonzero, what does this imply about the
representation of b as a linear combination of vectors in the range space of A and the null space of AT
?
Explain your answer.
(b) If the optimal solution x is zero and the optimal residual is nonzero, what does this imply about the
representation of b as a linear combination of vectors in the range space of A and the null space of AT
?
Explain your answer.
(c) Let b1 and b2 be nonzero m-vectors such that b1 6= b2. Let x1 denote a solution of the linear leastsquares problem involving A and b1, with a similar meaning for x2 and the least-squares problem
involving A and b2. If x1 = x2, what does this imply about the relationship between b1 and b2?
Explain.
Exercise 4.2. Let v be any nonzero n-vector. The associated Householder matrix is defined as
H(v) = I −
2vvT
kvk
2
2
.
(a) Show that, for any nonzero v, its associated Householder matrix is orthogonal.
(b) Show that, for any scalar α 6= 0, H(αv) = H(v).
(c) For any two nonzero n-vectors a and b with a 6= b and kak2 = kbk2, assume that there is an n-vector
u such that
kuk2 = 1 and Ha = (I − 2uuT
)a = b, where H = H(u).
Give an expression for u in terms of a and b.
(d) Let
a =

9
2
−1
!
and b =

7
2
−3
!
,
so that kak
2
2 = kbk
2
2 = 85/4. Give the explicit vector u defined in part (c), including an explanation of
how you computed it.
(e) Write down the explicit 2 × 2 Householder matrix associated with the vector u from part (d), and
confirm numerically that Ha = b.
2
Exercise 4.3. Let A be an m × n matrix with m > n and rank(A) = n. Assume that the singular value
decomposition of A is USV T
, where U is m × m and orthogonal, V is n × n and orthogonal, and S is an
m × n “diagonal” matrix of the form
S =

Sn
0
!
,
where Sn is a nonsingular n × n diagonal matrix Sn = diag(σ1, . . . , σn), with σ1 ≥ · · · ≥ σn > 0.
(1) Using the pseudoinverse of A and the fact that any m-vector b can be expressed as a linear combination
of the columns of U, mathematically express the solution x of the least-squares problem min kb − Axk
2
2
as a linear combination of the columns of V , i.e., specify the coefficients in the linear combination.
(2) In Matlab calculations for this problem, use format long e. Let
A =


1 1
1 1 + 10−6
1 1 + 10−6

 , b1 =


1
2.22474
−0.22474


and b2 =


−2
1
1

 ,
where kb1k2 = 2.44948487 and kb2k2 = 2.44948974 (both rounded to 9 figures), so that kb1 − b2k2 is
about 4.87 × 10−6
.
(a) Give U, S, and V from the computed SVD of A. Express b1 and b2 numerically as linear combinations of the columns of U, i.e., give the computed values of the coefficients in the linear
combinations.
(b) Give the computed matrix A†
, the pseudoinverse of A, obtained from the matrices U, V , and S.
(Do not use the Matlab command pinv except to check your result.)
(c) Let x1 be the least-squares solution of min kb1 − Axk
2
2
. Give x1, kx1k2, and the ratio kx1k/kb1k.
Express x1 as a linear combination of the columns of V , i.e., give the coefficients in the linear
combination, both in mathematical form and as calculated numbers.
(d) Let x2 be the least-squares solution of min kb2 − Axk
2
2
. Give x2, kx2k2, and the ratio kx2k/kb2k.
Express x2 as a linear combination of the columns of V , i.e., give the coefficients in the linear
combination, both in mathematical form and as calculated numbers.
(e) Comment on the difference in norm between x1 and x2 relative to the difference in norm between
b1 and b2. Explain this difference using your results from part (a).
Exercise 4.4. Let A be an m × n matrix with m < n such that rank(A) = m. Assume that A can be
written as
A =

B S 
, where B is nonsingular.
(a) Given A in the form above, let Z be defined as
Z =

−B−1S
In−m
!
, where In−m is the (n − m) × (n − m) identity.
Show that (i) AZ = 0 and that (ii) the columns of Z are linearly independent. (Which means that the
columns of Z form a basis for the null space of A.)
(b) When Z is defined as given above, describe how to form the matrix-products Zv and Z
T
q using only
S and the LU factorization of B (so that the explicit matrix B−1
is not needed).
3
Exercise 4.5. This problem involves a variation on the (extremely silly) model discussed in class, developed
by someone from another planet based on looking at pictures of smiling people in Vogue magazine. The
underlying premise is that the happiest people seem to be tall, thin, and blonde. Assume that the visitor
from another planet believes that happiness for a given individual is given by
h ≈ x1
√
t − 4 + x2
100
w

+ x3 exp(−c), (1)
where t is “tallness” (measured in feet), w is weight (measured in pounds), c is hair color (where the
measured value of c ranges from 0 to 1, with larger values meaning blonder hair), and h is happiness. The
three coefficients x1, x2, and x3 are unknown.
Suppose that you are given the following observed data for 6 people.
ti 5.2 6.0 5.9 5.6 6.2 5.7
wi 240 162.3 130.8 150.1 95.9 141.2
ci 0.13 0.83 1.0 0.24 0.31 0.47
Assume that you wish to find the optimal coefficients x = (x1, x2, x3)
T
that produce the best fit of the
model (1) to a given set of data by minimizing kb − Axk
2
2
for an appropriate matrix A and right-hand side
vector b.
If using Matlab for this problem, use format short e (and the equivalent in other systems).
(a) Give the mathematical form of the entries in row i of A, expressed in terms of ti
, wi
, and ci
.
(b) Give the specific matrix A and the value of cond2(A).
(c) Assume that the observed values of happiness for the six individuals are
h = (9, 8, 7, 10, 12, 9).
(i) Give the vector b that will appear in the least-squares problem, corresponding to the data above,
and give kbk2.
(ii) Solve the least-squares problem numerically, and state how you performed this calculation. Matlab
will do this with the command x = Ab, or you may prefer to form and solve the normal equations
explicitly.
(iii) Give the optimal x, the vector Ax, the optimal residual vector r = b − Ax, krk2, and the ratio
krk2/kbk2.
(iv) Based on the numerical results, comment on whether the model seems to you to be effective
at predicting the happiness of individuals in this group. Be explicit about how you measure
effectiveness.
(v) Which individual is predicted to be the happiest? Why (based on his/her individual properties)
might this be the case?
(vi) Which individual is predicted to be the least happy? Why (based on his/her individual properties)
might this be the case?
(vii) Which individual’s observed happiness is closest to the model’s prediction? Why (based on the
individual’s properties) might this be the case?
(viii) Which individual’s observed happiness is farthest from the model’s prediction? Why (based on
the individual’s properties) might this be the case?
(d) Assume that the happiness data were recorded incorrectly, and that the observed happiness values for
the same six individuals should be
h = (4.5, 6.5, 10, 5.5, 11, 6).
4
(i) Solve the least-squares problem numerically using the same A as in part (b), but with the second
set of happiness data. Give the vector b for the second set of happiness data, the optimal x, the
vector Ax, the optimal residual vector r = b − Ax, krk2, and the ratio krk2/kbk2.
(ii) Is the model an effective predictor of happiness with this set of data? Explain your opinion using
the numerical results.
(iii) Does anything about the optimal coefficients in this case strike you as strange? If so, please
explain and comment on possible causes, making an explicit comparison to the results in part (c).
