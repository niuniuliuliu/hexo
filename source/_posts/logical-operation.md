---
title: 逻辑运算符
categories:
  - 计算机基础
date: 2024-05-11 15:20:48
tags:
---

## 1. 逻辑与(AND)

### (A & B)  

**全1为1，有0为0**

```
0b1010 & 0b1100 = 0b1000
```

## 2. 逻辑或(OR)

### (A | B)

**全0为0，有1为1**
```
0b1010 | 0b1100 = 0b1110
```

## 3. 逻辑非(NOT)

### （!A）

**0变1，1变0**

```
NOT 0b1010 = 0b0101
```

计算机语言中的逻辑非(按位取反)通常是将符号位一起取反，然后将符号位之外的其他数字取反，末位再加上1取其补码。 这样做的目的是为了统一加减法，因为计算机中的减法是加上一个负数，负数用补码来表示。

如: ~0b1010 二进制01010

先取反： 10101

除符号位外取反： 11010

末位加1: 11011

得：-11

如果单纯只是想对无符号整数取反，可以通过全1的数与当前数异或运算就可以。

如对 0b1010 进行逻辑非运算，可通过如下方法取得结果：

```
0b1111 ^ 0b1010 = 0b0101
```



## 4.异或(XOR)

### (A ^ B)

**相同为0，不同为1**
```
0b1010 ^ 0b1100 = 0b0110
```

## 5.同或(XNOR)

### (A XNOR B)

**相同为1，不同为0**

计算机语言中一般没有同或运算符，可以通过 两个数的异或结果后再异或1 即可得到同或结果
```
0b1010 ^ 0b1100 ^ 0b1111 = 0b1001
```

## 6.与非(NAND)

### (A NAND B)

**全1为0，有0为1**

先进行逻辑与运算，再进行逻辑非运算
```
0b1010 NAND 0b1100 = 0b0111

0b1111 ^ (0b1010 & 0b1100) = 0b0111
```

## 7.或非(NOR)

### (A NOR B)

**全0为1，有1为0**

先进行逻辑与运算，再进行逻辑非运算
```
0b1010 NOR 0b1100 = 0b0001

0b1111 ^ (0b1010 | 0b1100) = 0b0001
```