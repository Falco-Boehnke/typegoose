---
title: "Environment Variables"
---

Typegoose allow the use of some Environment variables to set global options

## Variables

### TG_USE_NEW_ENUM

Set's the global options [`globalOptions.useNewEnum`]({{ site.baseurl }}{% link _docs/functions/setGlobalOptions.md%}#usenewenum) to `true`

### TG_ALLOW_MIXED

Set's the options [`options.allowMixed`]({{ site.baseurl }}{% link _docs/decorators/modelOptions.md%}#allowmixed) to the given Severity

Accepts:
- numbers, in the range of `Severity`
- strings, in the range of `Severity`

## Examples

```sh
TG_USE_NEW_ENUM=1 npm run script # result: "globalOptions.useNewEnum" is now true

TG_USE_NEW_ENUM= npm run script # result: "globalOptions.useNewEnum" is now false
```

```sh
TG_ALLOW_MIXED=ALLOW npm run script # result: "options.allowMixed" is now "ALLOW" (actual: 0)

TG_ALLOW_MIXED=0 npm run script # result: "options.allowMixed" is now "ALLOW" (actual: 0)
```