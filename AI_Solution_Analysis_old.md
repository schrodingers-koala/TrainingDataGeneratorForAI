# Training Data Generator for AI

Notebooks for prototyping of training data generation.

## Contents

- [MATH: Linear Algebra Data Generator](LinAlgDataGenerator.ipynb)

## Example

### Linear Algebra Data Generator (2 Equations, 2 Variables)

```text:2 equations, 2 variables
----- Problem 1 -----
In a market, 2 kinds of fruits, blueberries and kiwifruits are for sale.
The price of blueberry is 40 cents. The price of kiwifruit is 79 cents.
A shopper buys fruits at this market.
The number of fruits is 14.
The sum of price is 911 cents.
How many blueberries and kiwifruits does the shopper buy?
Show one solution.
----- Solution 1 -----
Eqs are followings.
Eq0: 1*blueberry + 1*kiwifruit - 14 = 0
Eq1: 40*blueberry + 79*kiwifruit - 911 = 0
Making new Eqs.
New Eq0 is 1*Eq0
New Eq1 is -40*Eq0 + 1*Eq1
New Eqs are followings.
Eq0: 1*blueberry + 1*kiwifruit - 14 = 0
Eq1: 39*kiwifruit - 351 = 0
Solution is blueberry = 5, kiwifruit = 9
```

### Linear Algebra Data Generator (3 Equations, 4 Variables)

```text:3 equations, 4 variables
----- Problem 2 -----
In a market, 4 kinds of fruits, apples, grapes, melons and strawberries are for sale.
The price of apple is 67 cents. The price of grape is 51 cents. The price of melon is 91 cents. The price of strawberry is 36 cents.
The weight of apple is 71 g. The weight of grape is 6 g. The weight of melon is 76 g. The weight of strawberry is 66 g.
A shopper buys fruits at this market.
The number of fruits is 27.
The sum of price is 1634 cents.
The sum of weight is 1647 g.
How many apples, grapes, melons and strawberries does the shopper buy?
Show one solution.
----- Solution 2 -----
Eqs are followings.
Eq0: 1*apple + 1*grape + 1*melon + 1*strawberry - 27 = 0
Eq1: 67*apple + 51*grape + 91*melon + 36*strawberry - 1634 = 0
Eq2: 71*apple + 6*grape + 76*melon + 66*strawberry - 1647 = 0
Making new Eqs.
New Eq0 is 1*Eq0
New Eq1 is -67*Eq0 + 1*Eq1
New Eq2 is 3219/16*Eq0 - 65/16*Eq1 + 1*Eq2
New Eqs are followings.
Eq0: 1*apple + 1*grape + 1*melon + 1*strawberry - 27 = 0
Eq1: -16*grape + 24*melon - 31*strawberry + 175 = 0
Eq2: -185/2*melon + 1935/16*strawberry - 7055/16 = 0
Eq2 leads the following relation.
melon = 387*N - 380
N is integer.
Calculating Eqs for dependent variables.
apple = 697 - 690*N
grape = 7*N - 3
melon = 387*N - 380
strawberry = 296*N - 287
Searching a solution for apple > 0, grape > 0, melon > 0 and strawberry > 0.
Step 1: N = 0, then apple = 697, grape = -3, melon = -380 and strawberry = -287.
There are minus value variables, grape = -3, melon = -380 and strawberry = -287.
Step 2: N = 1, then apple = 7, grape = 4, melon = 7 and strawberry = 9.
There is no minus value variable.
One solution is apple = 7, grape = 4, melon = 7 and strawberry = 9.
```

## AI Solution Analysis

### Bing AI Chat (2 Equations, 2 Variables)

<a name="2_2"></a>

Bing AI Chat fails solving all of these 5 problems.

|                                 | [Problem 1](./BingAIChat/2023_0916/Conversation_2Eqs_2Vars_P01.txt) | [Problem 2](./BingAIChat/2023_0916/Conversation_2Eqs_2Vars_P02.txt) | [Problem 3](./BingAIChat/2023_0916/Conversation_2Eqs_2Vars_P03.txt) | [Problem 4](./BingAIChat/2023_0916/Conversation_2Eqs_2Vars_P04.txt) | [Problem 5](./BingAIChat/2023_0916/Conversation_2Eqs_2Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |  Correct  |  Correct  |  Correct  |  Correct  |  Correct  |  Correct 5/5  |
|      Calculation generated      |    Yes    |    Yes    |    No     |    Yes    |    Yes    | Generated 4/5 |
|   Result of calculation check   |   Wrong   |   Wrong   |     -     |   Wrong   |   Wrong   |  Correct 0/4  |
|       Solution generated        |    No     |    Yes    |    Yes    |    Yes    |    Yes    | Generated 4/5 |
| Result of solution verification |     -     |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/4  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |

### Bing AI Chat (2 Equations, 3 Variables)

<a name="2_3"></a>

Bing AI Chat fails solving all of these 5 problems.

|                                 | [Problem 1](./BingAIChat/2023_0916/Conversation_2Eqs_3Vars_P01.txt) | [Problem 2](./BingAIChat/2023_0916/Conversation_2Eqs_3Vars_P02.txt) | [Problem 3](./BingAIChat/2023_0916/Conversation_2Eqs_3Vars_P03.txt) | [Problem 4](./BingAIChat/2023_0916/Conversation_2Eqs_3Vars_P04.txt) | [Problem 5](./BingAIChat/2023_0916/Conversation_2Eqs_3Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |  Correct  |  Correct  |  Correct  |  Correct  |  Correct  |  Correct 5/5  |
|      Calculation generated      |    Yes    |    Yes    |    No     |    No     |    Yes    | Generated 3/5 |
|   Result of calculation check   |   Wrong   |   Wrong   |     -     |     -     |   Wrong   |  Correct 0/3  |
|       Solution generated        |    Yes    |    No     |    Yes    |    Yes    |    Yes    | Generated 4/5 |
| Result of solution verification |   Wrong   |     -     |   Wrong   |   Wrong   |   Wrong   |  Correct 0/4  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |

### Bing AI Chat (2 Equations, 4 Variables)

<a name="2_4"></a>

Bing AI Chat fails solving all of these 5 problems.

|                                 | [Problem 1](./BingAIChat/2023_0916/Conversation_2Eqs_4Vars_P01.txt) | [Problem 2](./BingAIChat/2023_0916/Conversation_2Eqs_4Vars_P02.txt) | [Problem 3](./BingAIChat/2023_0916/Conversation_2Eqs_4Vars_P03.txt) | [Problem 4](./BingAIChat/2023_0916/Conversation_2Eqs_4Vars_P04.txt) | [Problem 5](./BingAIChat/2023_0916/Conversation_2Eqs_4Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |  Correct  |  Correct  |  Correct  |  Correct  |  Correct  |  Correct 5/5  |
|      Calculation generated      |    No     |    No     |    Yes    |    Yes    |    Yes    | Generated 3/5 |
|   Result of calculation check   |     -     |     -     |   Wrong   |   Wrong   |   Wrong   |  Correct 0/3  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    No     |    Yes    | Generated 4/5 |
| Result of solution verification |   Wrong   |   Wrong   |   Wrong   |     -     |   Wrong   |  Correct 0/4  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |

### Bing AI Chat (3 Equations, 3 Variables)

<a name="3_3"></a>

Bing AI Chat fails solving all of these 5 problems.

|                                 | [Problem 1](./BingAIChat/2023_0916/Conversation_3Eqs_3Vars_P01.txt) | [Problem 2](./BingAIChat/2023_0916/Conversation_3Eqs_3Vars_P02.txt) | [Problem 3](./BingAIChat/2023_0916/Conversation_3Eqs_3Vars_P03.txt) | [Problem 4](./BingAIChat/2023_0916/Conversation_3Eqs_3Vars_P04.txt) | [Problem 5](./BingAIChat/2023_0916/Conversation_3Eqs_3Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |  Correct  |  Correct  |  Correct  |  Correct  |  Correct  |  Correct 5/5  |
|      Calculation generated      |    No     |    Yes    |    No     |    No     |    Yes    | Generated 2/5 |
|   Result of calculation check   |     -     |   Wrong   |     -     |     -     |   Wrong   |  Correct 0/2  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
| Result of solution verification |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |

### Bing AI Chat (3 Equations, 4 Variables)

<a name="3_4"></a>

Bing AI Chat fails solving all of these 5 problems.

|                                 | [Problem 1](./BingAIChat/2023_0916/Conversation_3Eqs_4Vars_P01.txt) | [Problem 2](./BingAIChat/2023_0916/Conversation_3Eqs_4Vars_P02.txt) | [Problem 3](./BingAIChat/2023_0916/Conversation_3Eqs_4Vars_P03.txt) | [Problem 4](./BingAIChat/2023_0916/Conversation_3Eqs_4Vars_P04.txt) | [Problem 5](./BingAIChat/2023_0916/Conversation_3Eqs_4Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |  Correct  |  Correct  |  Correct  |  Correct  |  Correct  |  Correct 5/5  |
|      Calculation generated      |    No     |    Yes    |    Yes    |    No     |    No     | Generated 2/5 |
|   Result of calculation check   |     -     |   Wrong   |   Wrong   |     -     |     -     |  Correct 0/2  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
| Result of solution verification |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |
