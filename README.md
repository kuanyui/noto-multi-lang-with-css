# Noto Fonts and CSS for Multi-Languages

# What is and Why This?
- Pre-build Noto Sans Fonts (woff2) + pre-defined `@font-face` with appropriate `src: local()` and `unicode-range:` definitions. So the correcponding fonts will be lazy-loaded only when it indeedly needed in the page.
- Use this repo as submodule, to prevent your project repo from storing lots of large-sized font binary files.
> According to Noto's issue tracker, Due to the limitation of font format, the glyphs amount is limited in a font file, so Noto doesn't provide a font dist containing all languages

# Supported Alphabets / Characters
- Latin / Cyrillic / Greek
- CJK -- Kanji (Japanese Standard), Hangul, Katakana, Hiragana, Bopopmofo
- Arabic
- Hebrew

# Q & A
## What are the Unicode ranges?
Check the reference at https://jrgraphix.net/r/Unicode/ or [unicode-reference.md](/unicode-reference.md) in this repo.

## Why some unused font files?
Just ignore them, they are remained because they can be used to replace existing fonts easily.

And you can use Webpack's `css-loader` + `file-loader`, so the additional fonts won't be added into your dist bundle, don't worry about it.

## Why not all fonts are `woff2`?
Because I'm lazy.

Use [kombu](https://kombu.kanejaku.org/) to convert fonts into `woff2` in browser, but it can process one font at a time. So I'm too lazy to convert all of them currently.

