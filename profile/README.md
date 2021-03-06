# Base16384

Base16384 is a unicode-based encoding scheme that presents binary data (sequence of 8-bit bytes) in sequences of 14-bit printable Chinese characters. It saves 17% space compared to base64.

The famous project [go-cqhttp](https://github.com/Mrs4s/go-cqhttp) has built-in support for this encoding.

## Introduction

### Design

Base16384 uses 16384 (2<sup>14</sup>) Chinese characters (from `\u4E00` to `\u8DFF`) to represent binary data.

A `\u3D0x` is added after the output to represent the remainder modulo 7 of the input length.

### Comparison

|           | Base64          | Base16384         |
| --------- |:---------------:|:-----------------:|
| Overhead  | 33%             | 14%               |
| Charset   | `[0-9a-zA-Z+/]` | `[\u4E00-\u8DFF]` |
| Padding   | `=`             | `[\u3D00-\u3D06]` |
| Example   | `RXhhbXBsZQ==`  | `彞吖菁穥㴀`       |

## Awesome Projects

If you are developing related projects, feel tree to submit a pull request.

### Implementations

- C: [fumiama/base16384](https://github.com/fumiama/base16384) (original idea)
- Go: [fumiama/go-base16384](https://github.com/fumiama/go-base16384)
- JavaScript: [base16384/base16384.js](https://github.com/base16384/base16384.js)

### Usages

- [Mrs4s/go-cqhttp](https://github.com/Mrs4s/go-cqhttp)
