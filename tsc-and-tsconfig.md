## How TypeScript Compiles: tsc and tsconfig.json

### Browser and node.js cannot run TypeScript code directly, they only undrustand JavaScript, that's way wee need to convert TypeScript code into JavaScirpt, and the `tsc` command complete the job when i run `tsc` TypeScript compiler complie my .ts file into .js file.

## What Happens During Compilation

When we run the tsc command, the compiler goes through a few clear steps:

- Reads and checks code: First, tsc reads our .ts files and checks for any type errors.

- Reports errors: If there is any type mismatch or mistake, it shows an error message in the terminal.

- Removes types: Next, it removes all TypeScript types, interfaces, and annotations.

- Emits JavaScript: Finally, it creates clean .js files that our browser or Node.js can easily run.

```ts
TypeScript input:

// index.ts
const age: number = 20;
```

```js
JavaScript output:

// index.js
const age = 20;
```

## The Role of tsconfig.json

### The tsconfig.json file is the settings file for the compiler. It tells tsc how to compile our files and what rules to follow.

Here are four common options inside tsconfig.json:

- target: Defines the target JavaScript version for the output (for example, ES2020 or esnext).

- module: Sets the module system to use in the output code, like CommonJS or ESNext.

- outDir: Specifies the folder where the compiled .js files will be stored.

- strict: Enables strict type-checking rules to keep the code safe and clean.

Sample tsconfig.json

```json
{
	"compilerOptions": {
		"rootDir": "./src",
		"outDir": "./dist",
		"module": "esnext",
		"target": "esnext",
		"types": [],
		"strict": true,
		"moduleDetection": "force",
		"skipLibCheck": true
	}
}
```
