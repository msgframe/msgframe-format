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

## Type Prefix Code

| Type         | Prefix      | Description  |
| ------------ | ----------- | ------------ |
| UINT7        | 0xxx xxxx   | unsigned integer 0 to 127 |
| USER6        | 10xx xxxx   | User-defined types (0-63: 6 bits) |
| NIL          | 1100 0000   |              |
| FALSE        | 1100 0010   |              |
| TRUE         | 1100 0011   |              |
| INT8         | 1100 0100   |              |
| INT16        | 1100 0101   |              |
| INT32        | 1100 0110   |              |
| INT64        | 1100 0111   |              |
| BIT3         | 1100 1xxx   | bit value 1-7 bits |
| UINT8        | 1100 1111   | BIT8         |
| UINT16       | 1100 1000   |              |
| UINT32       | 1100 1001   |              |
| FLOAT32      | 1100 1010   |              |
| FLOAT64      | 1100 1011   |              |
| STR8         | 1100 1100   |              |
| STR16        | 1100 1101   |              |
| STR32        | 1100 1110   |              | 
| BIN8         | 1100 1111   |              |
| BIN16        | 1101 0000   |              |
| BIN32        | 1101 0001   |              |
| TIMESTAMP32  | 1101 0010   |              |
| TIMESTAMP64  | 1101 0011   |              |
| TIMESTAMP96  | 1101 0100   |              |
| ARRY8        | 1101 0101   |              |
| ARRY16       | 1101 0110   |              |
| ARRAY32      | 1101 0111   |              |
| MAP8         | 1101 1000   |              |
| MAP16        | 1101 1001   |              |
| MAP32        | 1101 1010   |              |
| DECIMAL64    | 1101 1011   | up-to 18 precision digits |
| DECIMAL128   | 1101 1100   | up-to 38 precision digits |
| NINT4        | 111x xxxx   | Negative int -1 to -32 | 
