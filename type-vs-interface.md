## Type vs Interface in TypeScript

## In TypeScript, we can use both `Type alias` and `Interface` to define custom types and object shape, `Type alias` is more connected to literals, unions, tuples, primitives, `Interface` is generally connected to objects and classes.

## 4 Differences between Type alias and Interface

### 1. Declaration merging

Interface name can be redeclared and it merge to a single interface, type alias can't redeclare.

### 2. Union types

I can create union using type alias, and can't create union using interface.

### 3. Extending

Interface extend using "extends" keyword, and type alias extend using "&" (intersection) operator.

### 4. Primitives and tuples

Type alias used for primitive and tuple, interface used for objects and classes.

```ts
type isActive = boolean;

type Role = "user" | "admin";

type Id = number | string;

interface User {
	id: number;
	name: string;
}
```

## When to Use Which

In short, I use `interface` when defining the shape of objects and working with classes, especially if the code needs to be extended. On the other hand, I use `type` when working with union types, tuples, or primitive aliases where `interface` cannot be used.

## Conclusion

In conclusion, both type aliases and interfaces can describe the shape of an object, but they serve different purposes. Interface is ideal for objects and classes, while type alias is the best choice for unions and complex types.
