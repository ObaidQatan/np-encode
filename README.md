# np-encode
Linear encoding for strings.

## Example
# 1- Encoding:
```js
import { encode } from 'np-encode';

let str = "Hi this is Obaid";
let enc_str = encode(str);
console.log(enc_str);
```
```bash
^78A+978+8A8+8A^+41083
$~
```

# 2- Decoding:
```js
import { decode } from 'np-encode';

let enc_str = "^78A+978+8A8+8A^+41083";
let str = encode(enc_str);
console.log(str);
```
```bash
Hi this is Obaid
$~
```

# Double Enc.
This can be used with another type of encoding like base64 or some sort of ciphering algorithm:

```js
import { encode } from 'np-encode';

let str = "Hi this is Obaid";
let enc_str = encode(str);

let double_enc_str = Buffer.from(enc_str,"utf-8").toString("base64");
console.log(double_enc_str);
```
```bash
Xjc4QSs5NzgrOEE4KzhBXis0MTA4Mw==
$~
```
