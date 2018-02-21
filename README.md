# censor-vowel
v 1.0.0
Replaces the vowels in a string with a provided character as string or default character.

## Installation
Download or clone this repository and direct your terminal to this directory.
Execute the following code in your terminal:
```
npm install censor-vowel
```
## API
**`censorVowel(value, character)`**
Where the value is meant to be a string, and the character is meant to be a string containing a character to replace the vowels in the given value with.

## Usage
If you want to use vowel in one of your files within this directory you need to include it in the top of your js file.
Your next move is to provide it with a string that contains vowels to replace and optionally what character they should be replaced with
```js
var censorVowel = require("censor-vowel");

censorVowel("Vowel") // => "V*w*l" (default)
censorVowel("Vowel", "%") // => "V&w&l"
```

### Methods
censor-vowel comes with a few methods:
* inner
* grawlix

### Methods Usage

#### Inner
```js
var censorVowel = require("censor-vowel")

censorVowel.inner("Vowel") // => "V****l" (default)
censorVowel.inner("Vowel", "%") // => "V&&&&l"
```

#### Grawlix
Grawlix works a little different. Instead of giving it a character to replace vowels or the string with, you give it a pattern to replace the characters.
Once the pattern (in this example 6 characters long) has replaced the first 6 characters it will repeat te pattern to replace the leftover characters.
TL;DR: grawlix replaces an entire string with a pattern provided as string.
```js
var censorVowel = require("censor-vowel")

censorVowel.grawlix("Vowel"); // => "@#$%!" (default)
censorVowel.grawlix("SlightlyLongerVowel", "&X!3@*"); // => "&X!3@*&X!3@*&X!3@*&"
```

## License
[MIT](LICENSE.md) © [Folkert-Jan van der Pol](https://github.com/FJvdPol)

## Special Thanks
This readme was written after using the [README.md](https://github.com/wooorm/ccount#readme) from [Titus Wormer](https://github.com/wooorm) as an example.
