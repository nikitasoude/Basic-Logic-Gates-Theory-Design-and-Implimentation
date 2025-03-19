Basic Logic Gates - Theory, Design & Implementation**

### Concept Overview
Logic gates are the building blocks of digital circuits. They perform basic logical functions and are implemented using electronic switches like transistors.

### Types of Basic Logic Gates
1. **AND Gate**
   - **Output** = `A • B`
   - **Truth Table:**

| A | B | Y (A AND B) |
|:-:|:-:|:------------:|
| 0 | 0 |      0       |
| 0 | 1 |      0       |
| 1 | 0 |      0       |
| 1 | 1 |      1       |

2. **OR Gate**
   - **Output** = `A + B`
   - **Truth Table:**

| A | B | Y (A OR B) |
|:-:|:-:|:-----------:|
| 0 | 0 |      0      |
| 0 | 1 |      1      |
| 1 | 0 |      1      |
| 1 | 1 |      1      |

3. **NOT Gate (Inverter)**
   - **Output** = `~A`
   - **Truth Table:**

| A | Y (~A) |
|:-:|:-------:|
| 0 |    1    |
| 1 |    0    |

4. **NAND Gate**
   - **Output** = `~(A • B)`
   - **Truth Table:**

| A | B | Y (~(A AND B)) |
|:-:|:-:|:---------------:|
| 0 | 0 |        1        |
| 0 | 1 |        1        |
| 1 | 0 |        1        |
| 1 | 1 |        0        |

5. **NOR Gate**
   - **Output** = `~(A + B)`
   - **Truth Table:**

| A | B | Y (~(A OR B)) |
|:-:|:-:|:--------------:|
| 0 | 0 |        1       |
| 0 | 1 |        0       |
| 1 | 0 |        0       |
| 1 | 1 |        0       |

6. **XOR Gate**
   - **Output** = `A ⊕ B`
   - **Truth Table:**

| A | B | Y (A XOR B) |
|:-:|:-:|:-------------:|
| 0 | 0 |       0       |
| 0 | 1 |       1       |
| 1 | 0 |       1       |
| 1 | 1 |       0       |

