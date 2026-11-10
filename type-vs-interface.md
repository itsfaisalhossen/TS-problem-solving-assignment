# Understanding the Core Differences Between Type Aliases and Interfaces in TypeScript

## Introduction

In TypeScript, defining contracts for data structures is fundamental for writing type-safe code. Developers frequently choose between `type` aliases and `interface` declarations. While they share many similarities, understanding their distinct behaviors and ideal use cases is essential for writing scalable code.

## Core Differences and Capabilities

### 1. Declaration Merging

Interfaces support declaration merging. If you define the same interface multiple times, TypeScript automatically merges their properties together. In contrast, declaring the same type alias twice results in a compile-time error.

```typescript
interface UserProfile {
  id: number;
}
interface UserProfile {
  name: string;
}
// Merged result: { id: number; name: string }
```
