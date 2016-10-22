# ListDiff

__ListDiff__ is an Swift port of [IGListKit](https://github.com/Instagram/IGListKit)'s [IGListDiff](https://github.com/Instagram/IGListKit/blob/cdc796746adf95d9a9ae78379a29cddf50c9f738/Source/IGListDiff.mm).

## Motivation

The motivation for this project came from the following challenge [challenge](https://github.com/Instagram/IGListKit/issues/76) which I learnt about from [Ryan Nystrom](https://twitter.com/_ryannystrom)'s talk in [iOSConf.SG](http://iosconf.sg).

## Getting Started

```
swift package generate-xcodeproj
```

## Rationale

During the port, I made several decisions which I would like to rationalize here.

- _Using caseless enum as namespace._ See [Erica Sadun's post here](http://ericasadun.com/2016/07/18/dear-erica-no-case-enums/).
- _No support for index paths._ Decided that this is out of the scope.
- _Stack vs Heap._ AFAIK, Swift does not advocates thinking about stack vs heap memory model, leaving the optimization decisions to compiler instead. Nevertheless, some of the guideline do favour `struct` more, so only `List.Entry` is a (final) class as we need reference to its instances.

## issues

- TODO: Equality check.
