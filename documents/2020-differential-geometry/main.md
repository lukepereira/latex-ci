---
title:  Differential Geometry
---

-   [Prerequisites](#prerequisites)
    -   [Topology of Manifolds Intro](#topology-of-manifolds-intro)
    -   [Algebras](#algebras)
    -   [Derivations](#derivations)
    -   [Equivalence Relations](#equivalence-relations)
    -   [On relation to Physics](#on-relation-to-physics)
-   [Manifolds](#manifolds)
    -   [Atlases and Charts](#atlases-and-charts)
    -   [Definition of manifold](#definition-of-manifold)
    -   [Examples of manifolds](#examples-of-manifolds)
        -   [N-spheres](#n-spheres)
        -   [Products and n-torus](#products-and-n-torus)
        -   [Real projective spaces](#real-projective-spaces)
        -   [Complex projective spaces](#complex-projective-spaces)
        -   [Grassmannians](#grassmannians)
        -   [Complex Grassmannians](#complex-grassmannians)
    -   [Oriented manifolds](#oriented-manifolds)
    -   [Open subsets](#open-subsets)
    -   [Compact subsets](#compact-subsets)
-   [Smooth Maps](#smooth-maps)
    -   [Smooth functions on manifolds](#smooth-functions-on-manifolds)
    -   [Smooth maps between manifolds](#smooth-maps-between-manifolds)
    -   [Diffeomorphisms of manifolds](#diffeomorphisms-of-manifolds)
    -   [Examples of smooth maps](#examples-of-smooth-maps)
        -   [Products, diagonal maps](#products-diagonal-maps)
        -   [The diffeomorphism $\mathbb R P^1 \cong S^1$
            ](#the-diffeomorphism-mathbb-r-p1-cong-s1)
        -   [The diffeomorphism
            $\mathbb C P^1 \cong S^2$](#the-diffeomorphism-mathbb-c-p1-cong-s2)
        -   [Maps to and from projective
            space](#maps-to-and-from-projective-space)
        -   [The Hopf fibration, a.k.a. the quotient map
            $S^{2n+1} \rightarrow \mathbb C P^n$](#the-hopf-fibration-a.k.a.-the-quotient-map-s2n1-rightarrow-mathbb-c-pn)
    -   [Submanifolds](#submanifolds)
    -   [Smooth maps of maximal rank](#smooth-maps-of-maximal-rank)
        -   [The rank of a smooth map](#the-rank-of-a-smooth-map)
        -   [Local diffeomorphisms](#local-diffeomorphisms)
        -   [Level sets, submersions](#level-sets-submersions)
        -   [Example: The Steiner surface](#example-the-steiner-surface)
        -   [Immersions](#immersions)
-   [The Tangent Bundle](#the-tangent-bundle)
    -   [Tangent map](#tangent-map)
        -   [Definition of the tangent map, basic
            properties](#definition-of-the-tangent-map-basic-properties)
        -   [Coordinate description of the tangent
            map](#coordinate-description-of-the-tangent-map)
    -   [Tangent spaces of
        submanifolds](#tangent-spaces-of-submanifolds)
        -   [Example: Steiner's surface
            revisited](#example-steiners-surface-revisited)
        -   [The tangent bundle](#the-tangent-bundle-1)
-   [Vector Fields](#vector-fields)
    -   [Vector fields as derivations](#vector-fields-as-derivations)
    -   [Vector fields as sections of the tangent
        bundle](#vector-fields-as-sections-of-the-tangent-bundle)
    -   [Lie brackets](#lie-brackets)
    -   [Related vector fields](#related-vector-fields)
    -   [Flows of vector fields](#flows-of-vector-fields)
    -   [Geometric interpretation of the Lie
        bracket](#geometric-interpretation-of-the-lie-bracket)
    -   [Frobenius theorem](#frobenius-theorem)
-   [Differential Forms](#differential-forms)
    -   [Review: Differential forms on
        $\mathbb R^m$](#review-differential-forms-on-mathbb-rm)
    -   [Dual spaces](#dual-spaces)
    -   [Cotangent spaces](#cotangent-spaces)
    -   [1-forms](#forms)
    -   [Pull-backs of function and
        1-forms](#pull-backs-of-function-and-1-forms)
    -   [Integration of 1-forms](#integration-of-1-forms)
    -   [2-forms](#forms-1)
    -   [k-forms](#k-forms)
        -   [Definition](#definition)
        -   [Wedge product](#wedge-product)
        -   [Exterior differential](#exterior-differential)
    -   [Lie derivatives and
        contractions](#lie-derivatives-and-contractions)
        -   [Pull-backs](#pull-backs)
        -   [Integration of differential
            forms](#integration-of-differential-forms)
        -   [Integration over oriented
            submanifolds](#integration-over-oriented-submanifolds)
        -   [Stokes' theorem](#stokes-theorem)
        -   [Volume forms](#volume-forms)
-   [De Rham Cohomology](#de-rham-cohomology)
-   [Overview of Riemannian Geometry](#overview-of-riemannian-geometry)
    -   [Covariant derivative and
        curvature](#covariant-derivative-and-curvature)
    -   [Curvature](#curvature)
-   [Lie Groups](#lie-groups)

# Prerequisites

## Topology of Manifolds Intro

The fundamental objects of study in differential geometry are manifolds.
Roughly, an n-dimensional manifold is a mathematical object that
"locally" looks like $\mathbb R^n$. Manifolds in euclidean space are
described with a *regular level set*, $S = f^{-1}(a)$ which defines a
smooth hypersurface $S \subseteq R^n$. For example, the n-dimensional
sphere described by:
$$S^n = \{ (x^0, \dots, x^n) \in \mathcal R^{n+1} | (x^0)^2 + \dots + (x^n)^2  = 1\}.$$
Another example is the 2-Torus, $T^2$. Given real numbers $r, R$ with
$0 < r < R$, take a circle of radius $r$ in the $x-z$ plane, with center
at $(R,0)$, and rotate about the $z$-axis:
$$T^2 = \{ (x,y,z) | (\sqrt{x^2 + y^2} - R)^2 + z^2 + r\}$$

The sphere, the torus, the double torus, triple torus, and so on are
*orientable* surfaces, which essentially means that they have two sides
which you might paint in two different colors. It turns out that these
are all orientable surfaces, if we consider the surfaces intrinsically
and only consider surfaces that are compact in the sense that they don't
go off to infinity and do not have a boundary (thus excluding a
cylinder, for example).

Not all surfaces can be realized as 'embedded' in $\mathbb R^3$; for
*non-orientable surfaces* one needs to allow for self-intersections.
This type of realization is referred to as an immersion: We don't allow
edges or corners, but we do allow that different parts of the surface
pass through each other. An example is the Klein bottle, which is not
possible to represent as a regular level set $f^{-1}(0)$ of a function
$f$ since any suface has one side where $f$ is positive and another side
where $f$ is negative.

The projective plane or projective space is denoted $\mathbb{R} P^2$ and
is defined as the set of all lines (i.e., 1-dimensional subspaces) in
$\mathbb{R}^3$. we can also think of $\mathbb{R} P^2$ as the set of
antipodal (i.e., opposite) points on $S^2$. Splitting the points into
those with distance $< \epsilon$ from the equator and those
$\geq \epsilon$ produces a Mobius strip and a two-dimensional disc.
Generating a smooth curve by gluing the boundary of a Mobius strip to
the boundary of a disk is depicted in what's known as Boy's surface.

Another operation for surfaces, generalizing the procedure of 'attaching
handles', is the connected sum Given two surfaces $\sigma_1$ and
$\sigma_2$, remove small disks around given points $p_1 \in \sigma_1$
and $p_2 \in \sigma_2$, to create two surfaces with boundary circles.
Then glue-in a cylinder connecting the two boundary circles, without
creating edges. The resulting surface is denoted $\sigma_1\#\sigma_2$.

It turns out that all closed, connected surfaces are obtained from
either the 2-sphere $S^2$, the Klein bottle, or $\mathbb{R} P^2$, by
attaching handles with the connected sum.

## Algebras

An algebra (over the field $\mathbb R$ of real numbers) is a *vector
space* $\mathscr{A}$, together with a *multiplication* (product)
$\mathscr{A} \times \mathscr{A} \rightarrow \mathscr{A}$,
$(a,b) \mapsto ab$ such that

1.  The multiplication is associative.

2.  The multiplication map is linear in both arguments.

The algebra is called commutative if $ab = ba$ for all $a,b \in A$. A
unital algebra is an algebra $A$ with a distinguished element
$1_{\mathscr{A}} \in \mathscr{A}$ (called the unit), with
$1_{\mathscr{A}} a = a = a1_{\mathscr{A}}$ for all $a \in \mathscr{A}$.

One can also consider non-associative product operations on vector
spaces, most importantly one has the class of *Lie algebras*. Some
examples include: The space of complex numbers which is a unital,
commutative algebra. $\mathbb H \cong \mathbb R^4$ of quaternions which
is a unital, non-commutative algebra. The space of $n\times n$ matricies
which is a noncommutative unital algebra. Given a topological space $X$,
one has the algebra $C(X)$ of continuous $\mathbb R$-valued functions.

A *homomorphism* of algebras
$\phi : \mathscr{A} \rightarrow \mathscr{A}'$ is a linear map preserving
products: $\phi(ab) = \phi(a)\phi(b)$. It is called an *isomorphism* of
algebras if $\phi$ is invertible. For the special case
$\mathscr{A}' = A$ , these are also called algebra *automorphisms* of
$\mathscr{A}$. Note that the algebra automorphisms form a group under
composition.

## Derivations

::: {.defn}
**Definition 1**. A derivation of an algebra $\mathscr A$ is a linear
map $D : \mathscr A \rightarrow \mathscr A$ satisfying the product rule
$$D(a_1 a_2) = D(a_1)a_2 +a_1D(a_2).$$.
:::

If $dim A < \infty$, a derivation is an infinitesimal automorphism of an
algebra.

Any given $x \in A$ defines a derivation $D(a) = [x,a] := xa-ax$. These
are called inner derivations. If $A$ is commutative (for example
$A = C ^\infty(M)$) the inner derivations are all trivial. At the other
extreme, for the matrix algebra $A = \text{Mat}\mathbb R(n)$, one may
show that every derivation is inner.

If $A$ is a unital algebra, with unit $1_A$, then $D(1A) = 0$ for all
derivations $D$.

Given two derivations $D_1,D_2$ of an algebra $A$, their commutator
$[D_1,D_2] = D_1 D_2 - D_2 D_1$ is again a derivation.

If the algebra $A$ is commutative, then the space of derivations is a
'left-module over $A$'. That is, if $D$ is a derivation and $x \in A$
then $a \mapsto (xD)(a) := xD(a)$ is again a derivation

## Equivalence Relations

\[Omitted\]

## On relation to Physics

In Albert Einstein's theory of General Relativity from 1916, space-time
was regarded as a 4-dimensional 'curved' manifold with no distinguished
coordinates. A local observer may want to introduce local $xyz$
coordinates to perform measurements, but all physically meaningful
quantities must admit formulations that are coordinate-free. At the same
time, it would seem unnatural to try to embed the 4-dimensional curved
space-time continuum into some higher-dimensional flat space, in the
absence of any physical significance for the additional dimensions. Some
years later, gauge theory once again emphasized coordinate-free
formulations, and provided physics motivations for more elaborate
constructions such as fiber bundles and connections. There are many
subbranches of differential geometry, for example complex geometry,
Riemannian geometry, or symplectic geometry, which further subdivide
into sub-sub-branches.

# Manifolds

## Atlases and Charts

Manifolds will initially be described in intrinsic or manifestly
coordinate-free terms. The basic feature of manifolds is the existence
of 'local coordinates'. The transition from one set of coordinates to
another should be smooth.

::: {.defn}
**Definition 2**. **(Smoothness and diffeomophisms)**

Let $U \subseteq \mathbb R^m$ and $V \subseteq \mathbb R^n$ be open
subsets. A map $F : U \rightarrow V$ is called *smooth* if it is
infinitely differentiable. The set of smooth functions from $U$ to $V$
is denoted $C^{\infty}(U,V)$. The map $F$ is called a *diffeomorphism*
from $U$ to $V$ if it is invertible, and the inverse map
$F^{-1}: V \rightarrow U$ is again smooth.
:::

::: {.defn}
**Definition 3**. **(Jacobian matrix)**

For a smooth map $F \in C^{\infty}(U,V)$ between open subsets
$U \subseteq R^m$ and $V \subseteq R^n$, and any $x \in U$, one defines
the Jacobian matrix $DF(x)$ to be the $n \times m$ matrix of partial
derivatives, $$(DF(x))^i_j = \frac{\partial F^i}{\partial x^j}$$ Its
determinant is called the Jacobian matrix of $F$ at $x$.
:::

::: {.theorem}
**Theorem 4**. ***(Inverse function theorem)***

*The inverse function theorem states that $F$ is a diffeomorphism if and
only if it is invertible, and for all $x \in U$, the Jacobian matrix
$DF(x)$ is invertible. This means one does not actually have to check
smoothness of the inverse map.*
:::

::: {.defn}
**Definition 5**. **(Charts)**

Let $M$ be a set.

1.  An $m$-dimensional (coordinate) chart $(U,\phi)$ on $M$ is a subset
    $U \subseteq M$ together with a map $\phi : U \rightarrow R^m$ ,
    such that $\phi(U) \subseteq R^m$ is open and $\phi$ is a bijection
    from $U$ to $\phi(U)$.

2.  Two charts $(U,\phi)$ and $(V,\psi)$ are called compatible if the
    subsets $\phi(U \cap V)$ and $\psi(U \cap V)$ are open, and the
    transition map
    $$\psi \circ \phi^{-1}  = \phi(U \cap V) \rightarrow \psi(U \cap V)$$
    is a diffeomorphism known as a change of coordinates. As a special
    case, charts with $U\cap V = \emptyset$ are always compatible.
:::

::: {.defn}
**Definition 6**. **(Atlas)**

Let $M$ be a set. An $m$-dimensional atlas on $M$ is a collection of
coordinate charts $\mathscr{A} =  \{(U_\alpha, \phi_\alpha) \}$ such
that,

1.  The $U_\alpha$ cover all of $M$, i.e. $\bigcup_\alpha U_\alpha = M$.

2.  For all indicies $\alpha, \beta$, the charts
    $(U_\alpha, \phi_\alpha)$ and $(U_\beta, \phi_\beta)$ are
    compatible.
:::

::: {.defn}
**Definition 7**. **(Sterographic projection)**

Regard $\mathbb R^2$ as the coordinate subspace of $\mathbb R^3$ on
which $z = 0$ runs through the center of the sphere; the "equator" is
the intersection of the sphere with this plane. Let $N = (0, 0, 1)$ be
the "north pole", and let $M$ be the rest of the sphere. For any point
$P$ on $M$, there is a unique line through $N$ and $P$, and this line
intersects the plane $z = 0$ in exactly one point $P'$. Define the
stereographic projection of $P$ to be this point $P'$ in the plane.
:::

::: {.example}
**Example 8**. **(Atlas on the 2-sphere)**

Let $S^2 \subseteq \mathbb R^3$ be the unit sphere. Let $n = (0,0,1)$ be
the north pole, and $s =(0,0,-1)$ be the south pole, and define an atlas
with two charts $(U_+,\phi_+)$ and $(U_-,\phi_-)$, where
$$U_+ = S^2 - {s}, U_- = S^2 - {n}$$ and the stereographic projection
from the south pole is given by, $$\begin{aligned}
    \phi_+ : U_+ \rightarrow \mathbb R^2, p \mapsto \phi_+(p)\\
    \phi_+(x, y,z) = \bigg( \frac{x}{1+z},\frac{y}{1+z} \bigg)\end{aligned}$$
and the stereographic projection from the north pole is given by,
$$\begin{aligned}
    \phi_- : U_+ \rightarrow \mathbb R^2, p \mapsto \phi_-(p)\\
    \phi_-(x, y,z) = \bigg( \frac{x}{1-z},\frac{y}{1-z} \bigg).\end{aligned}$$
The transition map on the overlap of the two charts is,
$$\phi_- \circ \phi_+^{-1} (u,v) =  \bigg( \frac{u}{u^2 + v^2}, \frac{v}{u^2 + v^2} \bigg).$$
:::

The 2-sphere with the atlas given by stereographic projections onto the
$x-y$-plane, and the 2-sphere with the atlas given by stereographic
projections onto the $y-z$-plane, should be one and the same manifold
$S^2$. To resolve this, we will use the following notion of
compatibility.

::: {.defn}
**Definition 9**. **(Compatibility)**

Suppose $\mathscr{A} =  \{(U_\alpha, \phi_\alpha) \}$ is an
$m$-dimensional atlas on $M$, and let $(U,\phi)$ be another chart. Then
$(U,\phi)$ is said to be *compatible* with $\mathscr{A}$ if it is
compatible with all charts $(U_\alpha, \phi_\alpha)$ of $\mathscr{A}$
:::

Note that $(U,\phi)$ is compatible with the atlas
$\mathscr{A} =  \{(U_\alpha, \phi_\alpha) \}$ if and only if the union
$\mathscr{A} \cup {(U,\phi)}$ is again an atlas on $M$. This suggests
defining a bigger atlas, by using all charts that are compatible with
the given atlas with the following lemma.

::: {.lemma}
**Lemma 10**. *Let $\mathscr{A} =  \{(U_\alpha, \phi_\alpha) \}$ be a
given atlas on the set $M$. If two charts $(U,\phi), (V,\psi)$ are
compatible with $\mathscr{A}$, then they are also compatible with each
other.*
:::

::: {.theorem}
**Theorem 11**. *Given an atlas
$\mathscr{A} =  \{(U_\alpha, \phi_\alpha) \}$ on $M$, let
$\Tilde{\mathscr{A}}$ be the collection of all charts $(U,\phi)$ that
are compatible with $\mathscr{A}$. Then $\Tilde{\mathscr{A}}$ is itself
an atlas on $M$, containing $\mathscr{A}$. In fact,
$\Tilde{\mathscr{A}}$ is the largest atlas containing $\mathscr{A}$.*
:::

::: {.defn}
**Definition 12**. **(Maximal and equivalent atlases)**

An atlas $\mathscr{A}$ is called *maximal* if it is not properly
contained in any larger atlas. Given an arbitrary atlas $\mathscr{A}$,
one calls $\Tilde{\mathscr{A}}$ the maximal atlas determined by
$\mathscr{A}$. Two atlases are called equivalent if every chart of one
atlas is compatible with every chart in the other atlas. Any maximal
atlas determines an equivalence class of atlases, and vice versa.
:::

## Definition of manifold

::: {.defn}
**Definition 13**. An $m$-dimensional manifold is a set $M$, together
with a maximal atlas $\mathscr{A} =  \{(U_\alpha, \phi_\alpha) \}$ with
the following properties:

1.  **(Countability condition)** $M$ is covered by countably many
    coordinate charts in $A$. That is, there are indices
    $\alpha_1, \alpha_2, \dots$ with $$M = \bigcup_i U_{\alpha_i}.$$

2.  **(Hausdorff condition)** For any two distinct points $p,q \in M$
    there are coordinate charts $(U_\alpha, \phi_\alpha)$ and
    $(U_\beta, \phi_\beta)$ in $A$ such that
    $p \in U_\alpha, q \in U_\beta$, with
    $$U_\alpha \cap U_\beta = \emptyset.$$
:::

The charts $(U,\phi) \in A$ are called (coordinate) charts on the
manifold $M$. The countability condition is used for various arguments
involving a proof by induction. The Hausdorff condition rules out some
strange examples that don't quite fit the idea of a space that is
locally like $\mathbb R^n$.

::: {.lemma}
**Lemma 14**. *Let $M$ be a set with a maximal atlas
$\mathscr{A} =  \{(U_\alpha, \phi_\alpha) \}$, and suppose $p,q \in M$
are distinct points contained in a single coordinate chart
$(U,\phi) \in \mathscr{A}$. Then we can find indices $\alpha,\beta$ such
that $p \in U_\alpha, q \in U_\beta$, with
$U_\alpha \cap U_\beta = \emptyset$.*
:::

## Examples of manifolds

### N-spheres

The construction of an atlas for the 2-sphere $S^2$, by stereographic
projection, also works for the n-sphere
$$S^n = \{ (x^0, \dots, x^n) \in \mathcal R^{n+1} | (x^0)^2 + \dots + (x^n)^2  = 1\}.$$
Let $U_{\pm}$ be the subsets obtained by removing $(\pm 1, 0,\dots, 0)$.
Stereographic projection defines bijections
$\phi_{\pm} : U_{\pm} \rightarrow \mathbb R^{n}$, where
$\phi_{\pm} (x^0, x^1, \cdots, x^n) = (u^1, \cdots, u^n)$ with
$\displaystyle u^{i} = \frac{x^j}{1\pm x^0}.$

Writing $u = (u^1,\dots,u^n)$, the transition functions are given by,
$$(\phi_- \circ \phi_+^{-1})(u) = \frac{u}{||u||^2}.$$

### Products and n-torus

Given manifolds $M,M'$ of dimensions $m,m'$, with atlases
$\{(U_\alpha,\phi_\alpha) \}$ and $\{(U_\beta,\phi_\beta)\}$, the
cartesian product $M \times M'$ is a manifold of dimension $m + m'$. An
atlas is given by the product charts $U_\alpha \times U_\beta$ with the
product maps
$\phi_\alpha \times \phi_\beta' : (x, x') \mapsto (\phi_\alpha(x), \phi_\beta'(x'))$.
For example, the 2-torus $T^2 = S^1 \times S^1$ becomes a manifold in
this way, and likewise for the n-torus,
$T^n = S^1 \times \dots \times S^1$.

### Real projective spaces

The n-dimensional projective space $\mathbb R P^n$, is the set of all
lines $l \subseteq \mathbb R^{n+1}$. It may also be regarded as a
quotient space,
$$\mathbb R P^n  = (\mathbb R^{n+1} \setminus \{0\}) / \sim$$
$\mathbb R P^n$ has a standard atlas,
$\mathscr{A} =  {(U_0,\phi_0),\dots,(U)n,\phi_n)}$ defined as follows.
For $j = 0,\dots,n,$ let
$U_j = \{(x^0 : \dots : x^n) \in \mathbb R P^n | x^j \neq 0\}$ be the
set for which the j-th coordinate is non-zero, and put
$$\phi_j : U_j \rightarrow \mathbb R^n, (x^0 : \dots : x^n ) \mapsto \bigg ( \frac{x^0}{x^j} ,\dots, \frac{x^n}{x^j} \bigg).$$

Geometrically, viewing $\mathbb RP^n$ as the set of lines in
$\mathbb R^{n+1}$, the subset $U_j \subseteq \mathbb RP^n$ consists of
those lines $l$ which intersect the affine hyperplane
$H_j = \{x \in \mathbb R^{n+1} | x^j = 1\}$ and the map $\phi_j$ takes
such a line $l$ to its unique point of intersection $l \cap H_j$,
followed by the identification $H_j \cong  \mathbb R^n$ (dropping the
coordinate $x^j = 1$). In low dimensions, we have that $\mathbb RP^0$ is
just a point, while $\mathbb RP^1$is a circle.

### Complex projective spaces

Similar to the real projective space, one can define a complex
projective space $\mathbb C P^n$ as the set of complex 1-dimensional
subspaces of $\mathbb C^{n+1}$.
$$\mathbb C P^n = (\mathbb C^{n+1} \setminus \{0\})/ \sim$$
Alternatively, letting
$S^{2n+1} \subseteq \mathbb C^{n+1} = \mathbb R^{2n+2}$ be the 'unit
sphere' consisting of complex vectors of length $||z|| = 1$, we have
$$\mathbb C P^n = S^{2n+1} / \sim$$ One defines charts $(U_j ,\phi_j)$
similar to those for the real projective space: $$\begin{aligned}
    U_j &= \{(z^0 : \dots : z^n) | z^j \neq 0\} \\
    \phi_j : U_j \rightarrow \mathbb C^{2n},& \ \ (z^0 : \dots : z^n ) \mapsto \bigg ( \frac{z^0}{z^j} ,\dots, \frac{z^n}{z^j} \bigg).\end{aligned}$$
The transition maps between charts are given by similar formulas as for
$\mathbb RP^n$ (just replace $x$ with $z$). The transition maps are not
only smooth but even *holomorphic*, making $\mathbb C P^n$ an example of
a complex manifold (of complex dimension $n$).

### Grassmannians

The set $Gr(k,n)$ of all $k$-dimensional subspaces of $\mathbb R^n$ is
called the Grassmannian of $k$-planes in $\mathbb R^n$. As a special
case, $Gr(1,n) = \mathbb RP^{n-1}$. We will show that for general $k$,
the Grassmannian is a manifold of dimension $dim(Gr(k,n)) = k(n-k)$.
\[Omitted\]

### Complex Grassmannians

Similar to the case of projective spaces, one can also consider the
complex Grassmannian $Gr \mathbb C(k,n)$ of complex $k$-dimensional
subspaces of $\mathbb C^n$ . It is a manifold of dimension $2k(n-k)$,
which can also be regarded as a complex manifold of complex dimension
$k(n-k)$.

## Oriented manifolds

The notion of an orientation on a manifold will become crucial later,
since integration of differential forms over manifolds is only defined
if the manifold is oriented.

::: {.defn}
**Definition 15**. **(Oriented atlas and manfold)**

The compatibility condition between charts $(U,\phi),(V,\psi)$ on a set
$M$ is that the change of coordinates map $\phi \circ \psi^{-1})$ is a
diffeomorphism. In particular, the Jacobian matrix
$D(\phi \circ \psi^{-1}))$ of the transition map is invertible, and
hence has non-zero determinant. If the determinant is $> 0$ everywhere,
then we say $(U,\phi),(V,\psi)$ are *oriented-compatible*. An *oriented
atlas* on $M$ is an atlas such that any two of its charts are
oriented-compatible; a *maximal oriented atlas* is one that contains
every chart that is oriented-compatible with all charts in this atlas.
An *oriented manifold* is a set with a maximal oriented atlas,
satisfying the Hausdorff and countability conditions. A manifold is
called orientable if it admits an oriented atlas.
:::

The spheres $S^n$ are orientable. To see this, consider the atlas with
the two charts given by stereographic projections. The Jacobian matrix
$D(\phi_-, \psi^{-1})_+)(u)$ has determinant of $-||u||^{-2n}$ which is
not an oriented atlas. To remedy this, simply compose one of the charts,
with the map $(u_1,u_2,\dots,u_n) \mapsto (-u_1,u_2,\dots,u_n)$; then
with the resulting new coordinate map $\Tilde{\phi}_-$ the atlas
$(U_+,\phi_+),(U_-,\Tilde{\phi}_-)$ will be an oriented atlas.

One can show that the real projective space $\mathbb R P^n$ is
orientable if and only if $n$ is odd or $n = 0$. More generally, the
Grassmannians space $Gr(k,n)$ is orientable if and only if $n$ is even
or $n = 1$. The complex projective spaces $\mathbb C P^n$ and complex
Grassmannians $Gr \mathbb C(k,n)$ are all orientable. This follows
because the transition maps for their standard charts, as maps between
open subsets of $\mathbb C^m$, are actually complex-holomorphic, and
this implies that as real maps, their Jacobian has positive determinant.

## Open subsets

Let $M$ be a set equipped with an $m$-dimensional maximal atlas
$\mathscr{A} =  \{(U_\alpha, \phi_\alpha) \}$.

::: {.defn}
**Definition 16**. **(Open subset)**

A subset $U \subseteq M$ is open if and only if for all charts
$(U_\alpha, \phi_\alpha) \in \mathscr{A}$ the set
$\phi_\alpha(U  \cap U_\alpha)$ is open.
:::

::: {.proposition}
**Proposition 1**. *Given $U \subseteq M$, let
$\mathscr{B} \subseteq \mathscr{A}$ be any collection of charts whose
union contains $U$. Then $U$ is open if and only if for all charts
$(U_\beta,\phi_\beta)$ from $\mathscr{B}$, the sets
$\phi_{\beta}(U \cap U_\beta)$ are open.*
:::

This means that to check that a subset $U$ is open, it is not actually
necessary to verify this condition for all charts. As the above
proposition shows, it is enough to check for any collection of charts
whose union contains $U$. In particular, we may take $\mathscr{A}$ to be
any atlas, not necessarily a maximal atlas.

If $\mathscr{A}$ is an atlas on $M$, and $U \subseteq M$ is open, then
$U$ inherits an atlas by restriction:
$$\mathscr{A}  = \{ (U \cap U_\alpha, \phi_\alpha |_{U \cap U_\alpha } ) \}$$

::: {.proposition}
**Proposition 2**. *An open subset of a manifold is again a manifold.*
:::

::: {.proposition}
**Proposition 3**. *Let $M$ be a set with an $m$-dimensional maximal
atlas. The collection of all open subsets of M has the following
properties*

1.  *$\emptyset, M$ are open.*

2.  *The intersection $U \cap U'$ of any two open sets $U,U'$ is again
    open.*

3.  *The union $\cap_i U_i$ of an arbitrary collection $U_i, i \in I$ of
    open sets is again open.*
:::

These properties mean, by definition, that the collection of open
subsets of $M$ define a *topology* on $M$. This allows us to adopt
various notions from topology:

1.  A subset $A \subseteq M$ is called *closed* if its complement
    $M \setminus A$ is open.

2.  $M$ is called *connected* if the only subsets $A \subseteq M$ that
    are both closed and open are $A = \emptyset$ and $A = M$.

3.  If $U$ is an open subset and $p \in U$, then $U$ is called an open
    neighborhood of $p$. More generally, if $A \subseteq U$ is a subset
    contained in $M$, then $U$ is called an *open neighborhood* of $A$.

The Hausdorff condition in the definition of manifolds can now be
restated as the condition that any two distinct points $p,q \in M$ have
disjoint open neighborhoods. (It is not necessary to take them to be
domains of coordinate charts.) It is immediate from the definition that
domains of coordinate charts are open. Indeed, this gives an alternative
way of defining the open sets.

## Compact subsets

Another important concept from topology that we will need is the notion
of *compactness*.

::: {.defn}
**Definition 17**. **(Compactness)**

A subset $A \subseteq \mathbb R^m$ is compact if it has the following
property: For every collection ${U_\alpha}$ of open subsets of $R^m$
whose union contains $A$, the set $A$ is already covered by finitely
many subsets from that collection.
:::

In short, $A \subseteq M$ is compact if every open cover admits a finite
subcover.

::: {.theorem}
**Theorem 18**. ***(Heine-Borel)***

*A subset $A \subseteq R^m$ is compact if and only if it is closed and
bounded.*
:::

::: {.proposition}
**Proposition 4**. *If $A \subseteq M$ is contained in the domain of a
coordinate chart $(U,\phi)$, then $A$ is compact in $M$ if and only if
$\phi(A)$ is compact in $R^n$.*
:::

The proposition is useful, since we can check compactness of $\phi(A)$
by using the Heine-Borel criterion. For more general subsets of $M$, we
can often decide compactness by combining this result with the
following:

::: {.proposition}
**Proposition 5**. *If $A_1,\dots,A_k \subseteq M$ is a finite
collection of compact subsets, then their union
$A = A_1 \cap \dots \cap A_k$ is again compact.*
:::

A simpler way of verifying compactness is by showing that they are
closed and bounded subsets of $\mathbb R^N$ for a suitable $N$.

::: {.proposition}
**Proposition 6**. *Let $M$ be a set with a maximal atlas. If
$A \subseteq M$ is compact, and $C \subseteq M$ is closed, then
$A \cap C$ is compact.*
:::

::: {.proposition}
**Proposition 7**. *If $M$ is a manifold, then every compact subset
$A \subseteq M$ is closed.*
:::

# Smooth Maps

## Smooth functions on manifolds

The notion of smooth functions on open subsets of Euclidean spaces
carries over to manifolds: A function is smooth if its expression in
local coordinates is smooth,

::: {.defn}
**Definition 19**. **(Smoothness)**

A function $f : M \rightarrow R$ on a manifold $M$ is called smooth if
for all charts $(U,\phi)$ the function
$$f \circ\phi^{-1}: \phi(U) \rightarrow \mathbb{R}$$ is smooth. The set
of smooth functions on $M$ is denoted $C^{\infty}(M)$.
:::

Since transition maps are diffeomorphisms, it suffices to check the
condition for the charts from any given atlas which need not be the
maximal atlas.

Given an open subset $U \subseteq M$, we say that a function $f$ is
smooth on $U$ if its restriction $f |_U$ is smooth. (Here we are using
that $U$ itself is a manifold.) Given $p \in M$, we say that $f$ is
smooth at $p$ if it is smooth on some open neighborhood of $p$.

::: {.lemma}
**Lemma 20**. *Smooth functions $f \in C^{\infty}(M)$ are continuous:
For every open subset $J \subseteq \mathbb R$, the pre-image
$f^{-1}(J) \subseteq M$ is open.*
:::

From the properties of smooth functions on $\mathbb R^m$, one
immediately gets the following properties of smooth functions on
manifolds $M$:

1.  If $f,g \in C^{\infty}(M)$ and $\lambda, \mu \in \mathbb R$, then
    $\lambda f + \mu g \in C^\infty(M)$.

2.  If $f,g \in C^\infty(M)$, then $f g \in C^\infty(M)$.

3.  $1 \in C^{\infty}(M)$ (where $1$ denotes the constant function
    $p \mapsto 1$)

These properties say that $C^{\infty}(M)$ is an *algebra* with unit 1.

::: {.proposition}
**Proposition 8**. *Suppose $M$ is any set with a maximal atlas, and
$p \neq q$ are two points in $M$. Then the following are equivalent:*

1.  *There are open subsets $U,V \subseteq M$ with
    $p \in U, q \in V, U \cap V = \emptyset$*

2.  *There exists $f \in C^\infty(M)$ with $f(p) \neq f(q)$.*
:::

::: {.corollary}
**Corollary 1**. ***(Criterion for Haudorff condition)***

*A set $M$ with an atlas satisfies the Hausdorff condition if and only
if for any two distinct points $p,q \in M$, there exists a smooth
function $f \in C^\infty(M)$ with $f(p) \neq f(q)$. In particular, if
there exists a smooth injective map $F : M \rightarrow \mathbb R^N$,
then $M$ is Hausdorff.*
:::

## Smooth maps between manifolds

::: {.defn}
**Definition 21**. A map $F : M \rightarrow N$ between manifolds is
smooth at $p \in M$ if there are coordinate charts $(U,\phi)$ around $p$
and $(V,\psi)$ around $F(p)$ such that $F(U) \subseteq V$ and such that
the composition
$$\psi \circ F \circ \phi^{-1}: \phi(U) \rightarrow \psi(V)$$ is smooth.
The function $F$ is called a smooth map from $M$ to $N$ if it is smooth
at all $p \in M$.
:::

The condition for smoothness at p does not depend on the choice of
charts. To check smoothness of $F$, it suffices to take any atlas of M
with the property that $F(U_\alpha) \subseteq V_\alpha$ and then check
smoothness of the maps. Smooth maps $M \rightarrow R$ are the same thing
as smooth functions on $M$, $C^{\infty} (M,R) = C^{\infty}(M)$.

::: {.proposition}
**Proposition 9**. *Suppose $F_1 : M_1 \rightarrow M_2$ and
$F_2 : M_2 \rightarrow M_3$ are smooth maps. Then the composition
$F_2 \circ F_1 : M_1 \rightarrow M_3$ is smooth.*
:::

## Diffeomorphisms of manifolds

::: {.defn}
**Definition 22**. **(Diffeomorphic manifolds)**

A smooth map $F : M \rightarrow N$ is called a *diffeomorphism* if it is
invertible, with a smooth inverse $F^{-1} : N \rightarrow M$. Manifolds
$M,N$ are called diffeomorphic if there exists a diffeomorphism from $M$
to $N$.
:::

In other words, a diffeomorphism of manifolds is a bijection of the
underlying sets that identifies the maximal atlases of the manifolds.
Manifolds that are diffeomorphic are therefore considered 'the same
manifolds'.

::: {.defn}
**Definition 23**. **(Homeomorphic manifolds)** A continuous map
$F : M \rightarrow N$ is called a *homeomorphism* if it is invertible,
with a continuous inverse. Manifolds $M,N$ are called homeomorphic if
there exists a homeomorphism from $M$ to $N$.
:::

Manifolds that are homeomorphic are considered 'the same topologically'.
Since every smooth map is continuous, every diffeomorphism is a
homeomorphism.

::: {.example}
**Example 24**. The standard example of a homeomorphism of smooth
manifolds that is not a diffeomorphism is the map
$\mathbb R \rightarrow \mathbb R, x \mapsto x^3$. Indeed, this map is
smooth and invertible, but the inverse map $y \mapsto y ^{\frac{1}{3}}$
is not smooth.
:::

It is quite possible for two manifolds to be homeomorphic but not
diffeomorphic, these are known as *exotic manifolds*. An *exotic sphere*
is homeomorphic but not diffeomorphic to the standard Euclidean
n-sphere. It is known that there are no exotic manifold structures on
$\mathbb R^n$ for $\mathbb R^n$ with $n \neq 4$, where there are
uncountably many such.

## Examples of smooth maps

### Products, diagonal maps

1.  If $M,N$ are manifolds, then the projection maps are smooth. Take
    product charts $U_\alpha \times V_\beta$.
    $$p^{T}_M : M \times N  \rightarrow M, \ \
            p^{T}_N :  M \times N \rightarrow N$$

2.  The diagonal inclusion is smooth. In a coordinate chart around a
    point, the map is the restriction to a subset of the diagonal
    inclusion. $$\Delta_M : M \rightarrow  M \times M$$

3.  Suppose $F : M \rightarrow N$ and $F' : M' \rightarrow N'$ are
    smooth maps. Then the direct product is smooth.
    $$F \times F' : M \times M' \rightarrow N \times N'$$

### The diffeomorphism $\mathbb R P^1 \cong S^1$ 

We have seen that $\mathbb R P^1 \cong S^1$. To obtain a diffeomorphism,
we construct a bijection between the standard atlases of both of the
manifolds described previously

### The diffeomorphism $\mathbb C P^1 \cong S^2$

By a similar reasoning, we find $\mathbb C P^1 \cong S^2$. For $S^2$ we
use the atlas given by stereographic projection. Regarding $u$ as a
complex number the normis just the absolute value of $u$, and the
transition map becomes $u \mapsto \frac{1}{u}$. Note that it is not
quite the same as the transition map for the standard atlas of
$\mathbb C P^1$, which is given by $u \mapsto u^{-1}$. We obtain a
unique diffeomorphism such that $\phi_+ \circ F \circ \phi_0^{-1}$ is
the identity and $\phi_- \circ F \circ \phi_1^{-1}$ is complex
conjugation

### Maps to and from projective space

The quotient map $\pi$ is smooth, as one verifies by checking in the
standard atlas for $\mathbb R P^n$.
$$\pi : \mathbb R^{n+1} \setminus \{0\} \rightarrow \mathbb R P^N, \ \ 
    x = (x^0, \dots, x^n) \mapsto (x^0, \dots, x^n)$$ Given a map
$F : \mathbb R P^n \rightarrow N$ to a manifold $N$, let
$\Tilde{F} = F \circ \pi : \mathbb R ^{n+1}\setminus \{0\} \rightarrow N$
be its composition with the projection map
$\pi : \mathbb R ^{n+1}\setminus \{0\} \rightarrow \mathbb R P^n$. That
is, $\Tilde{F} (x^0 , \dots, x^n ) = F(x^0 : \dots : x^n )$.

We claim that the map $F$ is smooth if and only the corresponding map
$\Tilde{F}$ is smooth. One direction is clear: If $F$ is smooth, then
$\Tilde{F} = F \circ \pi$ is a composition of smooth maps. For the other
direction, assuming that $\Tilde{F}$ is smooth, note that for the
standard chart $(U_j ,\phi_j)$, and the maps
$$(F \circ \phi^{-1}_j )(u^1 ,\dots, u^n ) = \Tilde{F}(u^1 ,\dots, u^i ,1,u ^{i+1} ,\dots,u^n ),$$
are smooth. An analogous argument applies to the complex projective
space $\mathbb C P^n$ , taking the $x^i$ to be complex numbers $z^i$

### The Hopf fibration, a.k.a. the quotient map $S^{2n+1} \rightarrow \mathbb C P^n$

As mentioned above, quotient map
$q : C^{n+1} \setminus \{0\} \rightarrow \mathbb C P^n$ is smooth. Since
any class $[z] = (z 0 : \dots : z^n )$ has a representative with
$|z^0|^2 + \dots +|z^n|^2 = 1$, and $|z^i|^2 = (x^i)^2 + (y^i)^2$ for
$z^i = x^i + \sqrt{-1}y^i$, we may also regard $\mathbb C P^n$ as a set
of equivalence classes in the unit sphere
$S^{2n+1} \subseteq \mathbb R^{2n+2} = \mathbb C^{n+1}$. The resulting
quotient map $$\pi : S^{2n+1} \rightarrow \mathbb C P^n$$ is again
smooth, because it can be written as a composition of two smooth maps
$\pi = q \circ \tau$ where
$\tau : S ^{2n+1} \mapsto \mathbb R^{2n+2} \setminus \{0\} = \mathbb C^{n+1} \setminus \{0\}$
is the inclusion map.

For any $p \in \mathbb C P^n$ , the corresponding fiber
$\pi^{-1} (p) \subset S^{2n+1}$ is diffeomorphic to a circle $S^1$
(which we may regard as complex numbers of absolute value 1). Indeed,
given any point $(z^0 , \dots ,z^n ) \in \pi^{-1} (p)$ in the fiber, the
other points are obtained as $(\lambda z^0 ,\dots, \lambda z^n )$ where
$|\lambda| = 1$.

In other words, we can think of
$$S^{2n+1} = \bigcup_{p \in \mathbb C P^n} \pi^{- 1}(p)$$ as a union of
circles, parametrized by the points of $\mathbb C P^n$. This is an
example of a *fiber bundle* or *fibration*.

An import important case occurs when $n = 1$. Identifying
$\mathbb C P^1 \cong  S^2$ as above, the map $\pi$ becomes a smooth map
$\pi : S^3 \rightarrow S^2$ with fibers diffeomorphic to $S^1$. This map
appears in many contexts; it is called the *Hopf fibration*.

Let $S \in S^3$ be the 'south pole', and $N \in S^3$ the 'north pole'.
We have that $S^3 - \{S\} \cong R^3$ by stereographic projection. The
set $\pi^{-1} (\pi(S)) -  \{S\}$ projects to a straight line (think of
it as a circle with 'infinite radius'). The fiber $\pi ^{-1} (N)$ is a
circle that goes around the straight line. If $Z \subseteq S^2$ is a
circle at a given 'latitude', then $\pi^{-1} (Z)$ is is a 2-torus. For
$Z$ close to north pole $N$ this 2-torus is very thin, while for $Z$
approaching the south pole $S$ the radius goes to infinity. Each such
2-torus is itself a union of circles $\pi^{-1} (p), p \in Z$. Those
circles are neither the usual 'vertical' or 'horizontal' circles of a
2-torus in $\mathbb R^3$ , but instead are 'tilted'. In fact, each such
circle is a 'perfect geometric circle' obtained as the intersection of
its 2-torus with a carefully positioned affine 2-plane. Moreover, any
two of the circles $\pi^{-1} (p)$ are 'linked' as though they were in a
chain.

A calculation shows that over the charts $U_+,U_-$ from stereographic
projection, the Hopf fibration is just a product. That is, one has
$$\pi^{-1} (U_+) \cong U_+ \times S^1, \ \ \pi^{-1} (U_-) \cong U_- \times S^1$$
In particular, the pre-image of the closed upper hemisphere is a solid
2-torus $D^2 \times S^1$ (with $D^2 = \{ z \in \mathbb C| |z| \leq 1 \}$
the unit disk), geometrically depicted as a 2-torus in $\mathbb R^3$
together with its interior. We hence see that the $S^3$ may be obtained
by gluing two solid 2-tori along their boundaries $S^1 \times S^1$.

## Submanifolds

::: {.defn}
**Definition 25**. A subset $S \subseteq M$ is called a *submanifold* of
dimension $k \leq m$, if for all $p \in S$ there exists a coordinate
chart $(U,\phi)$ around $p$ such that
$$\phi(U \cap S) = \phi(U) \cap \mathbb R^k .$$ Charts $(U,\phi)$ of $M$
with this property are called submanifold charts for $S$.
:::

::: {.defn}
**Definition 26**. A chart $(U, \phi)$ such that $U \cap S = \emptyset$
and $\phi (U) \cap \mathbb R^k = \emptyset$ is considered a *submanifold
chart*. The existence of submanifold charts is only required for points
$p$ that lie in $S$.
:::

Strictly speaking, a submanifold chart for $S$ is not a chart for $S$,
but is a chart for $M$ which is adapted to $S$. Submanifold charts
restrict to charts for $S$, and this may be used to construct an atlas
for $S$.

::: {.proposition}
**Proposition 10**. *Suppose $S$ is a submanifold of $M$. Then $S$ is a
$k$-dimensional manifold in its own right, with atlas consisting of all
charts $(U \cap S, \phi|U \cap S)$ such that $(U,\phi)$ is a submanifold
chart.*
:::

::: {.example}
**Example 27**. (Open subsets). The $m$-dimensional submanifolds of an
$m$-dimensional manifold are exactly the open subsets.
:::

::: {.example}
**Example 28**. (Projective spaces). For $k < n$, regard
$\mathbb R P^k \subseteq \mathbb R P^n$ as the subset of all
$(x^0 : \dots : x^n )$ for which $x^{k+1} = \dots = x^n = 0$. These are
submanifolds, with the standard charts $(U_i ,\phi_i)$ for
$\mathbb R P^n$ as submanifold charts. Similarly,
$\mathbb C P^k \subseteq \mathbb C P^n$ are submanifolds, and for
$n < n'$ we have $Gr(k,n) \subseteq Gr(k,n')$ as a submanifold.
:::

::: {.example}
**Example 29**. (Spheres). For $k < n$, regard $S^k \subseteq S^n$ as
the subset where the last $n-k$ coordinates are zero. These are
submanifolds where the charts for $S^n$ given by stereographic
projection are submanifold charts.
:::

::: {.proposition}
**Proposition 11**. *Let $F : M \rightarrow N$ be a smooth map between
manifolds of dimensions $m$ and $n$. Then
$$graph(F) = \{(F(p), p) | p \in M \} \subseteq N \times M$$ is a
submanifold of $N \times M$, of dimension equal to the dimension of
$M$.*

*This result has the following consequence: If a subset of a manifold,
$S \subseteq M$, can be locally described as the graph of a smooth map,
then $S$ is a submanifold.*
:::

::: {.proposition}
**Proposition 12**. *The inclusion map
$i : S \rightarrow M, p \mapsto p,$ which takes any point of $S$ to the
same point but viewed as a point of $M$, is smooth.*
:::

::: {.proposition}
**Proposition 13**. *Suppose $S$ is a submanifold of $M$. Then the open
subsets of $S$ for its manifold structure are exactly those of the form
$U \cap S$, where $U$ is an open subset of $M$.*
:::

In other words, the topology of $S$ as a manifold coincides with the
'subspace topology' as a subset of the manifold $M$.

As a consequence, if a manifold $M$ can be realized realized as a
submanifold $M \subseteq \mathbb R^n$, then $M$ is compact with respect
to its manifold topology if and only if it is compact as a subset of
$R^n$, if and only if it is a closed and bounded subset of
$\mathbb R^n$.

## Smooth maps of maximal rank

Let $F \in C^\infty(M,N)$ be a smooth map. Then the fibers (level sets)
$F^{-1}(q) = \{x \in M| F(x) = q\}$ for $q \in N$ need not be
submanifolds, in general.

### The rank of a smooth map

Let $U \subseteq \mathbb R^m$ and $V \subseteq \mathbb R^n$ be open
subsets, and $F \in  C^\infty(U,V)$ a smooth map.

::: {.defn}
**Definition 30**. The *derivative* of $F$ at $p \in U$ is the linear
map
$$D_pF : \mathbb R^m \rightarrow \mathbb R^n, \ \ v \mapsto \frac{d}{dt}\Bigr|_{\substack{ t=0 }} F(p+tv).$$

Recall that the *rank* of a linear map is the dimension of its range.
The rank of $F$ at $p$ is the rank of this linear map:
$$\text{rank}_p(F) = \text{rank}(D_p F).$$
:::

Equivalently, $D_p F$ is the $n \times m$ matrix of partial derivatives
and the rank of $F$ at $p$ is the rank of this matrix i.e., the number
of linearly independent rows or the number of linearly independent
columns.

::: {.defn}
**Definition 31**. Let $F \in C^\infty(M,N)$ be a smooth map between
manifolds, and $p \in M$. The rank of $F$ at $p \in M$ is defined as
$$\text{rank}_p(F) = \text{rank}_{\phi(p)}(\psi \circ F \circ \phi^{-1}).$$
for any two coordinate charts $(U,\phi)$ around $p$ and $(V,\psi)$
around $F(p)$ such that $F(U) \subseteq V$.
:::

::: {.defn}
**Definition 32**. The map $F$ is said to have *maximal rank* at $p$ if
$$\text{rank}_p(F) = \text{min}(\text{dim} M, \text{dim} N).$$ A point
$p \in M$ is called a *critical point* for $F$ if
$\text{rank}_p(F) < \text{min}(\text{dim} M, \text{dim} N)$.
:::

### Local diffeomorphisms

::: {.theorem}
**Theorem 33**. *(Inverse Function Theorem for $\mathbb R^m$).*

*Let $F \in C^\infty(U,V)$ be a smooth map between open subsets of
$\mathbb R^m$, and suppose that the derivative $D_pF$ at $p \in U$ is
invertible. Then there exists an open neighborhood $U_1 \subseteq U$ of
$p$ such that $F$ restricts to a diffeomorphism
$U_1 \rightarrow F(U_1)$.*
:::

The theorem tells us that for a smooth bijection, a sufficient condition
for smoothness of the inverse map is that the differential (i.e., the
first derivative) is invertible everywhere.

::: {.theorem}
**Theorem 34**. *(Inverse function theorem for manifolds)*

*Let $F \in C^\infty(M,N)$ be a smooth map between manifolds of the same
dimension $m = n$. If $p \in M$ is such that $\text{rank}_p(F) = m$,
then there exists an open neighborhood $U \subseteq M$ of $p$ such that
$F$ restricts to a diffeomorphism $U \rightarrow F(U)$.*
:::

A smooth map $F \in C^\infty(M,N)$ is called a local diffeomorphism if
$\text{dim} M = \text{dim}N$, and $F$ has maximal rank everywhere. By
the theorem, this is equivalent to the condition that every point $p$
has an open neighborhood $U$ such that $F$ restricts to a diffeomorphism
$U \rightarrow F(U)$.

### Level sets, submersions

::: {.proposition}
**Proposition 14**. *Suppose $F \in C^\infty(U,V)$ is a smooth map
between open subsets $U \subseteq R^m$ and $V \subseteq R^n$, and
suppose $p \in U$ is such that the derivative $D_p F$ is surjective.
Then there exists an open neighborhood $U_1 \subseteq U$ of $p$ and a
diffeomorphism
$\kappa : U_1 \rightarrow \kappa (U_1) \subseteq \mathbb R^m$ such that
$$(F \circ \kappa - 1)(u^1, \dots, u^m) = (u^{m-n+1},\dots,u^m)$$*

*for all $u = (u^1 ,\dots,u^m) \in \kappa(U_1)$.*
:::

Again, this result has a version for manifolds:

::: {.theorem}
**Theorem 35**. *Let $F \in C ^\infty(M,N)$ be a smooth map between
manifolds of dimensions $m \geq n$, and suppose $p \in M$ is such that
$\text{rank}_p(F) = n$. Then there exist coordinate charts $(U,\phi)$
around $p$ and $(V,\psi)$ around $F(p)$, with $F(U) \subseteq V$, such
that $$(\psi \circ F \circ \phi^{-1} )(u' ,u'') = u''$$ for all
$u = (u',u'') \in \phi(U)$. In particular, for all $q \in V$ the
intersection $F^{-1} (q)\cap U$ is a submanifold of dimension $m-n$.*
:::

::: {.defn}
**Definition 36**. Let $F \in C^\infty(M,N)$. A point $q \in N$ is
called a *regular value* of $F \in C^\infty(M,N)$ if for all
$x \in F^{-1} (q)$, one has $\text{rank}_x(F) = \text{dim}N$. It is
called a *singular value* if it is not a regular value.
:::

Note that regular values are only possible if
$\text{dim}N \leq \text{dim}M$. Note also that all points of $N$ that
are not in the image of the map F are considered regular values. We may
restate the theorem as follows:

::: {.theorem}
**Theorem 37**. *For any regular value $q \in N$ of a smooth map
$F \in C^\infty(M,N)$, the level set $S = F^{-1}(q)$ is a submanifold of
dimension $\text{dim}S = \text{dim}M - \text{dim}N$.*
:::

::: {.defn}
**Definition 38**. A smooth map $F \in C^\infty(M,N)$ is a *submersion*
if $\text{rank}_p(F) = \text{dim}N$ for all $p \in M$.

Thus, for a submersion all level sets $F^{-1} (q)$ are submanifolds.
:::

::: {.example}
**Example 39**. Recall that $\mathbb CP^n$ can be regarded as a quotient
of $S^{2n+1}$. Using charts, one can check that the quotient map
$\pi : S^{2n+1} \rightarrow \mathbb C P^n$ is a submersion. Hence its
fibers $\pi^-1 (q)$ are 1-dimensional submanifolds. As discussed before
these fibers are circles. As a special case, the Hopf fibration
$S^3 \rightarrow S^2$ is a submersion.
:::

::: {.example}
**Example 40**. Let $\mathbb H = \mathbb C^2 = \mathbb R^4$ be the
*quaternionic numbers*. The unit quaternions are a 3-sphere $S^3$ .
Generalizing the definition of $\mathbb R P^n$ and $\mathbb C P^n$,
there are also quaternionic projective spaces, $\mathbb H P^n$. These
are quotients of the unit sphere inside $\mathbb H^{n+1}$ , hence one
obtains submersions $$S^{4n+3} \mapsto \mathbb H P^n;$$ the fibers of
this submersion are diffeomorphic to $S^3$. For $n = 1$, one can show
that $\mathbb HP^1 = S^4$, hence one obtains a submersion
$\pi : S^7 \rightarrow S^4$ with fibers diffeomorphic to $S^3$.
:::

### Example: The Steiner surface

\[Omitted\]

### Immersions

::: {.proposition}
**Proposition 15**. *Suppose $F \in C^\infty(U,V)$ is a smooth map
between open subsets $U \subseteq \mathbb R^m$ and
$V \subseteq \mathbb R^n$, and suppose $p \in U$ is such that the
derivative $D_p F$ is injective. Then there exist smaller neighborhoods
$U_1 \subseteq U$ of $p$ and $V_1 \subseteq V$ of $F(p)$, with
$F(U_1) \subseteq V_1$, and a diffeomorphism
$\chi : V_1 \rightarrow \chi(V_1)$, such that
$(\chi \circ F)(u) = (u,0) \in R^m \times R^{n-m}$*
:::

The manifolds version reads as follows:

::: {.theorem}
**Theorem 41**. *Let $F \in C^\infty(M,N)$ be a smooth map between
manifolds of dimensions $m \infty n$, and $p \in M$ a point with
$\text{rank}_p(F) = m$. Then there are coordinate charts $(U,\phi)$
around $p$ and $(V,\psi)$ around $F(p)$ such that $F(U) \subseteq V$ and
$$(\psi \circ F \circ \phi{-1})(u) = (u,0).$$*

*In particular, $F(U) \subseteq N$ is a submanifold of dimension $m$.*
:::

::: {.defn}
**Definition 42**. A smooth map $F : M \mapsto N$ is an immersion if
$\text{rank}_p(F) = \text{dim}M$ for all $p \in M$.
:::

::: {.theorem}
**Theorem 43**. *If $M$ is a compact manifold, then every injective
immersion $F : M \rightarrow N$ is an embedding as a submanifold
$S = F(M)$. By an embedding, we will mean an immersion given as the
inclusion map for a submanifold.*
:::

# The Tangent Bundle

For embedded submanifolds $M \subseteq \mathbb R^n$, the tangent space
$T_p M$ at $p \in M$ can be defined as the set of all velocity vectors
$v = \gamma(0$), where $\gamma : J \rightarrow M$ is a smooth curve with
$\gamma(0) = p$; here $J \subseteq R$ is an open interval around $0$. It
turns out that $T_pM$ becomes a vector subspace of $\mathbb R^n$. For a
general manifold, we will define $T_pM$ as a set of directional
derivatives.

::: {.defn}
**Definition 44**. (Tangent spaces - first version)

Let $M$ be a manifold, $p \in M$. The *tangent space* $T_pM$ is the set
of all linear maps $v : C^{\infty}(M) \rightarrow \mathbb R$ of the form
$$v(f) = \frac{d}{dt}\Bigr|_{\substack{ t=0 }}  f(\gamma(t))$$ for some
smooth curve $\gamma \in C^\infty(J,M)$ with $\gamma(0) = p$.

The elements $v \in T_pM$ are called the *tangent vectors* to $M$ at
$p$.
:::

The following local coordinate description makes it clear that $T_pM$ is
a linear subspace of the vector space $L(C^\infty(M),R)$ of linear maps
$C^\infty(M) \rightarrow R$, of dimension equal to the dimension of $M$.

::: {.theorem}
**Theorem 45**. *Let $(U,\phi)$ be a coordinate chart around $p$. A
linear map $v : C^\infty(M) \rightarrow \mathbb R$ is in $T_pM$ if and
only if it has the form,
$$v(f) = m \sum_{i=1}^m a^i \frac{\partial (f \circ \phi^{-1} )}{ \partial u^i}\Bigr|_{u = \phi(p)}$$
for some $a = (a^1 ,\dots,a^m) \in \mathbb R^m$*
:::

We can use this result as an alternative definition of the tangent
space, namely:

::: {.defn}
**Definition 46**. (Tangent spaces - second version)

Let $(U,\phi)$ be a chart around $p$. The tangent space $T_pM$ is the
set of all linear maps $v : C^\infty(M) \rightarrow \mathbb R$ of the
form
$$v(f) = m \sum_{i=1}^m a^i \frac{\partial (f \circ \phi^{-1} )}{ \partial u^i}\Bigr|_{u = \phi(p)}$$
for some $a = (a^1 ,\dots,a^m) \in \mathbb R^m$.
:::

It is not immediately obvious from this second definition that $T_pM$ is
independent of the choice of coordinate chart, but this follows from the
equivalence with the first definition. Any choice of coordinate chart
$(U,\phi)$ around $p$ defines a vector space isomorphism
$T_pM \cong \mathbb R^m$, taking $v$ to $a = (a^1 ,\dots,a^m)$. In
particular, we see that if $U \subseteq \mathbb R^m$ is an open subset,
and $p \in U$, then $T_pU$ is the subspace of the space of linear maps
$C^\infty(M) \rightarrow \mathbb R$ spanned by the partial derivatives
at $p$.

We now describe yet another approach to tangent spaces which again
characterizes "directional derivatives" in a coordinate-free way, but
without reference to curves $\gamma$. Note first that every tangent
vector satisfies the product rule, also called the Leibniz rule:

::: {.lemma}
**Lemma 47**. *(Leibniz rule)*

*Let $v \in T_pM$ be a tangent vector at $p \in M$. Then
$$v(f g) = f(p) v(g) +v(f)g(p)$$ for all $f,g \in C ^\infty(M)$.*
:::

Alternatively, in local coordinates it is just the product rule for
partial derivatives. It turns out that the product rule completely
characterizes tangent vector:

::: {.theorem}
**Theorem 48**. *A linear map $v : C^\infty(M) \rightarrow \mathbb R$
defines an element of $T_pM$ if and only if it satisfies the Leibniz
product rule.*
:::

::: {.defn}
**Definition 49**. (Tangent spaces - third version)

The tangent space $T_pM$ is the space of linear maps
$C^\infty(M) \rightarrow \mathbb R$ satisfying the product rule,
$$v(f g) = f(p)v(g) +v(f)g(p)$$ for all $f,g \in C^\infty(M)$.
:::

::: {.defn}
**Definition 50**. (Tangent Vectors)

The *velocity vectors* of curves are elements of the tangent space. Let
$J \subseteq \mathbb R$ be an open interval, and
$\gamma \in C^\infty(J,M)$ a smooth curve. Then for any $t_0 \in J$, the
tangent (or velocity) vector $\dot{\gamma}(t_0) \in T_{\gamma(t_0)}M$ at
time $t_0$ is given in terms of its action on functions by
$(\dot{\gamma}(t_0))(f) = \frac{d}{dt} \Bigr |_{t=t_0} f(\gamma(t))$. We
will also use the notation $\frac{d\gamma}{dt} \Bigr|_(t_0)$ or
$\frac{d\gamma}{dt} \Bigr |_{t_0}$ to denote the velocity vector.
:::

## Tangent map

### Definition of the tangent map, basic properties

The following definition generalizes the derivative to smooth maps
between manifolds.

::: {.defn}
**Definition 51**. Let $M,N$ be manifolds and $F \in C^\infty(M,N)$. For
any $p \in M$, we define the tangent map to be the linear map
$$T_pF : T_pM \rightarrow T_{F(p)}N$$ given by
$$(T_{p}F(v))(g) = v(g \circ F)$$ for $v \in T_pM$ and
$g \in C^\infty(N)$
:::

::: {.proposition}
**Proposition 16**. *If $v \in T_p M$ is represented by a curve
$\gamma : J \rightarrow M$, then $(T_pF)(v)$ is represented by the curve
$F\circ \gamma$.*
:::

::: {.defn}
**Definition 52**. (Pull-backs, push-forwards)

For smooth maps $F \in C^\infty(M,N)$, one can consider various
'pull-backs' of objects on $N$ to objects on $M$, and 'push-forwards' of
objects on $M$ to objects on $N$. Pull-backs are generally denoted by
$F^{*}$, push-forwards by $F_{*}$. For example, functions on $N$ pull
back, curves push forward on $M$, and tangent vectors to $M$ also push
forward.
:::

::: {.proposition}
**Proposition 17**. *(Chain rule) Let $M,N,Q$ be manifolds. Under
composition of maps $F \in C^\infty(M,N)$ and $F0 \in C^\infty(N,Q)$,
$$T_p(F'\circ F) = T_{F(p)} F' \circ T_pF.$$*
:::

### Coordinate description of the tangent map

::: {.proposition}
**Proposition 18**. *Let $F \in C^\infty(U,V)$ is a smooth map between
open subsets $U \subseteq \mathbb R^m$ and $V \subseteq \mathbb R^n$.
For all $p \in M$, the tangent map $T_pF$ is just the derivative (i.e.,
Jacobian matrix) $D_pF$ of $F$ at $p$.*
:::

Now that we have recognized $TpF$ as the derivative expressed in a
coordinate-free way, we may liberate some of our earlier definitions
from coordinates:

-   The rank of $F$ at $p \in M$, denoted $\text{rank}p(F)$, is the rank
    of the linear map $T_pF$.

-   $F$ has maximal rank at $p$ if
    $\text{rank}p(F) = min(dim M, dim N)$.

-   $F$ is a submersion if $T_pF$ is surjective for all $p \in M$,

-   $F$ is an immersion if $T_pF$ is injective for all $p \in M$,

-   $F$ is a local diffeomorphism if $T_pF$ is an isomorphism for all
    $p \in M$.

-   $p \in M$ is a critical point of $F$ is $T_pF$ does not have maximal
    rank at $p$.

-   $q \in N$ is a regular value of $F$ if $T_pF$ is surjective for all
    $p \in F^{-1} (q)$ (in particular, if $q \not\in F(M))$

-   $q \in N$ is a singular value if it is not a regular value.

## Tangent spaces of submanifolds

Suppose $S \subseteq M$ is a submanifold, and $p \in S$. Then the
tangent space $T_pS$ is canonically identified as a subspace of $T_pM$.
Indeed, since the inclusion $i : S \mapsto M$ is an immersion, the
tangent map is an injective linear map, $T_pi : T_pS \rightarrow T_pM$,
and we identify $T_pS$ with the subspace given as the image of this map.

Recall, the kernel of a linear mapping, also known as the null space or
nullspace, is the set of vectors in the domain of the mapping which are
mapped to the zero vector.

::: {.proposition}
**Proposition 19**. *Let $F \in C ^{\infty}(M,N)$ be a smooth map,
having $q \in N$ as a regular value, and let $S^\infty F^{-1} (q)$. For
all $p \in S$, $$T_pS = \ker(T_pF),$$ as subspaces of $T_pM$.*
:::

::: {.corollary}
**Corollary 2**. *Suppose $V \subseteq \mathbb R^n$ is open, and
$q \in \mathbb R^k$ is a regular value of
$F \in C^\infty(M, \mathbb R^k)$, defining an embedded submanifold
$M = F^{-1} (q)$. For all $p \in M$, the tangent space
$T_pM \subseteq T_p \mathbb R^n = \mathbb R^n$ is given as
$$T_p M = \ker(T_pF) \equiv \ker(D_pF).$$*
:::

::: {.example}
**Example 53**. Various matrix Lie Groups are submanifolds
$G \subseteq \text{Mat}_{\mathbb R}(n)$, consisting of invertible
matrices with the properties
$$A,B \in G \implies AB \in G, A \in G \implies A^{-1} \in G.$$

The tangent space to the identity (group unit) for such matrix Lie
groups $G$ turns out to be important; it is commonly denoted by lower
case Fraktur letters $\mathfrak {g} = T_I G$.

1.  The *matrix Lie group*
    $$GL(n,R) = \{A \in \text{Mat} \mathbb R(n) | \det(A) \neq 0 \}$$ of
    all invertible matrices is an open subset of
    $\text{Mat} \mathbb R(n)$, hence
    $$\mathscr{gl}(n,R) = \text{Mat} \mathbb R(n)$$ is the entire space
    of matrices.

2.  For the group $O(n)$, consisting of matrices with
    $F(A) := A ^T A = I$, we have computed $T_A F(X) = X^T A + AX ^T$.
    For $A = I$, the kernel of this map is
    $$\mathfrak{o}(n) = \{ X \in \text{Mat}_\mathbb R(n) | X = -X \}.$$

3.  For the *special linear group*
    $SL(n,R) = \{A \in \text{MatR}(n)| \det(A) = 1\}$, given as the
    level set $F^{-1}(1)$ of the function
    $\det : \text{Mat}_\mathbb R(n) \rightarrow R$, we calculate
    $$D_A F(X) = \frac{d}{dt} \Bigr |_{t=0} F(A+tX) =  \frac{d}{dt} \Bigr |_{t=0} \det(A+tX) = \frac{d}{dt} \Bigr |_{t=0} \det(I+tA^{-1}X) = tr(A^{-1} X),$$
    where $tr : \text{Mat}_\mathbb R(n) \rightarrow R$ is the trace (sum
    of diagonal entries). Hence
    $$\mathfrak{sl}(n,R) = \{X \in \text{Mat}_\mathbb R (n)| tr(X) = 0 \}.$$
:::

### Example: Steiner's surface revisited

\[Omitted\]

### The tangent bundle

::: {.proposition}
**Proposition 20**. *For any manifold $M$ of dimension $m$, the tangent
bundle $$TM = \bigsqcup_{p\in M} T_p M$$ (disjoint union of vector
spaces) is a manifold of dimension $2m$. The map
$$\pi : TM \rightarrow M$$ taking $v \in TpM$ to the base point $p$, is
a smooth submersion, with fibers in the tangent spaces.*
:::

::: {.proposition}
**Proposition 21**. *For any smooth map $F \in C^\infty(M,N)$, the map
$T F : TM \rightarrow TN$ given on $T_pM$ as the tangent maps
$T_pF : T_pM \rightarrow T_{F(p)}N$, is a smooth map*
:::

# Vector Fields

## Vector fields as derivations

::: {.defn}
**Definition 54**. (Vector Fields - first definition).

A collection of tangent vectors $X_p, p \in M$ defines a vector field
$X \in \mathfrak X \in M$ if and only if for all functions
$f \in C^\infty(M)$ the function $p \mapsto X_p(f)$ is smooth. The space
of all vector fields on $M$ is denoted $\mathfrak X(M)$. We hence obtain
a linear map $X : C^\infty(M) \rightarrow C^\infty(M)$ such that
$$X (f)|_p = X_p(f).$$
:::

Since each $X_p$ satisfy the product rule (at $p$), it follows that $X$
itself satisfies a product rule. We can use this as an alternative
definition:

::: {.defn}
**Definition 55**. (Vector Fields - second definition).

A vector field on $M$ is a linear map
$X : C^\infty (M) \rightarrow C^\infty (M)$ satisfying the product rule,
$$X(f g) = X(f)g + f X(g)$$ for $f,g \in C^\infty(M)$.
:::

We can also express the smoothness of the tangent vectors $X_p$ in terms
of coordinate charts $(U,\phi)$. Recall that for any $p \in U$, and all
$f \in C^\infty(M)$, the tangent vector $X_p$ is expressed as
$$X_p(f) = \sum_{i=1}^m a^i (u) \frac{\partial}{\partial u^i} \Bigr |_{u=\phi(p)}  (f \circ \phi^{-1})$$

::: {.proposition}
**Proposition 22**. *The collection of tangent vectors $X_p,\  p \in M$
define a vector field if and only if for all charts $(U,\phi)$, the
functions $a^i : \phi(U) \rightarrow \mathbb R$ defined by
$$X_{\phi^{-1}(u)} (f) = \sum_{i=1}^m a^i (u) \frac{\partial}{\partial u^i} (f \circ \phi^{-1}),$$
are smooth.*
:::

## Vector fields as sections of the tangent bundle

::: {.defn}
**Definition 56**. (Vector fields -- third definition).

A vector field on $M$ is a smooth map $X \in C^\infty(M,TM)$ such that
$\pi \circ X$ is the identity.
:::

It is common practice to use the same symbol X both as a linear map from
smooth functions to smooth functions, i.e. $X : M \rightarrow TM$, or as
a map into the tangent bundle,
$X : C^\infty(M) \rightarrow C^\infty(M)$. The latter case can also be
expressed as the 'Lie derivative' to avoid confusion:
$L_X : C^\infty(M) \rightarrow C^\infty(M)$

## Lie brackets

::: {.theorem}
**Theorem 57**. *For any two vector fields $X,Y \in \mathfrak X(M)$
(regarded as derivations), the commutator
$$[X,Y] := X \circ Y - Y \circ X : C^\infty (M) \rightarrow C^\infty (M)$$
is again a vector field.*
:::

::: {.defn}
**Definition 58**. (Lie Brackets)

The vector field $[X,Y] := X \circ Y - Y \circ X$ is called the *Lie
bracket* of $X,Y \in \mathfrak X(M)$.
:::

Note: When calculating Lie brackets $X \circ Y - Y \circ X$ of vector
fields $X,Y$ in local coordinates, it is not necessary to work out the
second order derivatives -- we know in advance that these are going to
cancel out.

Let $S \subseteq M$ be a submanifold. A vector field
$X \in \mathfrak X(M)$ is called tangent to $S$ if for all $p \in S$,
the tangent vector $X_p$ lies in $T_pS \subseteq T_pM$. (Thus $X$
restricts to a vector field $X|_S \in \mathfrak X(S)$.)

::: {.proposition}
**Proposition 23**. *If two vector fields $X,Y \in \mathfrak X(M)$ are
tangent to a submanifold $S \subseteq M$, then their Lie bracket is
again tangent to $S$.*
:::

## Related vector fields

::: {.defn}
**Definition 59**. (F-related)

Let $F \in C^\infty(M,N)$ be a smooth map. Vector fields
$X \in \mathfrak X(M)$ and $Y \in \mathfrak X(N)$ are called
$F$-related, written as $X \sim_F Y$, if $T_pF(X_p) = Y_{F(p)}$ for all
$p \in M$.
:::

::: {.example}
**Example 60**. If $F$ is a diffeomorphism, then $X \sim_F Y$ if and
only if $Y = F_* X$. In particular, if $N = M$, then an equation
$X \sim_F X$ means that $X$ is invariant under $F$.
:::

The $F$-relation of vector fields also has a simple interpretation in
terms of the 'differential operator' picture.

::: {.proposition}
**Proposition 24**. *One has $X \sim_F Y$ if and only if for all
$g \in C^\infty(N), \ X(g \circ F) = Y(g) \circ F$.*
:::

::: {.theorem}
**Theorem 61**. *Let $F \in C ^\infty(M,N)$ For vector fields
$X_1,X_2 \in \mathfrak X(M)$ and $Y_1,Y_2 \in \mathfrak X(M)$, we have
$$X_1 \sim_F Y_1, \ X_2 \sim_F Y_2 \rightarrow [X1,X2] \sim_F [Y1,Y2].$$*
:::

## Flows of vector fields

Recall, For any curve $\gamma : J \rightarrow M$, with
$J \subseteq \mathbb R$ an open interval, and any $t \in J$, the
velocity vector
$\dot{\gamma}(t) \equiv \frac{d\gamma}{dt} \in T_{\gamma(t)}M$ is
defined as the tangent vector, given in terms of its action on functions
as $(\dot{\gamma}(t))(f) = \frac{d}{dt} f(\gamma(t))$. (The dot
signifies a t-derivative.)

Equivalently, one may think of the velocity vector as the image of
$\frac{\partial}{\partial t} |_{t} \in T_tJ \cong \mathbb R$ under the
tangent map
$T_t \gamma : \dot{\gamma}(t) = (T_t\gamma)( \frac{\partial}{\partial t}|_t)$.

::: {.defn}
**Definition 62**. Suppose $X \in \mathfrak X(M)$ is a vector field on a
manifold $M$. A smooth curve $\gamma \in C^\infty(J, M)$, where
$J \subseteq R$ is an open interval, is called a solution curve to $X$
if $\dot{\gamma}(t) = X_{\gamma(t)}$ for all $t \in J$.
:::

Geometrically, this means that at any given time $t$, the value of $X$
at $\gamma(t)$ agrees with the velocity vector to $\gamma$ at $t$, i.e.
$\frac{\partial}{\partial t} \sim_\gamma X$.

::: {.example}
**Example 63**. Consider first the case that
$M = U \subseteq \mathbb R^m$. Here curves $\gamma (t)$ are of the form,
$$\gamma(t) = x(t) = (x^1 (t),\dots, x^m (t)),$$ hence,
$$\dot{\gamma}(t) = \sum_{i=1}^m \frac{dx^i}{dt} \frac{\partial}{\partial x^i} \Bigr |_{x(t)}.$$
On the other hand, the vector field has the form
$X = \sum_{i=1}^m a^i (x) \frac{\partial}{\partial x i}$. This becomes
the system of first order ordinary differential equations,
$$\frac{dx^i}{dt} = a^i (x(t)), i = 1,\dots, m.$$
:::

::: {.theorem}
**Theorem 64**. *(Existence and uniqueness theorem for ODE's)*

*Let $U \subseteq \mathbb R$ m be an open subset, and
$a \in C^\infty(U, \mathbb R^m)$. For any given $x_0 \in U$, there is an
open interval $J_{x_0} \subseteq \mathbb R$ around $0$, and a solution
$x : J_{x_0} \rightarrow U$ of the ODE
$$\frac{d x^i}{dt} = a^i (x(t)), i = 1, \dots, m$$ with initial
condition $x(0) = x_0$, and which is maximal in the sense that any other
solution to this initial value problem is obtained by restriction to
some subinterval of $J_{x0}$.*
:::

Thus, $J_{x_0}$ is the maximal open interval on which the solution is
defined.

::: {.theorem}
**Theorem 65**. *(Dependence on initial conditions for ODE's)*

*For $a \in C^\infty(U,\mathbb R^m)$ as above, the set
$$\mathscr J = \{(t, x) \in \mathbb R \times U | t \in J_x \}.$$ is an
open neighborhood of $\{0\} \times U$ in $\mathbb R \times U$, and the
map $$\Phi : \mathscr  J \rightarrow U, \  (t, x) \mapsto \Phi(t, x)$$
is smooth.*
:::

For a general vector field $X \in \mathfrak X(M)$ on manifolds, Equation
$\dot{\gamma}(t) = X_{\gamma(t)}$ becomes
$\frac{dx^i}{dt} = a^i (x(t)), i = 1,\dots,m$ after introduction of
local coordinates. The existence and uniqueness theorem for ODE's
extends to manifolds, as follows:

::: {.theorem}
**Theorem 66**. *Let $X \in \mathfrak X(M)$ be a vector field on a
manifold $M$. For any given $p \in M$, there is an open interval
$\mathscr J_p \subseteq \mathbb R$ around $0$, and a solution
$\gamma : \mathscr J_p \rightarrow M$ of the initial value problem
$$\dot{\gamma}(t) = X_{\gamma(t)} ,\  \gamma(0) = p,$$ which is maximal
in the sense that any other solution of the initial value problem is
obtained by restriction to a subinterval. The set
$$\mathscr J = \{(t, p) \in\mathbb R \times M | t \in \mathscr J_p\}$$
is an open neighborhood of $\{0\} \times M$, and the map
$$\Phi : \mathscr J \rightarrow M,  \ (t, p) \mapsto  \Phi(t, p)$$ such
that $\gamma(t) = \Phi(t, p)$ solves the initial value problem mentioned
above and is smooth.*
:::

Note that the uniqueness part uses the Hausdorff property in the
definition of manifolds. Indeed, the uniqueness part may fail for
non-Hausdorff manifolds.

::: {.defn}
**Definition 67**. (Flow)

Given a vector field $X$, the map $\Phi : J \rightarrow M$ is called the
flow of $X$. For any given $p$, the curve $\gamma(t) = \Phi(t, p)$ is a
solution curve. One can also fix $t$ and consider the time-$t$ flow
$\Phi_t(p) \equiv \Phi(t, p).$
:::

Intuitively, $\Phi_t(p)$ is obtained from the initial point $p \in M$ by
flowing for time $t$ along the vector field $X$. One expects that first
flowing for time $t$, and then flowing for time $s$, should be the same
as flowing for time $t +s$. Indeed one has the following flow property

::: {.theorem}
**Theorem 68**. *(Flow property).*

*Let $X \in \mathscr X(M)$, with flow $\Phi : \mathscr J \rightarrow M$.
Let $(t_2, p) \in \mathscr J$, and $t_1 \in \mathbb R$. Then
$$(t_1,\Phi_{t_2} (p)) \in \mathscr J \iff (t_1 +t_2, p) \in \mathscr J,$$
and one has $$\phi_{t_1} (\Phi_{t_2} (p)) = \Phi_{t_1+t_2} (p).$$*
:::

We see in particular that for any $t$, the map
$\Phi_t : U_t \rightarrow M$ is a diffeomorphism onto its image
$\Phi_t(U_t) = U_{-t}$, with inverse $\Phi_{-t}$. Let $X$ be a vector
field, and $\mathscr J = \mathscr J^X$ be the domain of definition for
the flow $\Phi = \Phi^X$ .

::: {.defn}
**Definition 69**. A vector field $X \in \mathscr X (M)$ is called
complete if $\mathscr J^X = \mathbb R \times M$. Thus $X$ is complete if
and only if all solution curves exist for all time.
:::

A vector field may fail to be complete if a solution curve escapes to
infinity in finite time. This suggests that a vector fields $X$ that
vanishes outside a compact set must be complete, because the solution
curves are 'trapped' and cannot escape to infinity:

::: {.proposition}
**Proposition 25**. *If $X \in \mathfrak X(M)$ is a vector field that
has compact support, in the sense that $X |_{M-A} = 0$ for some compact
subset $A$, then $X$ is complete. In particular, every vector field on a
compact manifold is complete.*
:::

::: {.theorem}
**Theorem 70**. *If $X$ is a complete vector field, the flow $\Phi_t$
defines a $1$-parameter group of diffeomorphisms. That is, each $\Phi_t$
is a diffeomorphism and
$$\Phi_0 = id_M, \  \Phi_{t_1} \circ \Phi_{t_2} = \Phi_{t_1+t_2}.$$*

*Conversely, if $\Phi_t$ is a $1$-parameter group of diffeomorphisms
such that the map $(t, p) \mapsto \Phi_t(p)$ is smooth, the equation
$$X_p(f) = \frac{d}{dt} \Bigr  |_{t=0} f(\Phi_{t}(p))$$ defines a
complete vector field $X$ on $M$, with flow $\Phi_t$.*
:::

::: {.proposition}
**Proposition 26**. *Let $F \in C^\infty(M,N)$, and let
$X \in \mathscr X(M), Y \in \mathscr X(N)$ be complete vector fields,
with flows $\Phi^X_t , \Phi^Y_t$.
$$X \sim_F Y \iff F \circ \Phi^X_t = \Phi^Y_t \circ F$$ for all $t$.*
:::

In short, vector fields are $F$-related if and only if their flows are
$F$-related.
$\Phi^*_t : C^\infty (M) \rightarrow C^\infty (M), \Phi^* t : \mathfrak X(M) \rightarrow \mathfrak X(M)$.

## Geometric interpretation of the Lie bracket

For any smooth map $F \in C^\infty(M,N)$ we defined the pull-back
$$F^* : C ^\infty (N) \rightarrow C ^\infty (M), \ g \mapsto g \circ F.$$
If $F$ is a diffeomorphism, then we can also pull back vector fields:
$F^* : X(N) \rightarrow X(M), \ Y \mapsto F^*Y$, by the condition
$(F^*Y)(F^* g) = F^* (Y(g))$ for all functions $g$. That is,
$F^* Y \sim_F Y$, or in more detail $(F^*Y)_p = (T_pF)^{ -1}Y_{F(p)}$.
By Theorem 5.2, we have $F^*[X,Y] = [F^*X,F^*Y]$.

Any complete vector field $X \in \mathfrak X(M)$ with flow $\Phi_t$
gives rise to a families of pull-back map.
$$\Phi^*_t : C ^\infty (M) \rightarrow C^\infty (M), \  \Phi^*_t : X(M) \rightarrow X(M)$$

::: {.defn}
**Definition 71**. The Lie derivative of a function f with respect to
$X$ is the function
$$L_X (f) = \frac{d}{dt} \Bigr |_{t=0} \Phi^*_t f ;$$

thus $L_X (f) = X(f)$. The Lie derivative measures how $f$ changes in
the direction of $X$. Similarly, for a vector field $Y$ one defines the
Lie derivative $L_X (Y)$ by
$$L_X (Y) = \frac{d} {dt}\Bigr |_{t=0} \Phi^*_t Y \in X(M).$$
:::

::: {.defn}
**Definition 72**. For any $X,Y \in \mathfrak X(M)$, the Lie derivative
$L_X Y$ is just the Lie bracket: $L_X (Y) = [X,Y]$.
:::

Thus, the Lie bracket $[X,Y]$ measures 'infinitesimally' how the vector
field $Y$ changes along the flow of $X$. Note that in particular, $L_XY$
is skew-symmetric in $X$ and $Y$ -- this is not obvious from the
definition. One can also interpret the Lie bracket as measuring how the
flows of $X$ and $Y$ fail to commute.

::: {.theorem}
**Theorem 73**. *Let $X,Y$ be complete vector fields, with flows
$\Phi_t ,\Psi_s$. Then, $$\begin{aligned}
= 0 &\iff \Phi^*_t Y = Y \text{for all t}\\
    &\iff \Psi^*_s X = X \text{for all s} \\
    &\iff  \Phi_t \circ \Psi_s  = \Psi_s \circ \Phi_t \text{for all s,t.}\end{aligned}$$*
:::

## Frobenius theorem

We saw that for any vector field $X \in \mathfrak X(M)$, there are
solution curves through any given point $p \in M$. The image of this
curve is an (immersed) submanifold to which $X$ is everywhere tangent.
One might similarly 'integral surfaces' for pairs of vector fields, and
'integral submanifolds' for collections of vector fields

::: {.defn}
**Definition 74**. (Involutive)

Consider a sub-bundle $E \subseteq TM$ of rank $r$. Such a subbundle is
called *involutive* if the Lie bracket of any two sections of E is again
a section of $E$. For vector fields $X_i$ as above, the pointwise spans
$$E_p = \text{span} \{X_1|_p,\dots,X_r |_p\}$$ define a subbundle with
this property. Recall, an involution is a function that is its own
inverse.
:::

::: {.defn}
**Definition 75**. (Integral Submanifold)

Suppose $X_1,\dots,X_r$ are vector fields on the manifold $M$, such that
the tangent vectors $X_1|_p,\dots,X_r |_p \in T_pM$ are linearly
independent for all $p \in M$. A $r$-dimensional submanifold
$S \subseteq M$ is called an *integral submanifold* if the vector fields
$X_1,\dots,X_r$ are all tangent to $S$.

Suppose that there exists an integral submanifold $S$ through any given
point $p \in M$. Then each Lie bracket $[X_i ,X_j ] |_p \in T_pS$, and
hence is a linear combination of $X_1|_p,\dots,X_r |_p.$ It follows that
$$[X_i ,X_j ] = \sum_{k=1}^r c^k_{ij}X_k$$ for certain (smooth)
functions $c^k_{i j}$.

Indeed, given $X = \sum_{i=1}^m a^i X_i$ and $Y = \sum^m_{i=1} b^i X_i$
with functions $a^i ,b^i$, the condition above guarantees that $E$ is
involutive. Given any rank $r$ subbundle $E \subseteq TM$ (not
necessarily involutive), a submanifold $S \subseteq M$ is called an
integral submanifold if $E_p = T_pS$ for all $p \in S$.
:::

::: {.theorem}
**Theorem 76**. *(Frobenius theorem)*

*Let $E \subseteq TM$ be a subbundle of rank $r$. The following are
equivalent:*

1.  *There exists an integral submanifold through every $p \in M$.*

2.  *$E$ is involutive.*

*In fact, if $E$ is involutive, then it is possible to find a coordinate
chart $(U,\phi)$ near any given $p$, in such a way that the subbundle
$(T\phi)(E|_U ) \subseteq T\phi(U)$ is spanned by the first $r \leq m$
coordinate vector fields
$\frac{\partial}{\partial u^1},\dots, \frac{\partial}{\partial u^r}$.*
:::

Thus, for any involutive subbundle $E \subseteq TM$, then any $p \in M$
has an open neighborhood $U$ with a nice decomposition into
$r$-dimensional submanifolds. One calls such a decomposition (or
sometimes the involutive subbundle E itself) a (local) *foliation*. A
foliation gives a decomposition into submanifolds on a neighborhood of
any given point. Globally, the integral submanifolds are often only
immersed submanifolds, given by immersions $i : S \rightarrow M$ with
$(T_pi)(T_pS) = E_p$ for all $p \in S$.

::: {.example}
**Example 77**. Let $\Phi : M \rightarrow N$ be a submersion. Then the
subbundle $E \subseteq TM$ with fibers
$E_p = \text{ker}(T_p \Phi) \subseteq T_pM$ is an involutive subbundle
of rank $\dim M - \dim N$. Every fiber $\Phi^{-1}(q)$ is an integral
submanifold.
:::

# Differential Forms

## Review: Differential forms on $\mathbb R^m$

Differential forms are an approach to solving multivariable calculus
problems that is independent of coordinates. They provide a unified
approach to define integrands over curves, surfaces, solids, and
higher-dimensional manifolds.

::: {.defn}
**Definition 78**. (Wedge Product in $\mathbb R^m$)

The *exterior product* or *wedge product* is the product operator in an
exterior algebra. If $\alpha$ and $\beta$ are differential $k$-forms of
degrees $p$ and $q$, respectively, then
$$\alpha \wedge \beta=(-1)^{pq} \beta \wedge \alpha.$$ It is not (in
general) commutative, but it is associative, and bilinear.
:::

::: {.example}
**Example 79**. Let $\alpha, \beta \in \Omega^1(M)$. Then we define a
wedge product $\alpha \wedge \beta \in \Omega^2 (M)$, as follows:
$$(\alpha \wedge \beta)(X,Y) = \alpha (X)\beta(Y)-\alpha(Y)\beta(X).$$
:::

::: {.defn}
**Definition 80**. (Differential $k$-form)

A differential $k$-form on an open subset $U \subseteq \mathbb R^m$ is
an expression of the form
$$\omega = \sum_{i_1 \dots i_k} \omega i_1\dots i_k dx^{i_1} \wedge \dots \wedge  dx^{i_k}$$
where $\omega_{i_1\dots i_k} \in C^\infty(U)$ are functions, and the
indices are numbers $1 \leq i_1 < \dots < i_k \leq m$. The symbol
$\wedge$ denotes the exterior product of two differential forms.
:::

Let $\Omega^k (U)$ be the vector space consisting of such expressions,
with pointwise addition. It is convenient to introduce a short hand
notation $I = {i_1,\dots,i_k}$ for the index set, and write
$\omega = \sum_I \omega_I dx^I$ with
$\omega_I = \omega_{i_1 \dots i_k}$, and
$dx^I = dx^{i1} \wedge \dots \wedge dx^{ik}$.

Since a $k$-form is determined by these functions $\omega_I$, and since
there are $\frac{m!}{k!(m-k)!}$ ways of picking $k$-element subsets from
$\{1,\dots,m\}$, the space $\Omega^k (U)$ can be identified with
vector-valued smooth functions,
$\Omega^k (U) = C^\infty (U, \mathbb R ^{\frac{m!}{k!(m-k)!}})$.

An associative product operation
$\Omega^k (U) \times \Omega^l (U) \rightarrow \Omega^{k+l} (U)$ by the
'rule of computation' $dx^i \wedge d x^j = -dx^j \wedge d x^i$ for all
$i, j$; in particular $dx^i \wedge dx^i = 0$.

::: {.defn}
**Definition 81**. (Exterior Differential)

Using the product structure we may define the *exterior differential*
$$d : \Omega^k (U) \rightarrow \Omega^{k+1}(U),  \ d \bigg ( \sum_I \omega_I dx^I \bigg ) = \sum_{i=1}^m \sum_I \frac{\partial \omega_I}{\partial x^i} dx^i \wedge dx^I.$$
:::

The key property of the exterior differential is the following fact:

::: {.proposition}
**Proposition 27**. *The exterior differential satisfies
$$d \circ d = 0,$$ i.e. $dd\omega = 0$ for all $\omega$.*
:::

::: {.example}
**Example 82**. Consider forms on $\mathbb R^3$

-   The differential of a function $f \in \Omega^0 (\mathbb R^3 )$ is a
    1-form
    $$df = \frac{\partial  f}{\partial x} dx + \frac{\partial f}{\partial y}  dy+ \frac{\partial f}{\partial z} dz,$$
    with components being the gradient, $\text{grad} f = \nabla f$.

-   A 1-form $\omega \in \Omega^1 (\mathbb R^3 )$ is an expression
    $\omega = f dx+gdy+hdz$ with functions $f,g,h$. The differential is
    $$d\omega = \bigg( \frac{\partial g}{\partial x} - \frac{\partial f}{\partial y} \bigg )
            dx \wedge dy +
            \bigg ( \frac{\partial h}{\partial y} - \frac{\partial g}{\partial  z} \bigg)  dy\wedge dz + \bigg(\frac{\partial  f}{\partial  z} - \frac{\partial h}{\partial x} \bigg )  dz\wedge dx.$$
    Thinking of the coefficients of $\omega$ as the components of a
    function $F = (f,g,h) : U \rightarrow \mathbb R^3$, we see that the
    coefficients of $d \omega$ give the curl of $F$,
    $curl(F) = \nabla \times F$.

-   Finally, any 2-form $\omega \in \Omega^2 (\mathbb R^3 )$ may be
    written $\omega = a dy \wedge dz + b dz \wedge dx + c dx \wedge dy$,
    with $A = (a,b, c) : U \rightarrow \mathbb R^3$. We obtain
    $$d\omega = (\frac{\partial a}{\partial x} + \frac{\partial b}{\partial y} + \frac{\partial c}{\partial z}) dx \wedge dy \wedge dz;$$
    the coefficient is the divergence $div(A) = \nabla A$ The usual
    properties $curl(grad(f)) = 0, div(curl(F)) = 0$ are both special
    cases of $d \circ d = 0$.
:::

::: {.defn}
**Definition 83**. (Support)

The support $supp(\omega) \subseteq U$ of a differential form is the
smallest closed subset $Z$ so that $\omega$ restricted to any point in
the interior of $Z$ is not identically 0. Suppose
$\omega \in \Omega^m(U)$ is a compactly supported form of the top degree
$k = m$, i.e. it is the set
$$supp(\omega )= \{p\in U : \omega_p \neq 0 \}.$$ Such a differential
form is an expression $\omega = f dx^1 \wedge \dots \wedge dx^m$ where
$f \in C ^\infty(U)$ is a compactly supported function
:::

::: {.defn}
**Definition 84**. (Riemann Integral)

One defines the integral of $\omega$ to be the Riemann integral:
$$\int_U \omega = \int_{\mathbb R^m} f(x^1 ,\dots, x^m )dx^1 \dots dx^m.$$
:::

Note that we can regard $\omega$ as a form on all of $\mathbb R^m$, due
to the compact support condition.

Our aim is now to define differential forms on manifolds, beginning with
1-forms. Even though 1-forms on $U \subseteq \mathbb R^m$ are identified
with functions $U \rightarrow \mathbb R^m$, they should not be regarded
as vector fields, since their transformation properties under coordinate
changes are different. In fact, while vector fields are sections of the
tangent bundle, the 1-forms are sections of its dual space, the
cotangent bundle. We will thus begin with a review of dual spaces in
general.

## Dual spaces

::: {.defn}
**Definition 85**. (Dual space)

For any real vector space $E$, we denote by $E^* = L(E,\mathbb R)$ (the
linear subspace) as its *dual space*, consisting of all linear maps
$\alpha : E \rightarrow \mathbb R$.
:::

If $E$ is finite-dimensional, then the dual space is also
finite-dimensional, and $\dim E^* = \dim E$. It is common to write the
value of $\alpha \in E^*$ on $v \in E$ as a pairing, using the bracket
notation $\langle \alpha, v \rangle := \alpha(v);$. (In physics, it is
common to use Dirac bra-ket notation
$\langle \alpha | v \rangle := \alpha(v)$.)

::: {.defn}
**Definition 86**. (Dual Basis)

Let $e_1,\dots, e_r$ be a basis of $E$. Any element of $E^*$ is
determined by its values on these basis vectors. For $i = 1,\dots,r$,
let $e^i \in E^*$ be the linear functional such that
$$\langle e^i , e_j \rangle = \partial^i_j = 
    \begin{cases}
        0, & \text {if } i \neq j \\ 
        1, & \text{if } i = j
    \end{cases}$$ The elements $e^1, \dots, e^r$ are a basis of $E^*$;
this is called the *dual basis*.
:::

The element $\alpha \in E^*$ is described in terms of the dual bases as
$\alpha = \sum_{j=1}^r \alpha_j e^j, \  \alpha_j = \langle \alpha, e_j \rangle$.
Similarly, for vectors $v \in E$ we have
$v = \sum_{i=1}^r v^i e_i, \ v^i = \langle e^i , v \rangle$.

::: {.defn}
**Definition 87**. (Dual Map)

Given a linear map $R : E \rightarrow F$ between vector spaces, one
defines the dual map $R^* : F^* \rightarrow E^*$ (note the direction),
by setting $\langle R^* \beta, v \rangle = \langle \beta ,R(v)\rangle$
for $\beta \in F^*$ and $v \in E$.
:::

This satisfies $(R^*)^* = R$, and under the composition of linear maps,
$(R_1 \circ R_2)^* = R^*_2 \circ R^*_1$. In terms of basis
$e_1,\dots, e_r$ of $E$ and $f_1,\dots, f_s$ of $F$, and the
corresponding dual bases (with upper indices), a linear map
$R : E \rightarrow F$ is given by the matrix with entries
$R_i^j = \langle f^j , R(e_i)\rangle$, while $R^*$ is described by the
transpose of this matrix (the roles of $i$ and $j$ are reversed). Thus,
$(R^*)^j_i = R_i^j$.

## Cotangent spaces

::: {.defn}
**Definition 88**. (Cotangent spaces, vectors, maps)

The dual of the tangent space $T_pM$ of a manifold $M$ is called the
*cotangent space* at $p$, denoted $T^*_p M = (T_pM)^*$.

Elements of $T^*_p M$ are called *cotangent vectors*, or simply
covectors.

Given a smooth map $F \in C^\infty(M, N)$, and any $p \in M$ we have the
*cotangent map* $T^*_p F = (T_pF)^* : T^*_{F(p)}N \rightarrow T^*_p M$
defined as the dual to the tangent map.
:::

Thus, a co(tangent) vector at $p$ is a linear functional on the tangent
space, assigning to each tangent vector at $p$ a number. The very
definition of the tangent space suggests one such functional: Every
function $f \in C^\infty(M)$ defines a linear map,
$T_pM \rightarrow \mathbb R, v \mapsto v(f)$. This linear functional is
denoted $(d f)_p \in T^*_p M$.

::: {.defn}
**Definition 89**. (Differential)

Let $f \in C^\infty(M)$ and $p \in M$. The covector
$$(d f)p \in T^*_p M,  \langle (d f)_p, v\rangle = v(f).$$ is called the
differential of $f$ at $p$.
:::

::: {.lemma}
**Lemma 90**. *For $F \in C^\infty(M,N)$ and $g \in C^\infty(N),$
$$d(F^* g)_p = T^*_p F((dg)_{F(p)}).$$*

*Let $U \subseteq \mathbb R^m$ and $V \subseteq \mathbb R^n$ be open,
with coordinates $x^1 , \dots , x^m$ and $y^1,\dots, y^n$. For
$F \in C^\infty(U,V)$, the tangent map is described by the Jacobian
matrix.*

*Thought of as matrices, the coefficients of the cotangent map are the
transpose of the coefficients of the tangent map.*
:::

## 1-forms

Similar to the definition of vector fields, one can define co-vector
fields, more commonly known as 1-forms: Collections of covectors
$\alpha_p \in T^*_p M$ depending smoothly on the base point.

::: {.defn}
**Definition 91**. (1-form)

A 1-form on $M$ is a linear map
$$\alpha : \mathfrak X(M) \rightarrow C^\infty (M), \  X \mapsto \alpha(X) = \langle \alpha, X \rangle,$$
which is $C^\infty(M)$-linear in the sense that
$\alpha(f X) = f\alpha(X)$ for all
$f \in C^\infty(M), X \in \mathfrak X(M)$. The space of 1-forms is
denoted $\Omega^1 (M)$.
:::

Let us verify that a 1-form can be regarded as a collection of
covectors:

::: {.lemma}
**Lemma 92**. *Let $\alpha \in \Omega^1 (M)$ be a 1-form, and $p \in M$.
Then there is a unique covector in the cotangent space
$\alpha_p \in T^*_p M$ such that $\alpha(X)_p = \alpha_p(X_p)$ for all
$X \in \mathfrak X(M)$. Note, we indicate the value of the function
$\alpha(X)$ at $p$ by a subscript, just like we did for vector fields.*
:::

The first example of a 1-form is described in the following definition.

::: {.defn}
**Definition 93**. (Exterior differential)

The exterior differential of a function $f \in C^\infty(M)$ is the
1-form $d f \in \Omega^1 (M)$, defined in terms of its pairings with
vector fields $X \in \mathfrak X(M)$ as $\langle d f, X\rangle = X(f)$.
:::

::: {.lemma}
**Lemma 94**. *Let $\alpha : p \mapsto \alpha p \in T^*_p M$ be a
collection of covectors. Then $\alpha$ defines a 1-form, with
$$\alpha(X)_p = \alpha_p(X_p)$$ for $p \in M$, if and only if for all
charts $(U,\phi)$, the coefficient functions for $\alpha$ in the chart
are smooth*
:::

## Pull-backs of function and 1-forms

Recall that for any manifold $M$, the vector space $C^\infty(M)$ of
smooth functions is an algebra, with product the pointwise
multiplication. Any smooth map $F : M \rightarrow M'$ between manifolds
defined an algebra homomorphism, called the pull-back
$$F^* : C^\infty (M') \rightarrow C^\infty (M), \ \ f \mapsto F ^* (f) := f \circ F.$$
The fact that this preserves products is the following simple
calculation:
$$(F^* (f)F^* (g))(p) = f(F(p))g(F(p)) = (f g)(F(p)) = F^* (f g)(p).$$
Given another smooth map $F' : M' \rightarrow M''$ we have
$(F'\circ F)^* \circ F^* \circ (F' )^*$.

Let $F \in C^\infty(M,N)$ be a smooth map. Recall that for vector
fields, there is no general 'push-forward' or 'pull-back' operation,
unless $F$ is a diffeomorphism. For 1-forms the situation is better: for
any $p \in M$ one has the dual to the tangent map
$$T^*_p F = (T_pF)^* : T^*_{F(p)}N \rightarrow T^*_p M.$$ For a 1-form
$\beta \in \Omega^1 (N)$, we can therefore define
$(F^* \beta)_p := (T^*_p F)(\beta_{F(p)})$

::: {.lemma}
**Lemma 95**. *The collection of co-vectors $(F^*\beta)_p \in T^*_p M$
depends smoothly on $p$, defining a 1-form $F^*\beta \in \Omega^1 (M)$.*
:::

The Lemma shows that we have a well-defined pull-back map
$F^* : \Omega^1 (N) \rightarrow \Omega^1  (M), \beta \mapsto F^* \beta$.
Under composition of two maps, $(F_1 \circ F_2)^* = F^*_2 \circ F^*_1$.
The pull-back of forms is related to the pull-back of functions,
$g \mapsto F^*g = g \circ F$:

::: {.proposition}
**Proposition 28**. *For $g \in C^\infty(N)$, $F^* (dg) = d(F^* g)$.*
:::

Recall once again that while $F \in C^\infty(M,N)$ induces a tangent map
there is no natural push-forward operation for vector fields. By
contrast, for cotangent bundles there is no naturally induced map from
$T^*N$ to $T^*M$ (or the other way), yet there is a natural pull-back
operation for 1-forms. For any related vector fields $X \sim_F Y$, and
$\beta \in \Omega^1 (N)$, we then have that
$(F^* \beta)(X) = F^* (\beta(Y))$. Indeed, at any given $p \in M$ this
just becomes the definition of the pullback map.

## Integration of 1-forms

Given a curve $\gamma : J \rightarrow M$ in a manifold, and any 1-form
$\alpha \in \Omega^1 (M)$, we can consider the pull-back
$\gamma^*\alpha \in \Omega^1 (J)$. By the description of 1-forms on
$\mathbb R$, this is of the form $\gamma^*\alpha = f(t)dt$ for a smooth
function $f \in C^\infty(J)$.

To discuss integration, it is convenient to work with closed intervals
rather than open intervals. Let $[a,b] \subseteq R$ be a closed
interval. A map $\gamma : [a,b] \rightarrow M$ into a manifold will be
called smooth if it extends to a smooth map from an open interval
containing $[a,b]$. We will call such a map a smooth path.

::: {.defn}
**Definition 96**. (Integral)

Given a smooth path $\gamma : [a,b] \rightarrow M$, we define the
integral of a 1-form $\alpha \in \Gamma^1 (M)$ along $\gamma$ as
$$\int_\gamma \alpha = \int_b^a \gamma^*\alpha.$$
:::

The fundamental theorem of calculus has the following consequence for
manifolds. It is a special case of Stokes' theorem

::: {.proposition}
**Proposition 29**. *Let $\gamma : [a,b] \rightarrow M$ be a smooth
path, with $\gamma(a) = p, \ \gamma(b) = q$. For any
$f \in C^\infty(M)$, we have $\int_\gamma d f = f(q) -  f(p)$. In
particular, the integral of $d f$ depends only on the end points of the
path, rather than the path itself.*
:::

::: {.defn}
**Definition 97**. A 1-form $\alpha \in \Omega^1(M)$ such that
$\alpha = d f$ for some function $f \in C^\infty(M)$ is called exact.
:::

::: {.example}
**Example 98**. Consider the $1$-form
$\alpha = y^2 e^x dx+2y e^x dy \in \Omega(\mathbb R^2)$. Find the
integral of $\alpha$ along the path
$\gamma  : [0,1] \rightarrow M, \ t \mapsto (sin(\pi t/2),t^3 )$.
Observe that the 1-form $\alpha$ is exact: $\alpha = d (y^2 e^x) = d f$
with $f(x, y) = y^2 e^x$. The path has end points $\gamma (0) = (0,0)$
and $\gamma (1) = (1,1)$. Hence,
$\int_\gamma  \alpha = f(\gamma (1))- f(\gamma (0)) = e$.
:::

## 2-forms

::: {.defn}
**Definition 99**. A 2-form on $M$ is a $C^\infty(M)$-bilinear
skew-symmetric map
$$\alpha : \mathfrak X(M)\times \mathfrak X(M) \rightarrow C^\infty (M), (X,Y) \mapsto \alpha (X,Y)$$

Here skew-symmetry means that $\alpha(X,Y) = -\alpha(Y,X)$ for all
vector fields $X,Y$, while $C^\infty(M)$-bilinearity means
$$\alpha(f X,Y) = f\alpha(X,Y) = \alpha(X, fY)$$ for
$f \in C^\infty(M)$, as well as
$\alpha(X' + X'' ,Y) = \alpha(X',Y) + \alpha(X'',Y)$, and similarly in
the second argument. Also, if $\alpha$ is a 2-form then so is $f\alpha$
for any smooth function $f$.
:::

::: {.example}
**Example 100**. For an open subset $U \subseteq \mathbb R^m$, a 2-form
$\omega \in \Omega^2 (U)$ is uniquely determined by its values on
coordinate vector fields. By skew-symmetry the functions
$\omega_{i j} = \omega  \bigg ( \frac{\partial}{\partial  x^i} , \frac{\partial}{ \partial  x^j} \bigg )$
satisfy $\omega_{i j} = -\omega_{ji}$; hence it suffices to know these
functions for $i < j$. As a consequence, we see that the most general
2-form on $U$ is
$$\omega  = \frac{1}{2} \sum^m_{i, j=1} \omega_{i j} dx^i \wedge dx ^j = \sum_{i<j} \omega_{i j}dx^i \wedge dx^j.$$
:::

## k-forms

### Definition

::: {.defn}
**Definition 101**. Let $k$ be a non-negative integer. A k-form on $M$
is a $C^\infty(M)$-multilinear, skew-symmetric map
$$\alpha : \underbrace{\mathfrak X(M) \times \dots \times \mathfrak X(M)}_\text{k times} \rightarrow C^\infty (M).$$
The space of k-forms is denoted $\Omega^k (M)$; in particular
$\Omega^0 (M) = C^\infty(M)$
:::

Here, skew-symmetry means that $\alpha(X_1,\dots, X_k)$ changes sign
under exchange of any two of its elements. The
$C^\infty(M)$-multilinearity means $C^\infty(M)$-linearity in each
argument, similar to the condition for 2-forms. It implies $\alpha$ is
local in the sense that the value of $\alpha(X_1,\dots,X_k)$ at any
given $p \in M$ depends only on the values
$X_1|p,\dots,X_k |p \in T_pM$.

If $\alpha_1,\dots,\alpha_k$ are 1-forms, then one obtains a k-form
$\alpha =: \alpha_1\wedge\dots\wedge\alpha_k$ by wedge product.

Using $C^\infty$-multilinearity, a k-form on $U \subseteq R$ m is
uniquely determined by its values on coordinate vector fields. i.e. by
the functions,
$$\alpha_{i_1\dots i_k} = \alpha \bigg ( \frac{\partial}{\partial x^{i_1}}, \dots , \frac{\partial}{ \partial x ^{i_k}} \bigg )$$
Moreover, by skew-symmetry we only need to consider ordered index sets
$I = {i_1,\dots,i_k} \subseteq {1,\dots,m}$, that is,
$i_1 < \dots < i_k$. Using the wedge product notation, we obtain
$$\alpha = \sum_{i_1<\dots<i_k} \alpha_{i_1\dotsi_k} dx^{i_1} \wedge \dots dx^{i_k}.$$

### Wedge product

::: {.defn}
**Definition 102**. (k,l-shuffle )

A permutation $s \in \mathfrak S_{k+l}$ is called a $k,l$-shuffle if it
satisfies $$s(1) < \dots < s(k), \ \ s(k +1) < \dots < s(k +l).$$
:::

::: {.defn}
**Definition 103**. (Wedge product)

The wedge product of $\alpha  \in  \Gamma^k (M)$,
$\beta  \in  \Gamma^l (M)$ is the element
$$\alpha \wedge \beta \in  \Gamma^{k+l} (M)$$ given as
$$(\alpha \wedge\beta )(X^1,\dots ,X^{k+l}) = \sum sign(s) \alpha (X_{s(1)},\dots ,X_{s(k)}) \beta (X_{s(k+1)},...,X_{s(k+l)})$$
where the sum is over all $k,l$-shuffles.
:::

The wedge product is graded commutative: If $\alpha \in \Omega^k (M)$
and $\beta \in \Omega^l (M)$ then
$\alpha \wedge \beta = (-1) ^{kl}\beta \wedge \alpha$. Furthermore, it
is associative:

::: {.proposition}
**Proposition 30**. *Given $\alpha_i \in \Omega_{k_i} (M)$ we have
$(\alpha_1 \wedge \alpha_2)\wedge \alpha_3 = \alpha_1 \wedge (\alpha_2 \wedge \alpha_3)$*
:::

### Exterior differential

Recall that we defined the exterior differential on functions by the
formula $(d f)(X) = X(f)$. We will now extend this definition to all
forms.

::: {.theorem}
**Theorem 104**. *There is a unique collection of linear maps
$d : \Omega^k (M) \rightarrow \Omega^{k+1} (M)$, extending the map
$(d f)(X) = X(f)$ for $k = 0$, such that $d(d f) = 0$ and satisfying the
graded product rule,
$$d(\alpha \wedge \beta) = d\alpha \wedge \beta + (-1) k\alpha \wedge d\beta$$
for $\alpha \in \Omega^k (M)$ and $\beta \in \Omega^l (M)$. This
exterior differential satisfies $d \circ d = 0$.*
:::

::: {.defn}
**Definition 105**. (Exact, closed k-forms)

A k-form $\omega \in \Omega^k (M)$ is called *exact* if
$\omega = d\alpha$ for some $\alpha \in \Omega^{k-1} (M)$. It is called
closed if $d\omega = 0$.
:::

Since $d\circ d = 0$, the exact $k$-forms are a subspace of the space of
closed $k$-forms; a necessary condition for $\alpha$ to be exact is that
it is closed.

::: {.example}
**Example 106**. The quotient space (closed k-forms modulo exact
k-forms) is a vector space called the k-th (de Rham) cohomology
$$H^k (M) = \frac{\{\alpha \in \Omega^k (M)| \alpha is closed \}}{\{\alpha \in \Omega^k(M)| \alpha is exact \}}.$$

It turns out that whenever $M$ is compact (and often also if $M$ is
non-compact), $H ^k (M)$ is a finite-dimensional vector space. The
dimension of this vector space $b_k(M) = \dim H^k (M)$ is called the
k-th Betti number of $M$; these numbers are important invariants of $M$
which one can use to distinguish non-diffeomorphic manifolds.
:::

## Lie derivatives and contractions

::: {.defn}
**Definition 107**. (Contractions)

Given a vector field $X$, and a $k$-form $\alpha  \in \omega k (M)$, we
can define a $k-1$-form $$\iota_X \alpha \in \omega  k-1 (M)$$ by
*contraction*: Thinking of $\alpha$ as a multi-linear form, one simply
puts $X$ into the first slot:
$$(\iota_X\alpha )(X_1,...,X_{k-1}) = \alpha (X,X_1,\dots,X_{k-1}).$$
Contractions have the following compatibility with the wedge product,
similar to that for the exterior differential:
$$\iota_X (\alpha  \wedge \beta ) = \iota_X\alpha  \wedge \beta  + (-1) k\alpha  \wedge \iota_X \beta ,$$
for $\alpha  \in \omega^k (M)$,$\beta  \in \omega^l (M)$, which one
verifies by evaluating both sides on vector fields.
:::

Another important operator on forms is the Lie derivative:

::: {.theorem}
**Theorem 108**. *Given a vector field $X$, there is a unique collection
of linear maps $L_X : \Omega^k (M) \rightarrow \Omega^k (M)$, such that
$$L_X (f) = X(f), \ L_X (d f) = dX(f),$$ and satisfying the product
rule,
$$L_X (\alpha  \wedge \beta ) = L_X \alpha  \wedge \beta  +\alpha  \wedge L_X \beta$$
for $\alpha  \in \Omega^k (M)$ and $\beta  \in \Omega^l (M)$.*
:::

These operators, $d, L_X, \iota_X$, have the following compatibilities
with the wedge product: For $\alpha \in \Omega^k (M)$ and
$\beta \in \Omega^l (M)$ one has $$\begin{aligned}
d(\alpha \wedge\beta) &= (d\alpha)\wedge\beta + (-1) k\alpha \wedge d\beta,\\
L_X (\alpha \wedge\beta) &= (L_X\alpha)\wedge\beta +\alpha \wedge L_X \beta,\\
\iota_X (\alpha \wedge\beta) &= (\iota_X\alpha)\wedge\beta + (-1) k\alpha \wedge\iota_X \beta.\end{aligned}$$

One says that $L_X$ is an *even derivation* relative to the wedge
product, whereas $d,\iota_X$ are *odd derivations*. They also satisfy
important relations among each other: $$\begin{aligned}
    d \circ d = 0 \\
    L_X \circ L_Y -L_Y \circ L_X = L_{[X,Y]} \\
    \iota_X \circ \iota_Y +\iota_Y \circ \iota_X = 0 \\
    d \circ L_X -L_X \circ d = 0 \\
    L_X \circ \iota_Y -\iota_Y \circ L_X = \iota_[X,Y] \\
    \iota_X \circ d+d \circ \iota_X = L_X .\end{aligned}$$ This
collection of identities is referred to as the Cartan calculus, , and in
particular the last identity is called the Cartan formula.

### Pull-backs

::: {.defn}
**Definition 109**. (k-form Pullbacks)

Similar to the pull-back of functions (0-forms) and 1-forms, we have a
pull-back operation for k-forms,
$F^* : \Omega^k (N) \rightarrow \Omega^k (M)$ for any smooth map between
manifolds, $F \in C^\infty(M,N)$. Its evaluation at any $p \in M$ is
given by
$$(F^* \beta )_p(v_1,\dots, v_k) = \beta_{F(p)} (T_pF(v1),\dots,T_pF(v_k)).$$
:::

The pull-back map satisfies $d(F^*\beta) = F^*d\beta$, and for a wedge
product of forms,
$F^* (\beta_1 \wedge \beta_2) = F^* \beta_1 \wedge F^* \beta_2$.

::: {.proposition}
**Proposition 31**. *Let $U \subseteq \mathbb R^m$with coordinates $x^i$
, and $V \subseteq \mathbb R^n$ with coordinates $y^j$. Suppose $m = j$,
and $F \in C^\infty(U,V)$. Then
$$F^* (dy^1 \wedge \dots \wedge dy^n ) = J dx^ 1 \wedge \dots \wedge dx^n$$
where $J(x)$ is the determinant of the Jacobian matrix,
$$J(x) = \det \bigg (\frac{\partial F^i}{\partial  x^j} \bigg ) ^n_{i, j=1}.$$*
:::

The Lie derivative $L_X \alpha$ of a differential form with respect to a
vector field $X$ has an important interpretation in terms of the flow
$\Phi_t$ of $X$. Assuming for simplicity that $X$ is complete (so that
$\Phi_t$ is a globally defined diffeomorphism), one has the formula
$$L_X\alpha = \frac{d}{dt} \Bigr |_{t=0} \Phi^*_t \alpha.$$ The formula
shows that $L_X$ measures to what extent $\alpha$ is invariant under the
flow of $X$.

### Integration of differential forms

Differential forms of top degree can be integrated over oriented
manifolds. Let $M$ be an oriented manifold of dimension $m$, and
$\omega \in \Omega^m(M)$. Let $supp(\omega)$ be the support of $\omega$.
If $supp(\omega)$ is contained in an oriented coordinate chart
$(U,\phi)$, then one defines
$$\int_M \omega = \int_{\mathbb R^m} f(x)dx^1\cdots dx^m$$

where $f \in C^\infty(\mathbb R^m)$ is the function, with
$supp(f) \subseteq \phi(U)$, determined from
$$(\phi^{-1} )^* \omega = f dx^1 \wedge \cdots \wedge dx^m.$$ This
definition does not depend on the choice of oriented chart.

If $\omega$ is not necessarily supported in a single oriented chart, we
proceed as follows. Let $(U_i , \phi^i), \ i = 1,\dots,r$ be a finite
collection of oriented charts covering $supp(\omega)$. Together with
$U_0 = M \setminus supp(\omega)$ this is an open cover of $M$.

::: {.lemma}
**Lemma 110**. *Given a finite open cover of a manifold there exists a
partition of unity subordinate to the cover, i.e. functions
$\chi_i \in C^\infty(M)$ with $supp(\chi_i) \subseteq U_i$ and
$\sum_{i=0}^r \chi_i = 1$.*
:::

Indeed, partitions of unity exists for any open cover, not only finite
ones. Let $\chi_0, \dots, \chi_r$ be a partition of unity subordinate to
this cover. We define
$$\int_M \omega = \sum_{i=1}^r \int_M \chi_i \omega$$ where the summands
are defined as above, since $\chi_i\omega$ is supported in $U_i$ for
$i \geq 1$. It can be shown that this is well defined, independent of
the choice of oriented coordinate charts.

### Integration over oriented submanifolds

Let $M$ be a manifold, not necessarily oriented, and $S$ is a
k-dimensional oriented submanifold, with inclusion
$i : S \rightarrow M$. We define the integral over $S$, of any k-form
$\omega \in \Omega^k (M)$ such that $S \cap supp(\omega)$ is compact, as
follows:

$$\int_S \omega = \int_S i^* \omega.$$ Of course, this definition works
equally well for any smooth map from $S$ into $M$. For example, the
integral of compactly supported 1-forms along arbitrary paths
$\gamma : \mathbb R \rightarrow M$ is defined. Note also that $M$ itself
does not have to be oriented, it suffices that $S$ is oriented.

### Stokes' theorem

Let $M$ be an $m$-dimensional oriented manifold.

::: {.defn}
**Definition 111**. (Boundary and interior of region)

A region with (smooth) boundary in $M$ is a closed subset
$D \subseteq M$ with the following property: There exists a smooth
function $f \in C^\infty(M,R)$ such that $0$ is a regular value of $f$ ,
and $$D = \{p \in M | f(p) \leq 0 \}.$$ We do not consider $f$ itself as
part of the definition of $D$, only the existence of $f$ is required.

The interior of a region with boundary, given as the largest open subset
contained in $D$, is $$int(D) = \{p \in M| f(p) < 0,$$ and the boundary
itself is $$\partial D = \{p \in M| f(p) = 0 \},$$ a codimension 1
submanifold (i.e., hypersurface) in $M$.
:::

Recall that we are considering $D$ inside an oriented manifold $M$. The
boundary $\partial D$ may be covered by oriented submanifold charts
$(U,\phi)$, in such a way that $\partial D$ is given in the chart by the
condition $x^1 = 0$, and $D$ by the condition $x^1 \leq 0$:
$$\phi (U \cap D) = \phi (U) \cap \{x \in \mathbb R^m | x ^1 \leq 0 \}.$$

We call oriented submanifold charts of this kind *'region charts'*.

::: {.lemma}
**Lemma 112**. *The restriction of the region charts to $\partial D$
form an oriented atlas for $\partial D$.*
:::

In particular, $\partial D$ is again an oriented manifold. To repeat: If
$x^1 ,\dots, x^m$ are local coordinates near $p \in \partial D$,
compatible with the orientation and such that $D$ lies on the side
$x^1 \leq 0$, then $x^2 ,\dots, x^m$ are local coordinates on
$\partial D$. This convention of 'induced orientation' is arranged in
such a way that the Stokes' theorem holds without extra signs.

For an $m$-form $\omega$ such that $supp(\omega)\cap D$ is compact, the
integral $\int_D \omega$ is defined similar to the case of $D = M$.

::: {.theorem}
**Theorem 113**. *(Stokes' Theorem)*

*Let $M$ be an oriented manifold of dimension $m$, and $D \subseteq M$ a
region with smooth boundary $\partial D$. Let
$\alpha \in  \Omega^{m-1} (M)$ be a form of degree $m-1$, such that
$supp(\alpha)\cap D$ is compact. Then
$$\int_D d\alpha = \int_{\partial D} \alpha.$$*
:::

As explained above, the right hand side means
$\int_{\partial D} i^* \alpha$, where $i : \partial D \rightarrow M$ is
the inclusion map.

::: {.corollary}
**Corollary 3**. *Let $\alpha \int \Omega^{m-1}(M)$ be a compactly
supported form on the oriented manifold $M$. Then
$$\int_M d\alpha = 0.$$*
:::

Note that it does not suffice that $d\alpha$ has compact support. A
typical application of Stokes' theorem shows that for a closed form
$\omega \in \Omega^k (M)$, the integral of $\omega$ over an oriented
compact submanifold does not change with smooth deformations of the
submanifold.

::: {.theorem}
**Theorem 114**. *Let $\omega \in \Omega^k (M)$ be a closed form on a
manifold $M$, and $S$ a compact, oriented manifold of dimension $k$. Let
$F \in C^\infty(R\times S,M)$ be a smooth map, thought of as a smooth
family of maps $$F_t = F(t, \cdot) : S \rightarrow M.$$ Then the
integrals $\int_S F^* t \omega$ do not depend on $t$.*
:::

If $F_t$ is an embedding, then this is the integral of $\omega$ over the
submanifold $F_t(S) \subseteq M$.

::: {.defn}
**Definition 115**. (Smooth isotopy)

Given a smooth map $\phi : S \rightarrow M$, one refers to a smooth map
$F : R \times S \rightarrow M$ with $F_0 = \phi$ as an *smooth
deformation or isotopy* of $\phi$. We say that $\phi$ can be smoothly
deformed into $\phi'$ if there exists a smooth isotopy $F$ with
$\phi = F_0$ and $\phi' = F_1$.
:::

The previous theorem shows that if $S$ is oriented, and if there is a
closed form $\omega \in \Omega^k (M)$ with
$$\int_S \phi^* \omega \neq \int_S (\phi' )^* \omega$$ then $\phi$
cannot be smoothly deformed into $\phi 0$.

::: {.example}
**Example 116**. (Winding number).

Let$\omega \in \Omega^2 (\mathbb R^2\{0\})$ be the 1-form
$\omega = \frac{1}{x^2 +y^2} (xdy-ydx)$. In polar coordinates
$x = r \cos\theta, y = r\sin\theta$, one has that $\omega = d\theta$.
Using this fact one sees that $\omega$ is closed (but not exact, since
$\theta$ is not a globally defined function on $\mathbb R^2\{0\}$.)
Hence, if $\gamma : S^1 \rightarrow \mathbb R^2 \{0\}$ is any smooth map
(a 'loop'), then the integral $\int_{S^1} \gamma^*\omega$ does not
change under deformations (isotopies) of the loop. In particular,
$\gamma$ cannot be deformed into a constant map, unless the integral is
zero. The number
$$w(\gamma) = \frac{1}{2\pi} \int_{S^1} \gamma^*\omega$$ is the *winding
number* of $\gamma$. (One can show that this is always an integer, and
that two loops can be deformed into each other if and only if they have
the same winding number.)
:::

### Volume forms

::: {.defn}
**Definition 117**. A non vanishing 1-form $\alpha$ at point $p$ means
that there is a vector $v$ in $T_pM$ such that $\alpha_p(v)\neq 0$.
Similarly for the $k$-form, it means that there is a set of $k$ vectors
such the form is nonzero if evaluated on these vectors.
:::

::: {.defn}
**Definition 118**. (Volume form)

A top degree differential form $\Gamma \in \Omega^m(M)$ is called a
*volume form* if it is nonvanishing everywhere: $\Gamma_p \neq 0$ for
all $p \in M$. In a local coordinate chart $(U,\phi)$, this means that
$$(\phi^{-1} )^*\Gamma = f dx^1 \wedge \cdots \wedge dx^m$$ where
$f(x) \neq 0$ for all $x \in  \phi(U)$.
:::

::: {.lemma}
**Lemma 119**. *A volume form $\Gamma \in \Omega^m(M)$ determines an
orientation on $M$, by taking as the oriented charts those charts
$(U,\phi)$ such that*

*$$(\phi^{-1})^*\Gamma = f dx^1 \wedge \cdots \wedge dx^m$$ with $f > 0$
everywhere on $\Phi(U)$.*
:::

::: {.theorem}
**Theorem 120**. *A manifold $M$ is orientable if and only if it admits
a volume form. In this case, any two volume forms compatible with the
orientation differ by an everywhere positive smooth function:
$$\Gamma' = f \Gamma , f > 0.$$*
:::

::: {.defn}
**Definition 121**. (Volume)

For a compact manifold $M$ with a given volume form
$\Gamma \in \Omega^m(M)$, one can define the volume of $M$,
$$vol(M) = \int_M \Gamma.$$ Here the orientation used in the definition
of the integral is taken to be the orientation given by $\Gamma$ . Thus
$vol(M) > 0$.
:::

Note that volume forms are always closed, for degree reasons (since
$\Omega^{m+1} (M) = 0$). But on a compact manifold, they cannot be
exact:

::: {.theorem}
**Theorem 122**. *Let $M$ be a compact manifold with a volume form
$\Gamma \in \Omega^m(M)$. Then $\Gamma$ cannot be exact.*
:::

# De Rham Cohomology

The exterior derivative converts the algebra of differential forms on a
manifold into a graded differential algebra. The corresponding
cohomology is called the de Rham cohomology algebra.

See Text for full details:

http://im0.p.lodz.pl/ kubarski/AnalizaIV/Wyklady/GHV/ITOM/G-H-V-1

In article 1 it is shown that the de Rham cohomology satisfies the
dimension, homotopy, disjoint union, and Mayer-Vietoris axioms. In
article 2 various examples (retracts, PoincarC lemma, cohomology of Sn,
and RP\") are discussed. In article 3 everything is done again (with the
appropriate modifications) for differential forms with compact carrier.
In article 4 the integral is used to establish the PoincarC duality
theorem for a smooth orientable manifold. This theorem is applied in
article 5 (sec. 5.13 and 5.14) to determine the nth de Rham cohomology
space for any n-manifold (orientable or nonorientable). In sec. 5.15 the
duality theorem is used to show that a compact manifold has
finitedimensional de Rham cohomology. The de Rham cohomology of the
product of two manifolds is computed in article 6 (Kunneth theorems). In
article 7 one version of the de Rham theorem is established. The results
of this article are not quoted elsewhere in the book.

# Overview of Riemannian Geometry

Note, there may be changes in notation from switching reading source.

On $\mathbb R^n$ we have notions like:

1.  Length of vectors angles orthonormal/orthogonal geometry

2.  Areas volumes length of curves

3.  Distance between 2 points

4.  Parallel transport

Observe: All of the elements of Euclidean geometry on $\mathbb R$ is
entirely encoded in the inner product. We introduce geometry into smooth
manifolds by making a choice of inner products on each $TpM$ that varies
smoothly from point to point. This is an inner product.

::: {.defn}
**Definition 123**.
$$g: M \rightarrow T^2 (T^*_pM), p\mapsto g_p \in T^2 (T^*_pM)$$ so that
$g_p$ is an inner product on $T_pM$ and is bilinear symmetric,
nondegenerative, and positive definite.

Then $g_p \in C^\infty$ iff
$g: \mathfrak X(M) \times \mathfrak X(M) \rightarrow C^\infty(M)$,
defined by $g(x,y)(p )= g_p(x_p, y_p)$. Note, $g_p$ is non-linear.
:::

::: {.defn}
**Definition 124**. (M, g) is called a Riemannian manifold.
:::

The manifold has the following properties:

1.  The length of vectors for $v \in T_pm$, $||v|| = \sqrt{g(v,v)}$,
    $\cos (angle v w) = \frac{g(v,w)}{||v||||w||}$.

    ::: {.lemma}
    **Lemma 125**. *Near each point, there exists an orthonormal local
    frame.*
    :::

2.  The length of curve
    $\gamma := \int_a^b \sqrt{g(\gamma(t),\gamma ' (t))} dt$.

3.  Distance $d: M \times M \rightarrow [0, \infty)$ is defined by
    $d(p,q) = \inf(\int_0^1 || \gamma '(t)|| )dt$ where
    $\gamma(0) = p, \gamma(1) = q$.

    This makes $(M,d)$ a metric space so that the metric topology is the
    same as the original topology. One can show that $(M,d)$ is complete
    as a metric space iff $d(p,q)$ is obtained by a curve $\gamma$ for
    all $p,q \in M$.

4.  There is a natural isomorphism
    $\Phi_p: T_pM \rightarrow T^*_pM, \ v \mapsto (v^* : w \mapsto g(v,w))$.
    So there is a module isomorphism
    $\Phi : \mathfrak X \rightarrow \Omega '(M)$.

5.  Let $S \subseteq M$ be a $k$-dimensional manifold. Then $i^*g$
    (induced metric on S) is a Riemannian metric on $S$ giving $S$ the
    unique geometry inherited by $M$.

6.  Suppose $M$ in oriented. There does not exist a nowhere vanishing
    n-form called the volume form satisfying
    $\omega(x_1,\dots, x_n) = 1$ whenever $x$ is a local orthonormal
    frame that has positive orientation. This allows for integration of
    functions for $f \in C^\infty(M)$ defined as
    $\int_M f := \int_m f \omega$. Also, if $M$ is compact, we have
    $vol(M) = \int_M 1 \ \int_M  \omega$. Similarly,
    $Vol_{k-dim}(S) = \int_S 1$ with respect to the induced metric
    $i^* g$ on $S$.

7.  We say $(M, g)$, $(\Tilde{M}, \Tilde{g})$ are isometric if there
    exists a diffeomorphism $F: M \rightarrow \Tilde{M}$ such that
    $g = F^*\Tilde{g}$

## Covariant derivative and curvature

If a parallel transport of a vector along a curve has the property that
$D_{\gamma'(t)} = 0$, then $\gamma$ is the shortest distance between $p$
and $q$ so $\gamma$ is a line.

On a sphere in $S^2$, parrallel transport is equivalent to
$(\delta _{\gamma'(t)} X )^T = 0$ intrinsic to the round metric
$(S^3, g)$. Then the shortest paths are the curves which form great
circles.

Define $(\Tilde{\delta _{X}} Y)= (\delta_X Y)^T$ as the connection
operator for $X,Y\in \mathfrak{X}(S^2)$. This operator is intrinsic to
$S^2$ and satisfies:

1.  $C^\infty$-linear w.r.t. $X$.

2.  $\mathbb R$-linear w.r.t. $Y$.

3.  $(\Tilde{\delta _{X}} fY) = X(f)Y + f\Tilde{\delta_X}Y$.

4.  $\Tilde{\delta_x}y - \Tilde{\delta_y X} = L_x Y$

5.  $Z(g(x,y)) - g(\Tilde{\delta_Z} X,Y) - g(x, \Tilde{\delta_Z}y) = 0$

Let $\gamma$ be a curve, then
$$\frac{d}{dt} (g(X_\gamma(t)), Y_\gamma (T)) = g(\Tilde{\gamma'(t)}X, Y ) + g(X, \Tilde{\gamma'(t)} Y).$$

::: {.theorem}
**Theorem 126**. *On a manifold $(M, g)$ there does not exist a
connection
$\delta : \mathfrak X \times  \mathfrak X \rightarrow \mathfrak X$
satisfying (4) $$[X, Y] = \delta_X Y - D_Y X$$ and (5)
$$Z(g(x,y)) - g(\delta_Z X,Y) - g(x, \delta_Z y) = 0$$ compatible with
the metric. (5) gives rise to the notion of parallel transport on
Riemannian manifolds and is called the Levi-Civita connection.*

*So we say that $X$ is parrellel transported on a curve $\gamma$ on $M$
if $\delta_{\gamma'(t)} X = 0$ for all $t$.*
:::

::: {.defn}
**Definition 127**. (Geodesic)

$\gamma$ is a geodesic if $\delta_{\gamma'(t)} X = 0$ for all $t$.
:::

::: {.theorem}
**Theorem 128**. *If $d(p,q)$ is attained by a curve $\gamma$, then
$\gamma$ is a geodesic.*
:::

Note, the converse is not true. A counter example of a great circle
minus a small segment will not be the shortest distance between the two
points.

Let $(U, \phi)$ be a chart.
$$\delta_{\frac{\partial}{\partial x^i}} \frac{\partial }{\partial x^i}  = \sum_k \Gamma_{ij}^k \frac{\partial}{\partial x^k}$$
Where $\Gamma_{ij}^k$ are the Levi-Civita connection coeffecients and
are completely determined by the metric.
$$\Gamma _{ij}^{k}={\tfrac {1}{2}}g^{mk}\left(
 \frac{\partial g_{im}}{\partial x^j}
 + \frac{ \partial g_{jm}}{\partial x^i}
 -\frac{partial g_{ij}}{\partial x ^m}\right)$$

$$g_{ij} = g(\frac{\partial}{\partial x^i}, \frac{\partial}{\partial x^j})$$

The term covariant derivative is often used for the Levi-Civita
connection. The coefficients of this connection with respect to a system
of local coordinates are called Christoffel symbols.

## Curvature

Recall $L_[X,Y] = [L_X, L_Y]$. If $[X,Y]=0$ commutes, then
$L_X L_Y - L_Y L_X = 0$ This fails in general for the covariant
derivative. This failure is measured by a tensor field that plays a
central role in all of differential geometry.

$$R(X,Y) Z = \delta_X \delta_Y Z - \delta_Y \delta_X Z - \delta_[X,Y] Z$$

This is a (1, 3) tensor field which can be proven by showing that $R$ is
$C^\infty$-linear with respect to each component.

# Lie Groups

See notebook on Lie Groups

https://github.com/lukepereira/notebooks/

E. Meinrenken and G. Gross, Introduction to Differential Geometry,
Lecture Notes for MAT367.

Samelson, H. Review: Werner Greub, Stephen Halperin and Ray Vanstone,
Connections, curvature, and cohomology. Bull. Amer. Math. Soc. 83
(1977), no. 5, 1011--1015.
https://projecteuclid.org/euclid.bams/1183539466

Paul Seidel. 18.950 Differential Geometry. Fall 2008. Massachusetts
Institute of Technology: MIT OpenCourseWare, https://ocw.mit.edu.
License: Creative Commons BY-NC-SA.

Sigurdur Helgason. 18.755 Introduction to Lie Groups. Fall 2004.
Massachusetts Institute of Technology: MIT OpenCourseWare,
https://ocw.mit.edu. License: Creative Commons BY-NC-SA.
