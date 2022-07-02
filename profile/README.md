# Base16384

A unicode-based encoding scheme that presents binary data (sequence of 8-bit bytes) in sequences of 14-bit printable Chinese characters. It saves 17% space compared to base64.

Inspired by [fumiama/base16384](https://github.com/fumiama/base16384).

## Description

Base16384 uses 16384 (2<sup>14</sup>) Chinese characters (from `\u4E00` to `\u8DFF`) to represent binary data.

A `\u3D0x` is added after the output to represent the remainder modulo 7 of the input length.

## Comparison

|           | Base64          | Base16384         |
| --------- |:---------------:|:-----------------:|
| Overhead  | 33%             | 14%               |
| Charset   | `[0-9a-zA-Z+/]` | `[\u4E00-\u8DFF]` |
| Padding   | `=`             | `[\u3D00-\u3D06]` |
| Example   | `RXhhbXBsZQ==`  | `彞吖菁穥㴀`       |
