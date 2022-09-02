# Encoding
## ASCII
- American Standard Code for Information Interchange
- Uses 7 bits so has a 128 character set
- The basic standard for representing the English alphabet
- `a` = `97` = `1100001`

## Unicode
- Universal character set
- Has enough bits to store non-English characters Ж as well as Emoji 😃

## URL encoding
- URLs can only be transmitted using the ASCII character set
- Replaces unsafe ASCII characters with a `%` followed by 2 hexadecimal digits e.g. `space` = `%20`

## Base64
- Binary-to-text encoding scheme that represents binary data in an ASCII string format
- Each Base64 digit represents exactly 6 bits of data
- Text which does not divide into the 6-bit pattern cleanly is padded using `=`