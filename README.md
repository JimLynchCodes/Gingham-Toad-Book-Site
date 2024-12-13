# Gingham-Toad-Book-Site

Book code snippets:

original function:

```typescript
function fizzbuzzify (input: string) {
  return input
    .split(" ")
    .map(word, i) => {
      if ((i + 1) % 15 === 0) {return "fizzbuzz"}
      else if ((i + 1) % 5 === 0) {return "buzz"}
      else if ((i + 1) % 3 === 0) {return "fizz"}
      else {return word}
    })
    .join(" ");
}
```

function after fix, adds the filter line:
```typescript
function fizzbuzzify (input: string) {
  return input
    .split(" ")
    .filter(item => item !== "")
    .map(word, i) => {
      if ((i + 1) % 15 === 0) {return "fizzbuzz"}
      else if ((i + 1) % 5 === 0) {return "buzz"}
      else if ((i + 1) % 3 === 0) {return "fizz"}
      else {return word}
    })
    .join(" ");
}
```


function after refactoring, removing elses and braces:
```typescript
function fizzbuzzify (input: string) {
  return input
    .split(" ")
    .filter(item => item !== "")
    .map(word, i) => {
      if ((i + 1) % 15 === 0) return "fizzbuzz";
      if ((i + 1) % 5 === 0) return "buzz";
      if ((i + 1) % 3 === 0) return "fizz";
      return word;
    })
    .join(" ");
}
```


