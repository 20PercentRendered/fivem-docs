---
title: Exports
---

Use this to export functions so they can be called from other resources.\
Read more on [exports](http://localhost:1313/scripting-reference/resource-manifest/resource-manifest/#export)

## Signature

```ts
function exports(exportedName: string, fn: Function) => void
```

### Required arguments

- **exportedName**: The function name you want to export.
- **fn**: The function to execute when the export get called.

## Examples

```ts
exports("printSomething", () => {
  console.log("Something");
});
```

```ts
exports("dropPlayer", (src: string, reason: string) => {
  DropPlayer(src, reason);
});

// OR

exports("dropPlayer", DropPlayer);
```
