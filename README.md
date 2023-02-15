# Expands TS definitions for object-like types

A Typedoc plugin that expands TS definitions for object-like types.

Take the following example.

```ts
export type A = { name: string };
export type B = { age: number };
export type C = A & B & { id: number };
```

With the plugin, type `C` will expand to the following definition in your docs.

```ts};
export type C = {
  name: string;
  age: number;
  id: number;
};
```

## Installation

```shell
npm install typedoc-plugin-expand-object-like-types -D
```

Typedoc will automatically detect this plugin once installed.
