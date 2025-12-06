---
title: MA274 Final Project: Russell's Paradox and The Halting Problem
author: [Tin Nguyen, Rafay] 
date: 2025-11-22
tags: [ma274, math, cs, marp]
marp: true
theme: academic
paginate: true 
math: katex
---

<!-- _class: lead -->

# Embrace the Unknown: <br> Russell's Paradox <br> and The Halting Problem

#### 〜MA274 Final Presentation〜

<br>

Rafay Abid 
Tin Nguyen 

---

<!-- _header: Table of Contents -->

1. Russell's Paradox
1. The Halting Problem
1. 🤯🤯🤯 They're the same?
1. Math is broken ヽ(º ■ º l|l)ﾉ
1. Math is fixed ヽ(・∀・)ﾉ (mostly (ヽ(º ■ º l|l)ﾉ))

---

<!-- _header: BIG Questions -->

1. Can there be one perfect theory of all sets or all programs?
2. What happens when a system talks about itself.
3. Russell’s Paradox → flaw in early set theory.
4. Halting Problem → limit on what computers can decide.

**Our claim:** they are two versions of the same self-reference problem.

---

<!-- _header: Naive Picture of Sets -->

- A set = a collection of objects
    - e.g. set of all cats, set of all even numbers
- Sets can contain other sets as elements.
- Question: can a set contain itself?
- The set of all cats does not contain itself (it’s not a cat).
- Tempting idea: consider the set of all sets that do not contain themselves…

---

<!-- _header: The Russell Set -->

Let $R = \{ X : X ∉  X \}$. Then consider $R ∈ R?$

**Case 1** $R ∈ R$ Then by definition, $R ∉ R \quad ↯$

**Case 2** $R ∉  R$ Then by definition, $R ∈ R \quad ↯$


---

<!-- _header: The Halting Problem: Motivating Question -->

_The inifinite loop is a common bug. Can I write a program to detect if a given program and input will continue to run forever or not (halt)?_

---

<!-- _header: The Halting Problem: Motivating Question -->

_The inifinite loop is a common bug. Can I write a program to detect if a given program and input will continue to run forever or not (halt)?_

**Proposition: No** 

---

<!-- _header: The Halting Problem: Proof -->

Suppose such a program exists, call it $H$:

$H: \{P, I\} →  \{True, False\}$ s.t. \
$H(P, I) =$ _<$P(I)$ halts?>_

Then, define program $R$ s.t.

$R: \{Programs\} →  \{True, False\}$ s.t. \
$R(P)$ halts $\iff$ $H(P, P)$ loops forever \
$R(P)$ loops $\iff$ $H(P, P)$ halts

---

<!-- _header: The Halting Problem: Proof -->

Finally, consider $R(R)$ 

**Case 1:** $R(R)$ halts, \
so $H(R, R) = True$, \
so $R(R)$ loops forever $\quad ↯$.

**Case 2:** $R(R)$ loops forever, \
so $H(R, R) = False$, \
so $R(R)$ halts $\quad ↯$. 

<!-- **Proof by contradiction:**  -->
<!-- Suppose such a program exists, call it `CheckHalt` -->
<!---->
<!-- ```lua  -->
<!-- function CheckHalt(P, X) -->
<!--     if P(X) halts then  -->
<!--         print 'HALTS'  -->
<!--     else -->
<!--         print 'LOOPS FOREVER' -->
<!--     end -->
<!-- end -->
<!-- ``` -->
<!---->
<!-- Note: We can run `CheckHalt(P, P)` -->
<!---->
<!-- --- -->
<!---->
<!-- <!-- _header: The Halting Problem: Proof (cont.) --> -->
<!---->
<!-- Then, define the following program: -->
<!---->
<!-- ```lua  -->
<!-- function Russell(P) -->
<!--     if CheckHalt(P, P) prints "HALTS" then  -->
<!--         while true -- loops forever -->
<!--     else if CheckHalt(P, P) prints "LOOPS FOREVER" then -->
<!--         end  -->
<!--     end -->
<!-- end -->
<!-- ``` -->
<!---->
<!-- --- -->
<!---->
<!-- <!-- _header: The Halting Problem: Proof (cont.) --> -->
<!---->
<!-- Now, we consider -->
<!---->
<!-- ```lua  -->
<!-- function Russell(P) -->
<!--     if CheckHalt(P, P) prints "HALTS" then  -->
<!--         while true -- loops forever -->
<!--     else if CheckHalt(P, P) prints "LOOPS FOREVER" then -->
<!--         end  -->
<!--     end -->
<!-- end -->
<!-- ``` -->

---

<!-- _header: Math is broken ヽ(º ■ º l|l)ﾉ -->

- ~1900: goal = set-theoretic foundation for all of math.
- Early set theory allowed: “any property gives a set.”
- Russell’s paradox made this system is inconsistent.
- In an inconsistent logic, you can in principle prove anything.
- Mathematics would lose its reliability.
- Forced a foundational crisis:
    - Which collections should count as sets?
    - How do we control self-reference and “too big” sets?

---

<!-- _header: Math is fixed ヽ(・∀・)ﾉ (kind of): Response of Set Theorists -->

**Strategy:** restrict which sets exist.
- Not every property gets a set.

**Zermelo–Fraenkel Set Theory (ZF/ZFC):** 
- Uses specific axioms to build sets in stages from older sets.
- No “set of all sets” ⇒ Russell set cannot be formed.
- Replaces unrestricted comprehension with safer separation axioms.
**Type Theory:** 
- Organizes objects into levels/types.
- A set at one level only contains objects from lower levels.
- A set can never contain itself, so Russell-style sets are impossible
