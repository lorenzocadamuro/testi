# Testi
Create text styles with Sass.

## Install

```sh
npm install testi
```

## Syntax

```
@include testi(presetName, fontSize, lineHeight, fontWeight, letterSpacing);
```

## Configuration

Use the global variable ```$testi``` to configure your text styles; every css property is accepted.<br />
You can extend an existing preset using the ```extend``` attribute.

```sass
$testi: (
  "roboto": (
    font-family: 'Roboto',
    color: #111,
    antialiased: true // not required, true by default
  ),
  "title-1": (
    extend: "roboto",
    font-size: 4.0rem,
    line-height: 1.3em,
    letter-spacing: 0.1em
  ),
  "title-2": (
    extend: "title-1", // inherit the proporties of "title-1" preset
    font-size: 3.2rem,
    color: #0084ff
  ),
  "paragraph": (
    extend: "roboto",
    font-size: 1.8rem,
    line-height: 1.3em,
    font-weight: 300
  )
);
```

## Usage

```sass
@import "node_modules/testi/testi";
```

```sass
.box__title  {
  @include testi("title-1");
}
.box__subtitle {
  @include testi("title-2");
}
.box__description {
  @include testi("paragraph");
}
```
