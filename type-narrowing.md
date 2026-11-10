# Type Narrowing in TypeScript: A Practical Guide

## Introduction

TypeScript's type system frequently handles union types where a variable can hold values of different types at runtime. Type Narrowing is the mechanism of refining a broader type into a more specific, concrete type through conditional code paths and runtime guards.

## Common Type Narrowing Techniques

### 1. The `typeof` Guard

For primitive types such as `string`, `number`, and `boolean`, the built-in JavaScript `typeof` operator provides an effective runtime guard. TypeScript automatically narrows down the type inside conditional branches.

```typescript
function formatInput(value: string | number): string {
  if (typeof value === "string") {
    return value.trim().toLowerCase();
  }
  return value.toFixed(2);
}
```
