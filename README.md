# postcss-strip-comments
>
> A very lightweight PostCSS plugin to strip comments. No configuration available at this time.

## Installation

```sh
yarn add -D postcss-strip-comments
```

## Usage

```sh
postcss -u postcss-strip-comments -o dist/index.css src/index.css
```

This plugin turns this:

```css
/**
  * This is my class that spans multiple lines
  */
.lightest {
    /* These are my variables */
  --a: #fff;
  --b: rgba(255, 255, 255, 0.8);
  --c: 10px;
  --d: block;
  --e: var(--a);

/* These are my properties */
  text-transform: capitalize;
  color: var(--e);
  display: var(--d);
  font-size: var(--c, 18px);
}
```

Into this:

```css
.lightest {
  --a: #fff;
  --b: rgba(255, 255, 255, 0.8);
  --c: 10px;
  --d: block;
  --e: var(--a);
  text-transform: capitalize;
  color: var(--e);
  display: var(--d);
  font-size: var(--c, 18px);
}

```
