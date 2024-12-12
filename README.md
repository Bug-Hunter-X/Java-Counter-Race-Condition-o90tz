# Java Counter Race Condition

This repository demonstrates a common race condition in Java multithreading.  Two threads concurrently increment a counter, leading to an incorrect final count.

## The Problem

The `Counter` class is not thread-safe.  The `increment()` method is not atomic; multiple threads can interfere with each other's updates, resulting in lost increments.

## The Solution

The solution involves using appropriate synchronization mechanisms to ensure that only one thread can access and modify the `count` variable at a time. This can be done using either `synchronized` methods or blocks, or using atomic variables. 