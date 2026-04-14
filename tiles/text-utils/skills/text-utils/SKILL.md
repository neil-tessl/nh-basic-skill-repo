# Text Utils

A lightweight text utility library for formatting, slugifying, and transforming strings in TypeScript projects.

## When to use

Use `text-utils` when you need to:

- Convert user input or titles into URL-safe slugs
- Truncate long strings for display in UI components
- Capitalize words for headings or labels
- Convert between camelCase and kebab-case naming conventions
- Count words in a body of text

## Installation

```bash
npm install text-utils
```

## Usage

### Slugify text for URLs

```ts
import { slugify } from "text-utils";

slugify("Hello World!"); // "hello-world"
slugify("  Multiple   spaces  "); // "multiple-spaces"
slugify("Special @#$ Characters"); // "special-characters"
```

### Truncate long strings

```ts
import { truncate } from "text-utils";

truncate("A very long string that needs trimming", 20); // "A very long strin..."
truncate("Short", 20); // "Short"
```

### Capitalize first letter

```ts
import { capitalize } from "text-utils";

capitalize("hello"); // "Hello"
capitalize("already Capitalized"); // "Already Capitalized"
```

### Convert camelCase to kebab-case

```ts
import { camelToKebab } from "text-utils";

camelToKebab("backgroundColor"); // "background-color"
camelToKebab("fontSize"); // "font-size"
```

### Count words

```ts
import { wordCount } from "text-utils";

wordCount("The quick brown fox"); // 4
wordCount("  spaced  out  "); // 2
```

## API Reference

| Function | Signature | Description |
|---|---|---|
| `slugify` | `(text: string) => string` | Converts text to a URL-safe slug |
| `truncate` | `(text: string, maxLength: number) => string` | Truncates text with ellipsis |
| `capitalize` | `(text: string) => string` | Capitalizes the first character |
| `camelToKebab` | `(text: string) => string` | Converts camelCase to kebab-case |
| `wordCount` | `(text: string) => number` | Counts words in a string |
