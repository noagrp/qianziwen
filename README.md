# 千字文

A structured, reusable reader and explanation dataset for the traditional Chinese primer 《千字文》.

## Content architecture

- `data/qianziwen.json` — source metadata, original text, explanations, vocabulary notes and cultural notes
- `src/qianziwen-engine.js` — reusable navigation and full-text search engine
- `index.html` — reader UI only
- `manifest.webmanifest` / `sw.js` — PWA support

The JSON is intentionally independent from the website so other projects can reuse the material without parsing HTML.

## Base text

V1 follows the common received text of 《千字文》 attributed to 南朝梁·周兴嗣, checked against Chinese Wikisource and the Chinese Text Project.

Wikisource:
https://zh.wikisource.org/wiki/%E5%8D%83%E5%AD%97%E6%96%87

Chinese Text Project:
https://ctext.org/wiki.pl?if=gb&res=386897

The Wikisource page records multiple textual variants. This project uses one consistent common reading in the main text rather than silently mixing variant characters into the same line.

## Editorial rule

The explanation first explains what the original sentence actually says. Historical context, allusions, institutions, astronomy, geography and modern cautions belong in the cultural note. Generic repeated statements should be avoided.

Original text is kept in Traditional Chinese. Explanations and notes are newly written in Simplified Chinese.
