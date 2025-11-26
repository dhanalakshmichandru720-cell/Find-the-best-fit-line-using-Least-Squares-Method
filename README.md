# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
import numpy as np
import matplotlib.pyplot as plt

def estimate_coefficients(x, y):
    """
    Estimate slope (m) and intercept (c) for y = m*x + c using least squares.
    """
    if len(x) != len(y) or len(x) == 0:
        raise ValueError("x and y must have the same non-zero length.")

    n = len(x)
    mean_x = np.mean(x)
    mean_y = np.mean(y)

    # Calculate slope (m) and intercept (c)
    numerator = np.sum((x - mean_x) * (y - mean_y))
    denominator = np.sum((x - mean_x) ** 2)

    if denominator == 0:
        raise ValueError("All x values are identical; slope is undefined.")

    m = numerator / denominator
    c = mean_y - m * mean_x

    return m, c

def predict(x, m, c):
    """Predict y values for given x using y = m*x + c."""
    return m * x + c

def main():
    try:
        # Example dataset
        x = np.array([1, 2, 3, 4, 5], dtype=float)
        y = np.array([2, 4, 5, 4, 5], dtype=float)

        # Estimate coefficients
        m, c = estimate_coefficients(x, y)
        print(f"Estimated coefficients:\nSlope (m) = {m:.4f}\nIntercept (c) = {c:.4f}")

        # Predict values
        y_pred = predict(x, m, c)

        # Plotting
        plt.scatter(x, y, color="blue", label="Data points")
        plt.plot(x, y_pred, color="red", label=f"Fitted line: y = {m:.2f}x + {c:.2f}")
        plt.xlabel("X")
        plt.ylabel("Y")
        plt.title("Univariate Linear Regression (Least Squares)")
        plt.legend()
        plt.grid(True)
        plt.show()

    except Exception as e:
        print(f"Error: {e}")

if __name__ == "__main__":
    main()

Developed by: dhanalakshmi.c
RegisterNumber:  25018616
*/
```

## Output:
<img width="1354" height="636" alt="Screenshot (145)" src="https://github.com/user-attachments/assets/a882e833-646b-49d1-9833-017c00a26de3" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
