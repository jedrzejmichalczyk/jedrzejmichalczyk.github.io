---
layout: post
title: "Hello World"
date: 2026-02-12
categories: math
---

A first post to test LaTeX rendering and code highlighting.

## Inline math

Euler's identity $e^{i\pi} + 1 = 0$ connects five fundamental constants.

## Display math

The Gaussian integral:

$$\int_{-\infty}^{\infty} e^{-x^2} \, dx = \sqrt{\pi}$$

A matrix equation:

$$\begin{bmatrix} a & b \\ c & d \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} ax + by \\ cx + dy \end{bmatrix}$$

## Code

A simple Newton-Raphson iteration in Python:

```python
def newton(f, df, x0, tol=1e-12, maxiter=100):
    x = x0
    for _ in range(maxiter):
        dx = f(x) / df(x)
        x -= dx
        if abs(dx) < tol:
            return x
    raise RuntimeError("did not converge")
```

And in C:

```c
#include <math.h>

double newton(double (*f)(double), double (*df)(double),
              double x0, double tol, int maxiter) {
    double x = x0;
    for (int i = 0; i < maxiter; i++) {
        double dx = f(x) / df(x);
        x -= dx;
        if (fabs(dx) < tol) return x;
    }
    return NAN;
}
```
