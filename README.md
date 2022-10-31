[![build status](https://img.shields.io/travis/gcanti/io-ts/master.svg?style=flat-square)](https://travis-ci.org/gcanti/io-ts)
![npm downloads](https://img.shields.io/npm/dm/io-ts.svg)

Build based on [gcanti/io-ts](https://github.com/gcanti/io-ts), and add optional method to
allow to define an optional properties more readable.

```typescript
const AType = t.type({
  a: t.string,
  b: t.optional(t.string), // define an optional property
});

type A = t.TypeOf<typeof AType>;
//// Type A is like following:
// interface A {
//   a: string;
//   b?: string; // define an optional property
// }
```

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Installation](#installation)
- [Usage](#usage)
  - [Stable features](#stable-features)
  - [Experimental features (version `2.2+`)](#experimental-features-version-22)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Installation

To install the stable version

```sh
npm i io-ts fp-ts
```

**Note**. [`fp-ts`](https://github.com/gcanti/fp-ts) is a peer dependency for `io-ts`

# Usage

## Stable features

- [`index.ts` module](index.md)

## Experimental modules (version `2.2+`)

Experimental modules (\*) are published in order to get early feedback from the community, see these tracking [issues](https://github.com/gcanti/io-ts/issues?q=label%3Av2.2+) for further discussions and enhancements.

The experimental modules are **independent and backward-incompatible** with stable ones.

- [`Decoder.ts` module](Decoder.md)
- [`Encoder.ts` module](Encoder.md)
- [`Codec.ts` module](Codec.md)
- [`Eq.ts` module](Eq.md)
- [`Schema.ts` module (advanced feature)](Schema.md)

(\*) A feature tagged as _Experimental_ is in a high state of flux, you're at risk of it changing without notice.
