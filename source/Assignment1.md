
---
title: "Assignment 1: Matrix Multiplication"
date: 2025-06-06
---

## Matrix Multiplication Project Report

**Student Name**: Ivonne Andrea Anave Zenteno  
**Student ID**: LS2408221  
**Submission Date**: 26/03/2025  

---

## System Configuration

| **Parameter**               | **Value**                                                                 |
|-----------------------------|---------------------------------------------------------------------------|
| **CPU Model**               | Intel(R) Core(TM) i7-14650HX                                              |
| **Memory Size**             | total 15Gi, used 500Mi                                                    |
| **Operating System Version**| Linux WSL2 - Ubuntu 22.04                                                 |
| **Compiler Version**        | gcc (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0                                 |
| **Python Version**          | Python 3.12.9                                                             |

---

## Implementation Details

### C Language Implementation

```c
#include <stdio.h>
#include <stdlib.h>

#define SIZE 2

void printMatrix(int mat[SIZE][SIZE]) {
    for (int i = 0; i < SIZE; i++) {
        for (int j = 0; j < SIZE; j++) {
            printf("%d ", mat[i][j]);
        }
        printf("\n");
    }
}

void multiplyMatrices(int mat1[SIZE][SIZE], int mat2[SIZE][SIZE], int result[SIZE][SIZE]) {
    for (int i = 0; i < SIZE; i++) {
        for (int j = 0; j < SIZE; j++) {
            result[i][j] = 0;
            for (int k = 0; k < SIZE; k++) {
                result[i][j] += mat1[i][k] * mat2[k][j];
            }
        }
    }
}

int main() {
    int mat1[SIZE][SIZE] = {{1, 2}, {3, 4}};
    int mat2[SIZE][SIZE] = {{5, 6}, {7, 8}};
    int result[SIZE][SIZE];

    multiplyMatrices(mat1, mat2, result);

    printf("Matrix 1:\n");
    printMatrix(mat1);
    printf("Matrix 2:\n");
    printMatrix(mat2);
    printf("Result:\n");
    printMatrix(result);

    return 0;
}

