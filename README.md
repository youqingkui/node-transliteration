# Transliteration

Transliteration module for node.js. Transliterate unicode characters into latin ones. Supports all common unicode characters including CJK.

## Install

```
npm install transliteration
```

## Usage

### transliterate(str, unknown)

Transliterate `str`. Unknown characters will be converted to `unknown`

__Example__
```javascript
var transliteration = require('transliteration');
transliteration.transliterate('你好，世界'); // Ni Hao ,Shi Jie
```

### slugify(str, options)

Convert unicode string to slugs. It can be savely used in URL or file name.
You can provide an `options` parameter in the form of
```
{
  lowercase: true,
  separator: '-'
}
```
Leave it blank to use the above default values.

__Example__
```javascript
var transliteration = require('transliteration');
transliteration.slugify('你好，世界'); // ni-hao-shi-jie
transliteration.slugify('你好，世界', {lowercase: false, separator: '_'}); // Ni_Hao_Shi_Jie
```
