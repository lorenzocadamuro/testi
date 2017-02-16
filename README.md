# Testi
Create text styles with Sass.

## Install

```sh
npm install testi
```

## Usage

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

## Setup

Use the global variable ```$testi``` to configure your text styles.<br />
You can extend an existing preset using the ```extend``` attribute.

```sass
$testi: (
  "title-1": (
    font-family: "Helvetica",
    font-size: 20rem,
    line-height: 1.3em,
    letter-spacing: 0.05em
  ),
  "title-2": (
    extend: "title-1", // inherit the proporties of "title-1" preset
    font-size: 16rem
  ),
  "paragraph": (
    font-family: "Helvetica",
    font-size: 14rem,
    line-height: 1.3em,
    font-weight: 300
  ),
);
```

This is the default configuration of a preset:

```sass
$preset: (
  font-family: sans-serif,
  font-size: 1em,
  line-height: 1em,
  font-weight: 400,
  letter-spacing: 0em,
  antialiased: true
);
```
