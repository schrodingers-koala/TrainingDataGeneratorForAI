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

Bing AI Chat succeeded in solving all of these 5 problems.

Previous result was 0 success out of 5 problems. (For details, see  [AI Solution Analysis (old)](AI_Solution_Analysis_old.md#2_2))


|                                 | [Problem 1](./BingAIChat/2024_0714/Conversation_2Eqs_2Vars_P01.txt) | [Problem 2](./BingAIChat/2024_0714/Conversation_2Eqs_2Vars_P02.txt) | [Problem 3](./BingAIChat/2024_0714/Conversation_2Eqs_2Vars_P03.txt) | [Problem 4](./BingAIChat/2024_0714/Conversation_2Eqs_2Vars_P04.txt) | [Problem 5](./BingAIChat/2024_0714/Conversation_2Eqs_2Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |  Correct  |  Correct  |  Correct  |  Correct  |  Correct  |  Correct 5/5  |
|      Calculation generated      |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|   Result of calculation check   |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    |  Correct 5/5  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
| Result of solution verification |  Correct  |  Correct  |  Correct  |  Correct  |  Correct  |  Correct 5/5  |
|    Result of solving problem    |  Success  |  Success  |  Success  |  Success  |  SUccess  |  Success 5/5  |

### Bing AI Chat (2 Equations, 3 Variables)

Bing AI Chat succeeded in solving one of these 5 problems.

Previous result was 0 success out of 5 problems. (For details, see  [AI Solution Analysis (old)](AI_Solution_Analysis_old.md#2_3))


|                                 | [Problem 1](./BingAIChat/2024_0714/Conversation_2Eqs_3Vars_P01.txt) | [Problem 2](./BingAIChat/2024_0714/Conversation_2Eqs_3Vars_P02.txt) | [Problem 3](./BingAIChat/2024_0714/Conversation_2Eqs_3Vars_P03.txt) | [Problem 4](./BingAIChat/2024_0714/Conversation_2Eqs_3Vars_P04.txt) | [Problem 5](./BingAIChat/2024_0714/Conversation_2Eqs_3Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |  Correct  |  Correct  |  Correct  |  Correct  |  Correct  |  Correct 5/5  |
|      Calculation generated      |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|   Result of calculation check   |  Correct  |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 1/5  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
| Result of solution verification |  Correct  |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 1/5  |
|    Result of solving problem    |  Success  |   Fail    |   Fail    |   Fail    |   Fail    |  Success 1/5  |

### Bing AI Chat (2 Equations, 4 Variables)

Bing AI Chat failed in solving all of these 5 problems.

Previous result was 0 success out of 5 problems. (For details, see  [AI Solution Analysis (old)](AI_Solution_Analysis_old.md#2_4))


|                                 | [Problem 1](./BingAIChat/2024_0714/Conversation_2Eqs_4Vars_P01.txt) | [Problem 2](./BingAIChat/2024_0714/Conversation_2Eqs_4Vars_P02.txt) | [Problem 3](./BingAIChat/2024_0714/Conversation_2Eqs_4Vars_P03.txt) | [Problem 4](./BingAIChat/2024_0714/Conversation_2Eqs_4Vars_P04.txt) | [Problem 5](./BingAIChat/2024_0714/Conversation_2Eqs_4Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |  Correct  |  Correct  |  Correct  |  Correct  |  Correct  |  Correct 5/5  |
|      Calculation generated      |    Yes    |    No     |    Yes    |    Yes    |    No     | Generated 3/5 |
|   Result of calculation check   |   Wrong   |     -     |   Wrong   |   Wrong   |     -     |  Correct 0/3  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
| Result of solution verification |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |

### Bing AI Chat (3 Equations, 3 Variables)

Bing AI Chat failed in solving all of these 5 problems.

Previous result was 0 success out of 5 problems. (For details, see  [AI Solution Analysis (old)](AI_Solution_Analysis_old.md#3_3))


|                                 | [Problem 1](./BingAIChat/2024_0714/Conversation_3Eqs_3Vars_P01.txt) | [Problem 2](./BingAIChat/2024_0714/Conversation_3Eqs_3Vars_P02.txt) | [Problem 3](./BingAIChat/2024_0714/Conversation_3Eqs_3Vars_P03.txt) | [Problem 4](./BingAIChat/2024_0714/Conversation_3Eqs_3Vars_P04.txt) | [Problem 5](./BingAIChat/2024_0714/Conversation_3Eqs_3Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |  Correct  |  Correct  |  Correct  |  Correct  |  Correct  |  Correct 5/5  |
|      Calculation generated      |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|   Result of calculation check   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
| Result of solution verification |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |

### Bing AI Chat (3 Equations, 4 Variables)

Bing AI Chat failed in solving all of these 5 problems.

Previous result was 0 success out of 5 problems. (For details, see  [AI Solution Analysis (old)](AI_Solution_Analysis_old.md#3_4))


|                                 | [Problem 1](./BingAIChat/2024_0714/Conversation_3Eqs_4Vars_P01.txt) | [Problem 2](./BingAIChat/2024_0714/Conversation_3Eqs_4Vars_P02.txt) | [Problem 3](./BingAIChat/2024_0714/Conversation_3Eqs_4Vars_P03.txt) | [Problem 4](./BingAIChat/2024_0714/Conversation_3Eqs_4Vars_P04.txt) | [Problem 5](./BingAIChat/2024_0714/Conversation_3Eqs_4Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |  Correct  |  Correct  |  Correct  |  Correct  |  Correct  |  Correct 5/5  |
|      Calculation generated      |    Yes    |    No     |    No     |    Yes    |    Yes    | Generated 3/5 |
|   Result of calculation check   |   Wrong   |     -     |     -     |   Wrong   |   Wrong   |  Correct 0/3  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
| Result of solution verification |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |

### Bing AI Chat (2 Equations, 2 Variables, some sold by measure)

Bing AI Chat failed in solving all of these 5 problems.

|                                 | [Problem 1](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_2Vars_P01.txt) | [Problem 2](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_2Vars_P02.txt) | [Problem 3](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_2Vars_P03.txt) | [Problem 4](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_2Vars_P04.txt) | [Problem 5](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_2Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |  Correct  |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 1/5  |
|      Calculation generated      |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|   Result of calculation check   |  Correct  |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 1/5  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
| Result of solution verification |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |

### Bing AI Chat (2 Equations, 3 Variables, some sold by measure)

Bing AI Chat failed in solving all of these 5 problems.

|                                 | [Problem 1](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_3Vars_P01.txt) | [Problem 2](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_3Vars_P02.txt) | [Problem 3](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_3Vars_P03.txt) | [Problem 4](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_3Vars_P04.txt) | [Problem 5](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_3Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|      Calculation generated      |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|   Result of calculation check   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
| Result of solution verification |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |

### Bing AI Chat (2 Equations, 4 Variables, some sold by measure)

Bing AI Chat failed in solving all of these 5 problems.

|                                 | [Problem 1](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_4Vars_P01.txt) | [Problem 2](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_4Vars_P02.txt) | [Problem 3](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_4Vars_P03.txt) | [Problem 4](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_4Vars_P04.txt) | [Problem 5](./BingAIChat/2024_0714/Conversation_SoldByMeasure_2Eqs_4Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|      Calculation generated      |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|   Result of calculation check   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
| Result of solution verification |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |

### Bing AI Chat (3 Equations, 3 Variables, some sold by measure)

Bing AI Chat failed in solving all of these 5 problems.

|                                 | [Problem 1](./BingAIChat/2024_0714/Conversation_SoldByMeasure_3Eqs_3Vars_P01.txt) | [Problem 2](./BingAIChat/2024_0714/Conversation_SoldByMeasure_3Eqs_3Vars_P02.txt) | [Problem 3](./BingAIChat/2024_0714/Conversation_SoldByMeasure_3Eqs_3Vars_P03.txt) | [Problem 4](./BingAIChat/2024_0714/Conversation_SoldByMeasure_3Eqs_3Vars_P04.txt) | [Problem 5](./BingAIChat/2024_0714/Conversation_SoldByMeasure_3Eqs_3Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|      Calculation generated      |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|   Result of calculation check   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
| Result of solution verification |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |

### Bing AI Chat (3 Equations, 4 Variables, some sold by measure)

Bing AI Chat failed in solving all of these 5 problems.

|                                 | [Problem 1](./BingAIChat/2024_0714/Conversation_SoldByMeasure_3Eqs_4Vars_P01.txt) | [Problem 2](./BingAIChat/2024_0714/Conversation_SoldByMeasure_3Eqs_4Vars_P02.txt) | [Problem 3](./BingAIChat/2024_0714/Conversation_SoldByMeasure_3Eqs_4Vars_P03.txt) | [Problem 4](./BingAIChat/2024_0714/Conversation_SoldByMeasure_3Eqs_4Vars_P04.txt) | [Problem 5](./BingAIChat/2024_0714/Conversation_SoldByMeasure_3Eqs_4Vars_P05.txt) |    Summary    |
| :-----------------------------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-----------: |
|       Equation generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|     Representation of Eq.       |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|      Calculation generated      |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
|   Result of calculation check   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|       Solution generated        |    Yes    |    Yes    |    Yes    |    Yes    |    Yes    | Generated 5/5 |
| Result of solution verification |   Wrong   |   Wrong   |   Wrong   |   Wrong   |   Wrong   |  Correct 0/5  |
|    Result of solving problem    |   Fail    |   Fail    |   Fail    |   Fail    |   Fail    |  Success 0/5  |

## Resources
- [AI Solution Analysis (old)](AI_Solution_Analysis_old.md)
