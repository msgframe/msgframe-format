# MessageFrame Format 

## Primitive Types

- __NIL__: null value
- __BOOLEAN__: false or true
- __INTEGER__: 8, 16, 32, and 64-bit signed integers
  - __BIT__:  1-7 bit integers
- __FLOAT__: 32, 64-bit IEEE 754 floating point numbers
- __DECIMAL__: Arbitrary precision signed integers
- __STRING__ UTF-8 string values
- __BINARY__: Binary data. BASE64 encoding will be used for JSON representation  
- __TIMESTAMP__: 32, 64, 96-bit timestamp representation in UTC
- __ARRAY__: Fixed-length array
- __MAP__: Fixed-length key-value pairs

## Format

| Type         | Prefix      | Description  |
| ------------ | ----------- | ------------ |
| STR5         | 100x xxxx   | UTF-8 strings up to 32-bytes (5-bits) |
| ARRAY4       | 1010 xxxx   | Array up to size 16 (4 bits)          |
| MAP4         | 1011 xxxx   | Array up to size 16 (4 bits)          |
| NIL          | 1100 0000   |              |


| FALSE        | 0000 0010   |              |
| TRUE         | 0000 0011   |              |
| INT8         | 0000 0100   |              |
| INT16        | 0000 0101   |              |
| INT32        | 0000 0110   |              |
| INT64        | 0000 0111   |              |
| BIT1         | 0000 1000   |              |
| BIT2         | 0000 1001   |              |
| BIT3         | 0000 1010   |              |
| BIT4         | 0000 1011   |              |
| BIT5         | 0000 1100   |              |
| BIT6         | 0000 1101   |              |
| BIT7         | 0000 1110   |              |
| UNDEFINED    | 0000 1111   |              |
| FLOAT32      | 0001 0000   |              |
| FLOAT64      | 0001 0001   |              |
| DECIMAL32    | 0001 0010   |              |
| DECIMAL64    | 0001 0011   |              |
| DECIMAL(P,S) | 0001 0100   | precision, scale     |
| STR8         | 0001 0101   | UTF-8 string up to 8-bit length |
| STR16        | 0001 0110   |              |
| STR32        | 0001 0111   |              |
| BIN8         | 0001 1000   |              |
| BIN16        | 0001 1001   |              |
| BIN32        | 0001 1010   |              |
| TIMESTAMP32  | 0001 1011   |              |
| TIMESTAMP64  | 0001 1100   |              |
| TIMESTAMP96  | 0001 1101   |              |
| ARRAY16      | 0001 1110   |              |
| ARRAY32      | 0001 1111   |              |
| ARRAY32      | 0001 1101   |              |
  MAP16        | 0001 1101   |              |
  MAP32        | 0001 1101   |              |
