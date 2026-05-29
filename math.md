# 📐 Mathematics & Statistics — Expanded Crash Guide

> Use this as a quick review map before interviews.
> Try to explain each topic in **60–90 seconds**.

---

# 📚 Core Goal

* Handle simple derivatives
* Understand basic calculus rules
* Explain descriptive statistics
* Understand basic probability concepts

### Most Common Interview Questions

* Derivative of (x^2 \sin(2x))
* Product Rule
* Chain Rule
* Mean
* Variance
* Standard Deviation
* Basic Probability
* Correlation vs Causation

---

# 📈 Derivative Basics

A derivative measures how fast a function changes with respect to a variable.

---

# Common Derivative Rules

## Power Rule

\frac{d}{dx}(x^n)=n x^{n-1}

---

## Trigonometric Derivatives

\frac{d}{dx}(\sin(x))=\cos(x)

\frac{d}{dx}(\cos(x))=-\sin(x)

---

## Example

Derivative of:

Result:

f'(x)=2x

## ✅ Interview Answer

> A derivative tells us how a function changes with respect to x.



---

# ✖️ Product Rule

Used when two functions are multiplied together.

---

# Formula

f(x)=u(x)v(x) \Rightarrow f'(x)=u'(x)v(x)+u(x)v'(x)

---

# Example

Differentiate:

Using product rule:

* First function → (x^2)
* Second function → (\sin(2x))

Result:

f'(x)=2x\sin(2x)+x^2\cdot2\cos(2x)

## ✅ Interview Answer

> I use the product rule when two functions are multiplied.



---

# 🔗 Chain Rule

Used when one function is inside another function.

---

# Formula

\frac{d}{dx}f(g(x))=f'(g(x))\cdot g'(x)

---

# Example

Differentiate:

Steps:

1. Derivative of outer function:

   * (\sin → \cos)
2. Multiply by derivative of inner function:

   * derivative of (2x) is (2)

Result:

f'(x)=2\cos(2x)

## ✅ Interview Answer

> I use the chain rule when one function is inside another function.



---

# 📊 Mean

The mean is the average value of a dataset.

---

# Formula

\text{Mean}=\frac{x_1+x_2+\cdots+x_n}{n}

---

# Example

Dataset:

```text id="mean-example"
2, 4, 6
```

Mean:

[
\frac{2+4+6}{3}=4
]

---

## Important Point

The mean is sensitive to outliers.

## ✅ Interview Answer

> Mean summarizes the central value of a dataset.


---

# 📉 Variance

Variance measures how spread out values are around the mean.

---

# Formula

\text{Variance}=\frac{\sum (x_i-\mu)^2}{n}

---

## Key Idea

* Small variance → data close to mean
* Large variance → data spread out

## ✅ Interview Answer

> Variance tells us how much the data varies around the mean.



---

# 📏 Standard Deviation

Standard deviation is the square root of variance.

---

# Formula

\sigma=\sqrt{\text{Variance}}

---

## Why It Matters

It uses the same unit as the original data, making interpretation easier.

---

## Example

If:

* Mean height = 170 cm
* Standard deviation = 5 cm

Most values are near:

* 165–175 cm

## ✅ Interview Answer

> Standard deviation shows the typical distance from the mean.


---

# 🎲 Probability

Probability measures how likely an event is.

Range:

[
0 \le P(E) \le 1
]

* 0 → impossible
* 1 → certain

---

# Independent Events

If events A and B are independent:

---

# Mutually Exclusive Events

If A and B cannot happen together:

P(A \cup B)=P(A)+P(B)

---

# Example

Coin toss:

* Probability of heads = 0.5

Dice:

* Probability of rolling 6 = (1/6)

## ✅ Interview Answer

> Probability is a numerical measure of uncertainty.



---

# 🔄 Correlation vs Causation

## Correlation

Two variables change together statistically.

Example:

* Ice cream sales ↑
* Swimming activity ↑

---

## Causation

One variable directly causes another.

---

## Important Point

Correlation alone does NOT prove causation.

There may be hidden factors involved.

Example:

* Hot weather increases both ice cream sales and swimming

## ✅ Interview Answer

> Correlation is association, not necessarily cause and effect.


---

# ⚡ Quick Formula Revision

| Concept            | Formula                   |
| ------------------ | ------------------------- |
| Power Rule         | (n x^{n-1})               |
| Product Rule       | (u'v + uv')               |
| Chain Rule         | (f'(g(x))g'(x))           |
| Mean               | (\frac{\sum x}{n})        |
| Variance           | Average squared deviation |
| Standard Deviation | (\sqrt{\text{Variance}})  |


# 🎯 Likely Interview Questions

Practice these answers aloud. Do not memorize word-for-word; memorize the structure and key points.

## 1. What is the product rule?

If a function is the product of two functions, f(x) = u(x)v(x), then f'(x) = u'(x)v(x) + u(x)v'(x).

## 2. derivative of x^2 sin(2x)

## 3. What is variance?

Variance measures how spread out the data is around the mean. 

A small variance means values are close to the mean, while a large variance means values are more dispersed.

## Other questions:

- Plot a graph: y=0.5*sin(2x)+1
- Find Euclidean norm
- Find the dot product
- Distance of two points
- Basic probability: independent and mutually exclusive events.
---

# 🎯 Final Interview Tips

* Explain derivative steps slowly and clearly
* Mention “spread of data” for variance
* Mention “same unit as original data” for standard deviation
* Always distinguish correlation from causation
* Use simple examples like dice, coins, or student grades

---

# ⚡ Quick Revision Checklist

* [ ] Basic Derivatives
* [ ] Product Rule
* [ ] Chain Rule
* [ ] Mean
* [ ] Variance
* [ ] Standard Deviation
* [ ] Probability
* [ ] Correlation vs Causation

---

Good luck with your interview 🚀
