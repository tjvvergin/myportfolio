+++
title = 'Optimized C++'
date = 2025-04-01
draft = false
Description = "Here are just some of the optimizations I learned about in Ed Keenan's Optimized C++ class."
tags = ["projects"]
categories = ["projects"]
+++

# Optimized C++ with Edward Keenan

In Ed's class I learned a lot about how to make high performance C++ programs. In this class we learned optimizations like using SIMD or Single Instruction Multiple Data functions, optimized padding and alignment with data structures, pointer manipulation, return value optimizations, float optimization, and many more smaller optimizations. A lot of these optimizations are easy to implement but require a fairly in depth knowledge of the C++ compiler and CPU architecture to understand. Below I will go through a few examples of what we learned.

## RVO - Return Value Optimization

Return Value Optimization (RVO) is a compiler optimization that eliminates unnecessary copying when returning objects by value. Instead of creating a temporary object which then gets copied into the output, RVO optimizations make the program run faster by skipping the unnecessary CPU instructions that copy the temporary object because it just copies it directly from the original value. This optimization can make a function that runs many thousands of times per second run slightly faster which adds up a lot over time and can make a significant difference. Realistically this optimization is often done by the compiler itself when run with the correct performance optimization options but doing it manually can ensure that the compiler never runs into a situation where it cannot safely optimize the code which makes the code more robust.

```cpp
struct Data {
    int value;
    Data(int v) : value(v) { }
    Data(const Data& other) : value(other.value) { }
};

Data createDataOptimized() {
    // Directly returning a temporary enables RVO.
    return Data(42);
}

Data createDataUnoptimized() {
    // Returning a named object may inhibit RVO.
    Data temp(42);
    return temp;
}
```

## Optimized Data Structure Alignment and Padding

Proper data alignment ensures that variables are stored in memory at addresses optimized for the CPU, decreasing the amount of time the CPU spends loading the data instead of processing it. Misalignment can cause the CPU to waste clock cycles trying to load the next bits of data to process when it already could have started working if it had access to the data because it was aligned properly. Modern alignment specifiers like `alignas` can make aligning data easier but improper understanding of the underlying size of the data can cause even more wasted memory and CPU clock cycles. This is why proper understanding of the structure is essential when trying to implement the optimizations.

```cpp
struct Unoptimized {
    char  a;
    int   b;
    char c;
};

struct alignas(16) Optimized {
    int   b;
    char  a;
    char  c;
};
```

## SIMD - Single Instruction Multiple Data

SIMD allows a single instruction to process multiple data elements simultaneously. This parallel approach can improve performance greatly as correctly implemented code can achieve a theoretically very large performance boost by utilizing the correct instructions. The reason it is so large is because instead of doing one math operation per instruction a properly designed SIMD intrinsics program can perform multiple (2 or more) math operations in that very same amount of time. This can be extremely beneficial where high computational performance is important. Below I have included an example of some of the things we learned in class using SSE4.1 128bit floating point numbers.

```cpp
int main() {
    alignas(16) float a[4] = {1.0f, 2.0f, 3.0f, 4.0f};
    alignas(16) float b[4] = {8.0f, 7.0f, 6.0f, 5.0f};
    alignas(16) float c[4];

    __m128 va = _mm_load_ps(a);
    __m128 vb = _mm_load_ps(b);
    __m128 vc = _mm_add_ps(va, vb);
    _mm_store_ps(c, vc);

    for (int i = 0; i < 4; i++)
        std::cout << c[i] << " ";
    return 0;
}
```