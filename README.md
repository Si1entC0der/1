# Advanced Problem Solving with TypeScript & OOP

## Assignment Overview

This repository contains solutions for the B7A1 TypeScript assignment covering fundamental TypeScript concepts including data typing, interfaces, generics, class inheritance, and type narrowing.

## File Structure

```
├── solutions.ts   — All 7 coding solutions
├── blog-1.md      — Blog: why unknown is safer than any, and type narrowing
├── blog-2.md      — Blog: the four pillars of OOP in TypeScript
└── README.md      — This file
```

## Problems Solved

| Problem | Function | Description |
|---|---|---|
| 1 | `filterEvenNumbers` | Filters even numbers from an array |
| 2 | `reverseString` | Reverses a string |
| 3 | `checkType` | Type guard using union type `StringOrNumber` |
| 4 | `getProperty` | Generic function with `keyof` constraint |
| 5 | `toggleReadStatus` | Adds `isRead` property to a `Book` interface object |
| 6 | `Student` class | Inherits from `Person`, adds `grade` and `getDetails()` |
| 7 | `getIntersection` | Returns elements common to two arrays |

## Blog Posts

- **Blog 1:** Why `any` is a type safety hole and how `unknown` with type narrowing is the safer approach
- **Blog 2:** A guide on using `Pick` and `Omit` utility types to create specialized slices of interfaces, ensuring the codebase remains DRY (Don't Repeat Yourself) and maintainable.

## How to Run

```bash
# Install TypeScript globally if not already installed
npm install -g typescript

# Compile the solutions file
tsc solutions.ts

# Run the compiled output
node solutions.js
```
