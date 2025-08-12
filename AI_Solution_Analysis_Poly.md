# AI Solution Analysis of Polynomial Problem

## Example

For details about generating examples, please refer to [Polynomial Data Generator](PolynomialDataGenerator.ipynb).

### Polynomial Data Generator (Easier mode)

```text:Easier mode
----- Problem 1 -----
Simplify (304*a^9*b^5*c + 144*a^8*b^6*c + 456*a^7*b^8*c^8 + 216*a^6*b^9*c^8)/(-36*a*c - 76*b^2 - 36*b*c - 76*c^2 + 250), where a + b + c - 1 = 0, a^2 + b^2 + c^2 - 4 = 0.
Please solve the problem and express it with a polynomial.
----- Solution 1 -----
4*a**7*b**5*c + 6*a**5*b**8*c**8
```

### Polynomial Data Generator (Easy mode)

```text:Easy mode
----- Problem 2 -----
Simplify (2*a^12*b^12*c^9 + 3*a^9*b^8*c^11 + 2*a^8*b^12*c^8 + 56*a^8*b^5*c^7 + 70*a^7*b^6*c^7 + 3*a^5*b^8*c^10 + 56*a^4*b^5*c^6 + 70*a^3*b^6*c^6)/(2*a^6*b^7*c^2 + 3*a^3*b^3*c^4 - 70*a*c - 56*b^2 - 70*b*c - 56*c^2 + 119), where a + b + c - 1 = 0, a^2 + b^2 + c^2 - 4 = 0.
Please solve the problem and express it with a polynomial.
----- Solution 2 -----
a**6*b**5*c**7 + a**2*b**5*c**6
```

## AI Solution Analysis

## Test Procedure

- Step 1: A tester sends a problem to AI.

- Step 2: AI tries to solve the problem. (Up to 3 times)

  - Step 2.1: AI chooses a way to provides a solution, a polynomial or a python code.

    (Polynomial Case)
    - Step 2.2P: AI sends a polynomial to the tester.
    - Step 2.3P: The tester verify the polynomial.

      If the polynomial is correct, this test procedure stops.

      If the polynomial is wrong, go to Step 2.

    (Python Code Case)
    - Step 2.2C: AI sends a python code to the tester. (Up to 10 times)
    - Step 2.3C: The tester run the python code.

      If the python code returns a polynomial successfully, go to Step 2.4C.

      If the python code fails, the tester send the error to AI and go to Step 2.2C.

    - Step 2.4C: The tester verify the polynomial.

      If the polynomial is correct, this test procedure stops.

      If the polynomial is wrong, go to Step 2.

### Bing AI Chat (Easier mode)

Bing AI Chat succeeded in solving 2 of these 5 problems.

|                                 |  | [Problem 1](./BingAIChat/Polynomial/20250811/Easier/P01/) | [Problem 2](./BingAIChat/Polynomial/20250811/Easier/P02/) | [Problem 3](./BingAIChat/Polynomial/20250811/Easier/P03/) | [Problem 4](./BingAIChat/Polynomial/20250811/Easier/P04/) | [Problem 5](./BingAIChat/Polynomial/20250811/Easier/P05/) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
| 1st try | Choice       |    Code   |    Code   |    Code   |    Code   |    Code   |             |
|         | Code fail    |    2/3    |    0/1    |    2/5    |    0/1    |    1/2    |             |
|         | Timeout      |    0/3    |    0/1    |    2/5    |    0/1    |    0/2    |             |
|         | Code success |    1/3    |    1/1    |    1/5    |    1/1    |    1/2    |             |
|         | Verify       | Not Poly. | Not Poly. | Not Poly. |Wrong Poly.| Not Poly. |             |
|         | Result       |    Fail   |    Fail   |    Fail   |    Fail   |    Fail   |             |
| 2nd try | Choice       |    Code   |    Code   |    Code   |    Code   |    Poly   |             |
|         | Code fails   |    0/1    |    0/1    |    0/1    |    0/1    |     -     |             |
|         | Timeout      |    0/1    |    0/1    |    0/1    |    0/1    |     -     |             |
|         | Code success |    0/1    |    0/1    |    0/1    |    1/1    |     -     |             |
|         | Verify       | Not Poly. | Not Poly. | Not Poly. |Wrong Poly.|  Correct  |             |
|         | Result       |    Fail   |    Fail   |    Fail   |    Fail   |  Success  |             |
| 3rd try | Choice       |    Code   |    Poly   |    Code   |    Code   |           |             |
|         | Code fails   |    0/1    |     -     |    0/1    |    0/1    |           |             |
|         | Timeout      |    0/1    |     -     |    0/1    |    0/1    |           |             |
|         | Code success |    1/1    |     -     |    1/1    |    1/1    |           |             |
|         | Verify       |Wrong Poly.|  Correct  |Wrong Poly.|Wrong Poly.|           |             |
|         | Result       |    Fail   |  Success  |    Fail   |    Fail   |           |             |
|  Total  | Result       |    Fail   |  Success  |    Fail   |    Fail   |  Success  | Success 2/5 |

### Bing AI Chat (Easy mode)

Bing AI Chat failed in solving all of these 5 problems.

|                                 |  | [Problem 1](./BingAIChat/Polynomial/20250811/Easy/P01/) | [Problem 2](./BingAIChat/Polynomial/20250811/Easy/P02/) | [Problem 3](./BingAIChat/Polynomial/20250811/Easy/P03/) | [Problem 4](./BingAIChat/Polynomial/20250811/Easy/P04/) | [Problem 5](./BingAIChat/Polynomial/20250811/Easy/P05/) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
| 1st try | Choice       |    Code   |    Code   |    Code   |    Code   |    Code   |             |
|         | Code fail    |    4/5    |    0/1    |    0/1    |    0/2    |    1/4    |             |
|         | Timeout      |    0/5    |    0/1    |    0/1    |    1/2    |    2/4    |             |
|         | Code success |    1/5    |    1/1    |    1/1    |    1/2    |    1/4    |             |
|         | Verify       | Not Poly. |Wrong Poly.| Not Poly. | Not Poly. | Not Poly. |             |
|         | Result       |    Fail   |    Fail   |    Fail   |    Fail   |    Fail   |             |
| 2nd try | Choice       |    Code   |    Code   |    Code   |    Code   |    Code   |             |
|         | Code fails   |    3/9    |    3/9    |    0/1    |    3/6    |    1/2    |             |
|         | Timeout      |    5/9    |    5/9    |    0/1    |    2/6    |    0/2    |             |
|         | Code success |    1/9    |    1/9    |    1/1    |    1/6    |    1/2    |             |
|         | Verify       | Not Poly. | Not Poly. | Not Poly. |Wrong Poly.| Not Poly. |             |
|         | Result       |    Fail   |    Fail   |    Fail   |    Fail   |    Fail   |             |
| 3rd try | Choice       |    Code   |    Code   |    Code   |    Code   |    Code   |             |
|         | Code fails   |    0/1    |    8/10   |    0/1    |    0/1    |    4/8    |             |
|         | Timeout      |    0/1    |    1/10   |    0/1    |    0/1    |    3/8    |             |
|         | Code success |    1/1    |    1/10   |    1/1    |    1/1    |    1/8    |             |
|         | Verify       |Wrong Poly.|Wrong Poly.|Wrong Poly.|Wrong Poly.|Wrong Poly.|             |
|         | Result       |    Fail   |    Fail   |    Fail   |    Fail   |    Fail   |             |
|  Total  | Result       |    Fail   |    Fail   |    Fail   |    Fail   |    Fail   | Success 0/5 |
