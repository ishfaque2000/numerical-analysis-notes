# 📘 Numerical Analysis Notes
## ✨ Based on Burden & Faires

> 🎓 **Sukkur IBA University** &nbsp;|&nbsp; 📐 Numerical Methods &nbsp;|&nbsp; 🗓️ 2025

---

# 1️⃣ Root Finding Methods &nbsp; 🔍

## 🔹 Bisection Method

Used to find roots in interval $[a, b]$.

**Condition:** $f(a) \cdot f(b) < 0$

### Formula:

$$
c = \frac{a + b}{2}
$$

### Steps:
1. Check sign change
2. Compute midpoint
3. Replace interval
4. Repeat

### Error:

$$
\left|\text{error}\right| \leq \frac{b - a}{2^n}
$$

---

## 🔹 Newton-Raphson Method &nbsp; ∫

### Formula:

$$
x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}
$$

### Features:
- Fast (quadratic) convergence
- Requires derivative $f'(x)$

### Error:

$$
|e_{n+1}| = O\!\left(e_n^2\right)
$$

---

## 🔹 Secant Method &nbsp; √

### Formula:

$$
x_{n+1} = x_n - f(x_n) \cdot \frac{x_n - x_{n-1}}{f(x_n) - f(x_{n-1})}
$$

### Features:
- No derivative needed
- Faster than Bisection (superlinear convergence)

---

# 2️⃣ Interpolation &nbsp; 📊

## 🔹 Lagrange Interpolation

### Formula:

$$
P(x) = \sum_{i=0}^{n} f(x_i)\, L_i(x)
$$

Where:

$$
L_i(x) = \prod_{\substack{j=0 \\ j \neq i}}^{n} \frac{x - x_j}{x_i - x_j}
$$

---

## 🔹 Newton's Divided Difference Interpolation

### Formula:

$$
P(x) = f[x_0] + f[x_0, x_1](x - x_0) + f[x_0, x_1, x_2](x - x_0)(x - x_1) + \cdots
$$

### First-Order Divided Difference:

$$
f[x_i,\, x_{i+1}] = \frac{f(x_{i+1}) - f(x_i)}{x_{i+1} - x_i}
$$

---

# 3️⃣ Numerical Differentiation &nbsp; 𝑑/𝑑𝑥

## 🔹 Finite Difference Formulas

All formulas are derived from the Taylor Series expansion.

---

### Forward Difference &nbsp; ➡️

$$
f'(x_0) \approx \frac{f(x_0 + h) - f(x_0)}{h}, \qquad O(h)
$$

---

### Backward Difference &nbsp; ⬅️

$$
f'(x_0) \approx \frac{f(x_0) - f(x_0 - h)}{h}, \qquad O(h)
$$

---

### Centered Difference &nbsp; ↔️

$$
f'(x_0) \approx \frac{f(x_0 + h) - f(x_0 - h)}{2h}, \qquad O(h^2)
$$

---

### Three-Point Endpoint Formula &nbsp; 📍

$$
f'(x_0) \approx \frac{-3f(x_0) + 4f(x_0 + h) - f(x_0 + 2h)}{2h}, \qquad O(h^2)
$$

---

### Five-Point Midpoint Formula &nbsp; ⭐

$$
f'(x_0) \approx \frac{f(x_0 - 2h) - 8f(x_0 - h) + 8f(x_0 + h) - f(x_0 + 2h)}{12h}, \qquad O(h^4)
$$

---

# 4️⃣ Numerical Integration &nbsp; ∑

## 🔹 Trapezoidal Rule &nbsp; 📐

$$
\int_a^b f(x)\,dx \approx \frac{h}{2}\bigl[f(a) + f(b)\bigr]
$$

where $h = b - a$.

---

## 🔹 Simpson's $\tfrac{1}{3}$ Rule &nbsp; 📐📐

$$
\int_a^b f(x)\,dx \approx \frac{h}{3}\bigl[f(x_0) + 4f(x_1) + f(x_2)\bigr]
$$

where $h = \dfrac{b - a}{2}$, $\;x_0 = a$, $\;x_1 = \tfrac{a+b}{2}$, $\;x_2 = b$.

---

## 🔹 Simpson's $\tfrac{3}{8}$ Rule &nbsp; 📐📐📐

$$
\int_a^b f(x)\,dx \approx \frac{3h}{8}\bigl[f(x_0) + 3f(x_1) + 3f(x_2) + f(x_3)\bigr]
$$

where $h = \dfrac{b - a}{3}$.

---

# 🎯 Key Takeaways

- Smaller $h$ gives better accuracy
- Centered formulas are more accurate than forward/backward
- Higher-order methods give higher accuracy
- Tradeoff: Accuracy vs. Computation

---

# 🚀 End of Notes

---

<br>

> | | |
> |---|---|
> | ✍️ **Author** | Ishfaque Ahmed |
> | 🎓 **Institution** | Sukkur IBA University |
> | 📅 **Date** | 2025 |
> | 📘 **Reference** | Burden & Faires — *Numerical Analysis* |
