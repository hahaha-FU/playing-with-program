#  Simple Password Check

## Description
This Python program reads a password from standard input and checks it against a hidden correct value.  
You need to determine what the password should be to get the flag.

## Goal
- Understand how the program reads and checks the password.
- Figure out the correct input format.

## Hints
- The password is a simple byte string.
- Pay attention to how the program reads input (`sys.stdin.buffer.read1()`).
- Remove any leading/trailing whitespace.

## Notes
- This is the first step in learning how to read and analyze programs safely.
__________
#  Another Password

## Description
Similar to Challenge 1, this program requests a password but uses a different hidden value.

## Goal
- Analyze the Python program to understand the correct password.

## Hints
- Input format is raw bytes.
- Use hex or direct byte input if necessary.
- Compare input length with the expected length printed by the program.
_________
# Newline Awareness

## Description
The program reads input and warns if there are newlines (`\n`) in the entered password.

## Goal
- Provide the correct password while avoiding newlines.

## Hints
- Editors sometimes add a newline at the end of files; strip them before submission.
- Check the byte length printed to understand the input expected.
_____________
# Password From File

## Description
This program reads the password from a local file named `xthd`.  
It warns if there are newlines in the input.

## Goal
- Analyze the program and prepare the input file correctly.
- Avoid newlines.

## Hints
- Make sure the file contains the exact byte sequence expected.
- Strip any extra characters automatically added by editors.
______________
# Password From File Argument

## Description
The program reads a password from a file provided as a command-line argument.

## Goal
- Understand the required input format for the file.
- Avoid newlines if present.

## Hints
- The program will exit if the file does not exist.
- The correct password is in bytes, not a string.
________________
# Hex Input

## Description
The program expects input in hex format and converts it before checking.

## Goal
- Provide the correct hex string representing the password bytes.

## Hints
- Use `bytes.fromhex()` to understand what the program expects.
- Input must be hex without spaces.
________________
# Multi-byte Hex

## Description
The program uses multiple bytes as the password, entered in hex.

## Goal
- Convert your password to the expected hex format before submission.

## Hints
- Input is hex encoded; remove any whitespace.
- Compare the byte length printed to verify correctness.
_____________
# Hex Password Decoding

## Description
The program expects a password that must be hex-decoded before comparison.

## Goal
- Prepare input in hex, convert to bytes internally.

## Hints
- Check the code for any intermediate conversions.
- Remove spaces and newlines before hex encoding.
________________
# Double Hex Decoding

## Description
The program may require multiple rounds of hex decoding.

## Goal
- Understand how many times to decode the input to get the correct bytes.

## Hints
- Follow the decoding process shown in the program.
- Avoid any extra characters in input.
_____________
# Binary Bits Encoding

## Description
This challenge encodes the password in binary bits (`0` and `1`) before checking.

## Goal
- Convert your input into bits, following 8 bits per byte.

## Hints
- Input must be complete bytes (multiples of 8 bits).
- The program will assert if invalid characters are present.
____________
# Bitstream Conversion

## Description
Similar to Challenge 10, the program converts a bitstream into bytes.

## Goal
- Convert input bits correctly to match the expected byte sequence.

## Hints
- Use big-endian conversion (`int.to_bytes()`).
- Ensure correct byte length.
_________________
# Hex From File

## Description
Password is read from a file and hex-decoded.

## Goal
- Prepare the input file in correct hex format.

## Hints
- Only one round of hex decoding is needed here.
___________
# Multiple Hex Decoding

## Description
Password requires multiple rounds of hex decoding from file input.

## Goal
- Determine how many rounds of decoding are needed.

## Hints
- Check how many `bytes.fromhex()` calls the program uses.
_______________
#  Emoji Password

## Description
The password consists of emojis encoded in UTF-8 and hex-decoded.

## Goal
- Understand how to encode emojis into the format expected.

## Hints
- Use `utf-8` encoding.
- Hex decode the input once before checking.
_____________
# UTF-16 Conversion

## Description
The program reads a password from file, decodes from UTF-16, then encodes to Latin-1 before checking.

## Goal
- Prepare the input file in UTF-16 format.

## Hints
- Editors may introduce BOM; avoid extra characters.
- Do not use the correct password as-is; process it through UTF-16 -> Latin-1.
______________
# Reverse + Hex

## Description
The program reverses your input and then hex-decodes it.

## Goal
- Reverse your input string before converting from hex.

## Hints
- Make sure hex string is valid after reversing.
- Strip whitespace or newlines.
_______________
#  Base64 Password

## Description
Password is base64-encoded before comparison.

## Goal
- Encode your password in base64 correctly.

## Hints
- Check if the program double-encodes or single-encodes.
- Remove any padding or whitespace issues.
______________
# Base64 + Raw Bytes

## Description
Program decodes base64 input into raw bytes for checking.

## Goal
- Provide input base64-encoded to match the expected byte sequence.

## Hints
- Use proper base64 encoding without newlines.
__________________
# Bits + Base64

## Description
Password is converted to bits, base64-encoded twice, then converted to bits again.

## Goal
- Follow the encoding steps carefully.

## Hints
- Use `format(c, "08b")` to encode bytes into bits.
- Apply base64 encodings in the correct order.
____________
# Complex Base64 + Bits

## Description
Program combines bit encoding and double base64 encoding.

## Goal
- Encode your password in the exact sequence expected by the program.

## Hints
- Pay attention to byte order and bitstream conversion.
- Keep consistent encoding format throughout.
___________
#Final Hex + File Input

## Description
Reads password from file, hex-decodes multiple times.

## Goal
- Prepare input file with multiple rounds of hex decoding.

## Hints
- Count `bytes.fromhex()` calls in the program to know how many times to decode.
- Ensure no newlines or extra spaces.
________________

