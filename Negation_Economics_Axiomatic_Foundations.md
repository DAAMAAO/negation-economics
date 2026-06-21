<div class="titlepage">

# Axiomatic Foundations of Negation-based Economics: From Parsing Operators to Asset Pricing

​                                                           **Mao Jianyu**

​                                                 Independent Researcher

​                                                       **Date:** June 2026  


## Abstract

Negation-based Economics proposes a core proposition distinct from mainstream asset pricing theory: the value of an asset does not reside in its own attributes, but in its relations of exclusion against alternatives. This paper establishes the axiomatic foundation of this proposition. Five core axioms form a complete generative chain from "parsing" to "value." We introduce the parsing operator, the negation channel, and channel closure as core mathematical objects, and formulate the Asset Generation Condition, the Negation-based Representation of Value, and the Negation-based Representation of Pricing. The axiomatic path is independent of traditional economics' reliance on historical transaction data and probability distributions, providing a unified mathematical foundation for treating emerging economic objects not yet assetized—low-altitude airspace, data assets, carbon emission allowances.

**Keywords:** Negation-based Economics; Axiomatization; Parsing Operator; Negation Channel; Asset Pricing

AI Disclosure: The core research question, theoretical framework, axiom system, core concepts (including the parsing operator, negation channel, and channel closure), and all principal arguments of this paper were independently proposed by the author. During the writing process, the author engaged in multi-round dialogue with an AI tool (DeepSeek) for: ① clarifying and refining argumentation logic; ② optimizing terminology selection (e.g., adjusting "partitioning" to "parsing" to strengthen the analogy with linguistics); ③ designing the parameters and structure of the numerical example; and ④ performing English translation and language polishing. The AI did not participate in the generation of core ideas or the construction of the theoretical framework. The author bears full responsibility for the entire content of this paper.

<div class="body-start">

## Notation

| Symbol | Meaning |
|:---|:---|
| Ω | State space — the set of all possible states of an economic system |
| P | Parsing operator — partitions Ω into discrete units |
| Bᵢ | Parsed unit i — a discrete, identifiable subspace of Ω |
| ¬Bᵢ | Complement of Bᵢ — all states excluded from Bᵢ |
| ∂Bᵢ | Boundary of Bᵢ — the interface between Bᵢ and ¬Bᵢ |
| C | Negation channel — the triple (∂B, V, T) |
| V(s) | Verifiability function — V(s) ∈ {0,1}, whether state s satisfies entry conditions |
| T | Transferability function — governs circulation of boundary entry rights |
| Aᵢ | Asset — the ordered pair (Pᵢ, ∂Bᵢ) |
| V(Aᵢ) | Value of asset Aᵢ |
| w(s) | Exclusion intensity at state s |
| u(s) | Economic unacceptability of state s as an alternative |
| H(C) | Channel hardness — D(C) × L(C) |
| D(C) | Demand base scale for the channel |
| L(C) | Legal guarantee strength for the channel |
| p | Market price (lowercase; not to be confused with P) |

**Note:** Uppercase P denotes the parsing operator; lowercase p denotes market price. Uppercase V(Aᵢ) denotes asset value; V(s) denotes the verifiability function on states.
| I(·) | Indicator function |
| E[·] | Statistical expectation |


## 1. Introduction

### 1.1 Problem Statement

​     Standard economics, when addressing the question "what is an asset," tacitly assumes that the asset already exists. Asset valuation relies on historical transaction data. Insurance actuarial methods rely on historical claims data. Derivatives pricing relies on the market price of the underlying. From Marshall's supply-demand curves to Walras's general equilibrium, from Fisher's discounted cash flow to Black-Scholes option pricing, this framework shares an unexamined premise: **the object under analysis is already an asset.**

​     This premise is self-consistent when applied to traditional asset classes—land, stocks, bonds, commodities—that have been operating stably for centuries. But when entirely new, not-yet-priced objects emerge—low-altitude airspace, large-scale datasets, carbon emission allowances—the standard framework exposes a structural blind spot. These objects exist physically but have not yet been born as economic assets.

​     Negation-based Economics (Mao, 2026) proposes the following core proposition: the economic determinacy of an asset does not reside in its physical or legal attributes, but in its relation of negation—its "not being" other alternatives. The economic value of a low-altitude logistics air route does not reside in the thermodynamic or electromagnetic properties of the airspace itself, but in the time differential of "one hour is not four hours." This proposition opens the possibility of treating emerging assets without waiting for historical data to accumulate. But it has hitherto lacked rigorous mathematical formalization. The goal of this paper is to establish an axiomatic foundation.

### 1.2 Scope and Positioning

​     This paper establishes the axiomatic skeleton—the logical chain from parsing to pricing. Rigorous mathematical proofs of the theorems, statistical identifiability of parameters, and large-scale empirical validation are left for future work. The present version is suitable for academic discussion and invites formalization efforts from the community.

### 1.3 Relation to Existing Literature

​     This paper sits at the intersection of three research traditions.

**Asset pricing theory** (Fisher, 1930; Markowitz, 1952; Black & Scholes, 1973) provides the standard toolkit for valuing assets that already exist and generate observable cash flows or market prices. The negation-based framework does not compete with this tradition—it addresses a logically prior question: under what conditions does an object *become* an asset in the first place? Traditional pricing theory begins where the Asset Generation Condition ends.

**Institutional economics** (Coase, 1937; North, 1990) has long recognized that property rights and transaction costs determine market boundaries. The negation channel formalizes a specific mechanism within this tradition: how institutions manufacture assets by closing the three lock-tongues of exclusivity, verifiability, and transferability. The process of "assetization"—transforming non-market objects into tradable financial assets (Krippner, 2005; Pistor, 2019)—finds an operational criterion in channel closure.

**The economics of low-altitude airspace** is an emerging field with no canonical pricing methodology. Existing approaches typically borrow land valuation frameworks or spectrum auction models. Both fail because airspace lacks the positive attributes—location, fertility, bandwidth—that anchor those frameworks. The negation-based approach replaces the question "what attributes does this airspace have?" with "what slower alternatives does this route exclude?"


## 2. Fundamental Objects and Definitions

### 2.1 State Space

​     Let Ω denote the set of all possible states of a given economic system. The state space in its natural state is continuous and undifferentiated. A continuum cannot be directly processed by economic institutions—law, property rights, and pricing all require that the object has already been partitioned into discrete, manageable units.

### 2.2 The Parsing Operator

**Definition 1 (Parsing Operator).** A parsing operator P is a mapping: P: Ω → {B₁, B₂, ..., Bₙ}, satisfying: (1) Completeness: ∪ᵢ Bᵢ = Ω; (2) Mutual exclusivity: Bᵢ ∩ Bⱼ = ∅ for i ≠ j; (3) Identifiability: for any Bᵢ, there exists a unique identifier ID(Bᵢ) and attribute labels A(Bᵢ).

The term "parsing" is chosen deliberately. In linguistics, parsing is the operation that decomposes a continuous stream of speech into discrete syntactic constituents—without parsing, there is no grammar, no meaning, no language. The economic parsing operator performs an analogous function: it decomposes a continuous state space into discrete, nameable units. Without parsing, there is no economic grammar—no property rights, no contracts, no prices. The choice of "parsing" over "partitioning" reflects this deeper analogy: both operations are prerequisites for a system of signification to emerge.

**Proposition 1 (Parsing Priority).** Parsing is logically prior to pricing and trading.

### 2.3 Boundary and Negation

**Definition 2 (Boundary).** For any parsed unit Bᵢ, its boundary ∂Bᵢ = Ω − Bᵢ. The essence of a boundary is exclusion.

**Definition 3 (Negation Channel).** A negation channel C = (∂B, V, T), where V is a verifiability function and T is a transferability function.


## 3. The Axiom System

### 3.1 Five Core Axioms

| Axiom | Formal Statement | Economic Correspondence |
|:---|:---|:---|
| **A1. Parsing Axiom** | Asset ⇒ Parsing | Assets must originate from parsing. Airspace must be gridded before it can become a route asset. |
| **A2. Boundary Axiom** | Parsing ⇒ Boundary | Parsing inevitably generates boundaries. Boundary = identifiability. |
| **A3. Negation Axiom** | Essence of boundary = exclusion | "Determination is negation." Value does not come from "what something has." |
| **A4. Asset Axiom** | A = (P, ∂B) | An asset = parsing right + boundary. |
| **A5. Value Axiom** | V(A) = g(intensity(∂B), unacceptability(¬B)) | Value depends on exclusion intensity × unacceptability of excluded alternatives. |

**The Generative Chain:** Parsing → Boundary → Negation → Asset → Value → Price

### 3.2 Elaboration of the Axioms

**Axiom 1 (Parsing).** An asset is manufactured, and the first step is parsing. A plot of land must be partitioned by cadastral survey. Spectrum must be partitioned into frequency bands. Airspace must be gridded—space into cells, time into windows. That which is unparsed cannot be titled or priced.

**Axiom 2 (Boundary).** Boundaries produce identifiability. Without them, rights cannot be allocated. Land rights: "from here it is no longer yours." Airspace rights: "from this altitude you may not fly."

**Axiom 3 (Negation).** The hard core. A route's value does not originate from the airspace itself, but from its exclusion of ground transport. Land's value does not originate from fertility, but from excluding others.

**Axiom 4 (Asset).** An asset = parsing right (birth certificate) + boundary (scope of exclusion). Absent either, the asset is not constituted.

**Axiom 5 (Value).** Desert land: high exclusion intensity × low unacceptability = low value. City land: high exclusion intensity × high unacceptability = high value. Agricultural drone airspace: low. Cold-chain pharma airspace: high.


## 4. Core Theorems

### 4.1 Asset Generation Condition: Channel Closure

**Definition 4 (Channel Closure).** A negation channel C = (∂B, V, T) is **closed** iff: (1) Exclusivity: ∃s ∈ ¬B, V(s)=0; (2) Verifiability: ∀s, V(s)∈{0,1} independently verifiable; (3) Transferability: ∃T for reallocating entry rights.

**Theorem 1 (Asset Generation Condition).** A becomes an asset ⇔ C is closed.

**Proof sketch.** (⇒) Asset ⇒ excludable, verifiable, transferable ⇒ three closure conditions hold. (⇐) C closed ⇒ scarcity (exclusivity) + contract enforcement (verifiability) + market exchange (transferability) ⇒ A is a tradable economic asset. A formal proof with explicit counterfactual construction is in Appendix A.

**Corollary 1 (Channel Degeneration).** Any single lock-tongue failure ⇒ A degenerates to non-asset.

### 4.2 The Negation-based Representation of Value

**Theorem 2 (Value Representation).** Let w, u be bounded measurable functions on ¬B. Then the value of asset A is:

$$
V(A) = ∫_{s∈¬B} w(s) × u(s) ds
$$
where w(s) ∈ [0,1] is exclusion intensity at state s, and u(s) ≥ 0 is the economic unacceptability of s as an alternative.

**Remarks on the integral.** The boundedness of w and u on ¬B ensures the integral exists as a Lebesgue integral. In applied settings, ¬B is typically finite (a discrete set of alternative transport modes, routes, or products), reducing the integral to a finite sum. The function space assumptions are mild and hold for any empirically estimable w and u. A derivation sketch and a numerical example are provided in Appendix B.

### 4.3 The Negation-based Representation of Pricing

**Theorem 3 (Pricing Representation).** Let there be N market participants indexed by j = 1,...,N. Each participant j forms a subjective assessment of the exclusion intensity wⱼ(s) and unacceptability uⱼ(s). Let Iⱼ(s∉B) indicate participant j's individual negation decision (1 = "the alternative is unacceptable, I must use B"). The market price p is:

$$
p = E[I(s∉B)] × ū
$$
where the expectation E[·] is taken over the equilibrium distribution of individual negation decisions in the market, and ū = (1/N) Σⱼ uⱼ is the average unacceptability across participants. A microfoundation sketch deriving this from individual decisions to market aggregation is in Appendix B.

**Economic meaning.** Price rising = fewer people saying "won't buy." Price falling = more people saying "won't buy." The market price is not a measure of value—it is the statistical aggregate of collective negation. Hayek's "prices convey knowledge" finds its precise correspondence: prices convey changes in collective negation intensity.

### 4.4 Value and Price: Relationship and Distinction

​     Theorem 2 defines **value** V(A) as a technical construct—a function of the exclusion technology (w) and the objective unacceptability of alternatives (u). Theorem 3 defines **price** p as a market equilibrium outcome—a function of subjective individual negation decisions aggregated through exchange.

​     The two are not identical in general. Value is a property of the asset's negation channel; price is a property of the market's collective negation decisions. Differences arise from transaction costs, information asymmetries, and market power. In the frictionless limit—perfect competition, complete information, no transaction costs—we conjecture that p → V(A) as N → ∞. Proving this convergence is left for future work.

### 4.5 Comparison with Standard Pricing Theory

​     Traditional pricing: V = ΣCFₜ/(1+r)ᵗ assumes the asset already exists. Negation-based pricing: inserts a prior step—confirm channel closure before valuation.


## 5. Conclusion and Outlook

​     This paper established the axiomatic foundations of Negation-based Economics. Five axioms form the generative chain Parsing → Boundary → Negation → Asset → Value. The Asset Generation Condition provides necessary and sufficient conditions for asset constitution. The Value Representation anchors value in exclusion intensity, not internal attributes. The Pricing Representation reinterprets prices as collective negation statistics.

​     Future work: (1) Rigorous mathematical proofs, including convergence of p → V(A); (2) Multi-channel coupling optimization; (3) Empirical validation using mandatorily collected flight data.

​     The axiomatization responds to a substantive challenge: **if "the asset already exists" is abandoned, can economics remain rigorous?** Yes—with the Parsing Axiom added.


## Appendix A: Formal Proof of Theorem 1

**Proof of (⇒).** Assume A is an asset. Construct C = (∂B, V, T). ∂B is well-defined (Axiom 1). V(s) = 1 if s satisfies entry conditions. T is A's ownership transfer mechanism. Since A is an asset: ownership is enforceable → V(s) publicly verifiable (verifiability closure); A is scarce → ∃s with V(s)=0 (exclusivity closure); A is tradable → T exists (transferability closure). ∴ C is closed.

**Proof of (⇐).** Assume C is closed. Exclusivity → B not universally accessible → scarcity. Verifiability → contract enforcement and dispute resolution possible. Transferability → market exchange enabled. ∴ A meets the definition of a tradable economic asset. 

**Counterfactual analysis.** Dropping exclusivity → public good. Dropping verifiability → unenforceable ownership. Dropping transferability → no market. Each single failure destroys asset status.


## Appendix B: Derivation Sketches and Numerical Example

### B.1 Derivation Sketch for Theorem 2 (Value Integral)

​     Consider an asset A with boundary ∂B. For each excluded state s ∈ ¬B, two things matter: how strongly it is excluded (w(s)) and how much an economic agent would suffer if forced to use s instead of B (u(s)). The total value of A is the sum—over all excluded alternatives—of "how much exclusion" times "how bad the alternative is."

​     When ¬B is discrete (the typical applied case—a finite set of alternative routes or products): V(A) = Σ_{s∈¬B} w(s) × u(s). When ¬B is continuous, the sum becomes an integral. The boundedness of w and u ensures convergence. In practice, w(s) can be estimated from utilization rates and enforcement costs; u(s) can be estimated from the price and time differential between B and each alternative s.

### B.2 Derivation Sketch for Theorem 3 (Pricing Microfoundation)

​     Consider N market participants. Each participant j faces a binary choice: use asset B (pay its price p) or use an alternative s ∈ ¬B (incur unacceptability uⱼ(s) weighted by how strongly s is excluded, wⱼ(s)).

​     Participant j chooses B if and only if: p ≤ wⱼ(s) × uⱼ(s) for the best available alternative s. Equivalently, participant j says "no" to the alternative (Iⱼ(s∉B) = 1) when the alternative's effective cost exceeds the price of B.

​     Aggregating across all participants: the proportion choosing B = (1/N) Σⱼ Iⱼ(s∉B) = E[I(s∉B)]. Market clearing requires supply = demand at price p, yielding p = E[I] × ū where ū is the average unacceptability. The expectation is taken over the cross-sectional distribution of (wⱼ, uⱼ) in the market at equilibrium.

​     This is a sketch; a full derivation would specify the distribution of types, the supply side, and the equilibrium selection mechanism.

### B.3 Numerical Example

Consider a low-altitude air route B connecting two cities. There are two excluded alternatives: ground trucking (s₁) and high-speed rail (s₂).

**Parameters (hypothetical):**

| Alternative | Exclusion intensity w(s) | Unacceptability u(s) | w × u |
|:---|:---:|:---:|:---:|
| Ground trucking (s₁) | 0.9 | 80 (time cost in equivalent monetary units) | 72 |
| High-speed rail (s₂) | 0.6 | 30 (schedule inflexibility cost) | 18 |

**Value:** V(A) = 72 + 18 = 90 (in equivalent monetary units per use).

​     Suppose there are 100 shippers. 60 have high time sensitivity (u₁=80), 40 have moderate sensitivity (u₁=30). With w(s₁)=0.9, the high-sensitivity shippers all find the alternative unacceptable (I=1); the moderate group is split—20 find it unacceptable, 20 accept the alternative. E[I] = (60+20)/100 = 0.8. ū (weighted by which alternative is the binding constraint for each shipper) ≈ 65. **Price:** p = 0.8 × 65 = 52.

​     Note that price (52) < value (90). The gap (38) reflects that some shippers accept alternatives even though those alternatives have positive unacceptability—the market does not capture the full exclusion value. In the limit where all shippers find all alternatives maximally unacceptable, E[I] → 1 and p → V(A).


---

**References**

[1] Knight, F. H. (1921). *Risk, Uncertainty and Profit*.
[2] Fisher, I. (1930). *The Theory of Interest*.
[3] Coase, R. H. (1937). The Nature of the Firm. *Economica*.
[4] Hayek, F. A. (1945). The Use of Knowledge in Society. *American Economic Review*.
[5] Markowitz, H. (1952). Portfolio Selection. *Journal of Finance*.
[6] North, D. C. (1990). *Institutions, Institutional Change and Economic Performance*.
[7] Black, F. & Scholes, M. (1973). The Pricing of Options and Corporate Liabilities. *Journal of Political Economy*.
[8] Krippner, G. R. (2005). The Financialization of the American Economy. *Socio-Economic Review*, 3(2), 173–208.
[9] Pistor, K. (2019). *The Code of Capital: How the Law Creates Wealth and Inequality*. Princeton University Press.
[10] Mao, J. (2026). *Negation-based Economics: An Introduction*. Forthcoming.
[11] Mao, J. (2026). *A General Treatise on Negation-based Economics*. In preparation.

---

June 2026 
