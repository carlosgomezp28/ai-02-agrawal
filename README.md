# Repository 2 — Agrawal, Gans & Goldfarb (2025)

Agrawal, A. K., Gans, J. S., & Goldfarb, A. (2025), “The Economics of Bicycles for the Mind,” *NBER Working Paper 34034*.

## 1. Economic question

The paper asks how cognitive tools—especially computers and AI—change effort, productivity, and inequality when work is an iterative process of finding and implementing improvements. Its central distinction is between three human capabilities:

- **Implementation skill** (`s`): how effectively effort is converted into successful execution.
- **Opportunity judgment** (`rho(t)`): the ability to notice another opportunity to improve the task.
- **Payoff judgment** (`eta`): the ability to recognize or choose the valuable action after implementation succeeds.

A cognitive tool can substitute for implementation skill by raising success or lowering cost at a given effort while reducing the marginal return to additional human effort. The worker then optimally supplies less implementation effort, even though net output rises. Judgment is different: opportunity judgment supplies more occasions on which the tool can be used and is therefore complementary. Payoff judgment is complementary only when tool adoption raises equilibrium implementation success; its direct technological benefit can be offset by the induced fall in effort.

## 2. Core model

Conditional on perceiving an opportunity, the agent receives net benefit

```math
M(e;\theta)=p(se;\theta)\eta\Delta-c(e;\theta),
```

where `e` is effort, `s` is implementation skill, `theta` is tool quality, `eta` is payoff judgment, and `Delta` is the value of a realized improvement. The agent solves

```math
e(\theta)\in\arg\max_{e\geq 0}\left\{p(se;\theta)\eta\Delta-c(e;\theta)\right\}.
```

For an interior optimum, the first-order condition is

```math
p_x(se;\theta)s\eta\Delta=c_e(e;\theta).
```

In period `t`, an opportunity is perceived with probability `rho(t)`. If none is perceived, the improvement process ends. With initial probability `rho_0`, constant later probability `rho`, and discount factor `delta`, time-invariant optimal effort gives

```math
\begin{aligned}
V_0(\theta)
&=\rho_0M(e(\theta);\theta)
\left[1+\rho\delta+(\rho\delta)^2+\cdots\right]\\
&=\frac{\rho_0}{1-\rho\delta}M(e(\theta);\theta),
\end{aligned}
```

provided `rho delta < 1`.

## 3. Proposition 1

A cognitive tool weakly raises `p` and weakly lowers `c` at every effort, with a strict direct improvement, and makes the marginal-benefit-to-marginal-cost ratio

```math
R(e,\theta)=\frac{p_x(se;\theta)}{c_e(e;\theta)}
```

strictly decreasing in `theta`. With concave success, convex cost, an interior solution, and enough strictness for a unique comparison, the tool lowers optimal implementation effort and raises continuation value:

```math
e(1)<e(0),
\qquad
V_0(1)>V_0(0).
```

The FOC fixes the ratio at

```math
R(e(\theta),\theta)=\frac{1}{s\eta\Delta}.
```

At the old effort, adoption lowers `R`. Because `R` also decreases with effort, effort must fall to restore the FOC. Nevertheless,

```math
M(e(1);1)\geq M(e(0);1)>M(e(0);0),
```

so the optimized per-opportunity benefit and total continuation value rise.

## 4. Proposition 2 — who benefits from the tool?

Let

```math
\Gamma=\sum_{t=0}^{\infty}
\left(\prod_{i=0}^{t}\rho(i)\right)\delta^t
```

and define the adoption gain

```math
D=V_0(1)-V_0(0)
=\Gamma\left[M^*(1)-M^*(0)\right]>0.
```

### Opportunity judgment

Opportunity judgment is always complementary: increasing an opportunity probability raises `Gamma` and creates more occasions to earn the positive per-opportunity adoption gain. Earlier opportunities matter more because they affect more continuation terms and are less heavily discounted.

### Implementation skill

Implementation skill substitutes for the tool when

```math
p_{s\theta}(se;\theta)<0.
```

Under this cross-partial condition, higher tool quality reduces the marginal productivity of implementation skill, so

```math
\frac{\partial D}{\partial s}<0.
```

### Payoff judgment

Payoff judgment is only conditionally complementary. For optimized net benefit,

```math
\begin{aligned}
\frac{dM^*}{d\eta}
&=M_\eta+M_e e_\eta\\
&=p(se(\theta);\theta)\Delta,
\end{aligned}
```

because `M_e = 0` at the optimum. Therefore,

```math
\frac{dD}{d\eta}
=\Gamma\Delta
\left[p(se(1);1)-p(se(0);0)\right].
```

The sign is ambiguous: the tool directly raises implementation performance, but it also lowers effort. Payoff judgment complements adoption if and only if the direct tool effect is large enough that equilibrium success probability does not fall.

## 5. Proposition 3 — inequality

Section 4 specializes the model to

```math
p(se;\theta)=\sqrt{se+\theta},
\qquad
c(e)=e.
```

The FOC is

```math
\frac{\eta s}{2\sqrt{se+\theta}}=1,
```

which yields

```math
e(\theta)=\frac{\eta^2s}{4}-\frac{\theta}{s}.
```

This interior formula is valid only when

```math
\eta^2s^2>4\theta.
```

With the opportunity multiplier

```math
G=\frac{\rho_0}{1-\rho\delta},
```

continuation value is

```math
V(\theta)=G\left[\frac{\eta^2s}{4}+\frac{\theta}{s}\right].
```

The term `theta/s` gives a larger tool boost to workers with low implementation skill, while `G` makes the benefit larger for workers with stronger opportunity judgment.

Under the paper's independence assumptions, the variance derivative is

```math
\frac{d\operatorname{Var}(V(\theta))}{d\theta}
=a_0+2\theta\operatorname{Var}(G/s),
```

where

```math
a_0=
\frac{E[\eta^2]}{2}
\left[
E[G^2]-(E[G])^2\bar{s}E[1/s]
\right].
```

Condition (30) is

```math
\frac{E[G^2]}{(E[G])^2}
<\bar{s}E[1/s].
```

It implies `a_0 < 0`, so variance initially falls. Moreover,

```math
\frac{d^2\operatorname{Var}(V(\theta))}{d\theta^2}
=2\operatorname{Var}(G/s)\geq 0,
```

so variance is convex on the common interior-solution domain. A genuine interior U-shape additionally requires

```math
\theta^*=
\frac{E[\eta^2]}{4}
\frac{(E[G])^2\bar{s}E[1/s]-E[G^2]}
{\operatorname{Var}(G/s)}
```

to lie inside that domain. Condition (30) makes `theta*` positive; it does not by itself establish an unconditional or global U-shape.

## 6. Variance of individual benefits

Individual `i`'s benefit relative to no tool is

```math
B_i(\theta)=V_i(\theta)-V_i(0)=\theta\frac{G_i}{s_i}.
```

Hence

```math
\operatorname{Var}(B(\theta))
=\theta^2\operatorname{Var}(G/s),
```

and

```math
\frac{d\operatorname{Var}(B(\theta))}{d\theta}
=2\theta\operatorname{Var}(G/s)\geq0.
```

Benefit variance rises monotonically for positive `theta` when `G/s` is heterogeneous. Total-value variance can nevertheless fall initially because the unequal benefits may be negatively correlated with baseline productivity: low-implementation-skill workers receive the larger boosts.

## 7. Where I did not believe the LLM

The LLM initially described the variance as globally U-shaped on `[0, infinity)`. After being challenged about interiority and equation (32), it retracted that statement. The formula

```math
e(\theta)=\frac{\eta^2s}{4}-\frac{\theta}{s}
```

can be used only while effort remains positive for the relevant individuals. The verified conclusion is convexity on the common interior-solution domain; an interior U-shape requires `theta*` to fall inside that domain.

The referee check also found that equation (32)'s positive derivative at `theta = 1` does not follow solely from condition (30) under the reconstructed assumptions: it additionally requires `theta* < 1` and validity of the interior solution through one. This is a referee concern about the stated conditions, not a definitive declaration that the paper contains an error.

A suspected typo in the paper's coefficient-of-variation definition was also retracted. PDF text extraction can omit square-root signs, so the available extracted text was insufficient to verify that the typeset paper actually omitted one.

## 8. Main takeaway

AI does not simply substitute for “skill.” It substitutes for implementation capability while changing the value of judgment. Productivity and inequality therefore depend on whether heterogeneity lies primarily in implementation skill, opportunity judgment, or payoff judgment—and on whether workers remain at interior effort choices as the tool improves.

## Repository contents

| Path | Contents |
|---|---|
| `README.md` | Weekly model summary, derivations, and referee check |
| `prompts.md` | LLM prompts and responses |
| `hand/` | Handwritten derivation material |
| `presentation.tex` | Source for the five-minute presentation |
| `presentation.pdf` | Compiled five-minute presentation |
| `paper/` | The paper and related paper notes |
