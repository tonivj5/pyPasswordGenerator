# pyPassGenerator

It's a simple program that it's able to generate randoms, variables length and with custom characters passwords and... it's written in Python!

---

How can I use it?
===
```bash
$ pip install pypassgenerator
```

```python
from pyPassGenerator import generatePass
myPass = generatePass(5, "a", True)
```


Parameters
===

Order | Parameter | What does it do?
--- | --- | ---
0 | *long* | You can choose how long you want to generate your password
1 | *mixVocabulary* | You choose your game of characters
2 | *repeatCharacters* | It lets you or doesn't let you to use characters that it already has used

long - `int`
---
You can choose how long you want to generate your password.

mixVocabulary - `String` - Default: `a`
---
You choose your game of characters.

Value | What does it do?
--- | ---
*a* | All (lower/upper-case vocals, lower/upper-case consonants, numbers and specials)
*v* | Only lower-case vocals
*V* | Only upper-case vocals
*c* | Only lower-case consonants
*C* | Only upper-case consonants
*n* | Only numbers
*s* | Only specials

It's possible to use combinations, for example:

    Cn -> Only upper-case consonants and numbers.

- Example
```python
    generatePass(5, "Cn")
    return '75WT4'
```

If you want to use your own game of characters, you will type '@' at start of parameter, for example:

    @bXcD3 -> Only will be used the characters b, X, c, D and 3.

- Example
```python
    generatePass(5, "@bXcD3")
    return 'X3c33'
```

repeatCharacters - `Boolean` - Default: `True`
---
It lets you or doesn't let you to use characters that it already has used.

Value | What does it do?
--- | ---
*True* | This lets you to repeat characters that it's already in passphrase.
*False* | This doesn't let you to repeat characters that it's already in passphrase.
This parameter is used for generate password with characters that isn't possible to repeat (`True`) or it's possible to repeat (`False`).
