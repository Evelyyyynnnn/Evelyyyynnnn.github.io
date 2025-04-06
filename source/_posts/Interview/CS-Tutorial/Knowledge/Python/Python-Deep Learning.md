---
tags: Interview
date: 2025-04-11 10:15:38
---



### Gradient_descent Mechanism
```python
import numpy as np
import numpy.linalg as linalg

def loss_function(A, b, x):
    """Evaluates the loss (1 / 2) * |Ax - b|^2."""
    residual = np.dot(A, x) - b
    return 0.5 * np.dot(residual, residual)

def gradient(A, b, x):
    """Evaluates the gradient of (1 / 2) * |Ax - b|^2."""
    residual = np.dot(A, x) - b
    return np.dot(A.T, residual)

def gradient_descent(A, b, x_0, num_iterations):
    """Runs gradient descent to minimize the loss (1 / 2) * |Ax - b|^2."""
    x = x_0
    for _ in range(num_iterations):
        grad = gradient(A, b, x)
        grad_norm_sq = np.dot(grad, grad)
        if grad_norm_sq == 0:
            break
        step_size = loss_function(A, b, x) / grad_norm_sq
        x = x - step_size * grad
    gradnorm = linalg.norm(gradient(A, b, x))
    return x, gradnorm

# 示例测试
if __name__ == "__main__":
    A = np.array([[1, -1], [0, 1]])
    b = np.array([0, 0])
    x_0 = np.array([1, 1])
    num_iterations = 100
    solution, gradnorm = gradient_descent(A, b, x_0, num_iterations)
    print("Solution:", solution)
    print("Gradient norm:", gradnorm)

```