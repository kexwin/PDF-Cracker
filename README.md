# PDF-Cracker
PDF-Cracker is a Python tool for cracking password-protected PDF files using either a wordlist (dictionary attack) or a brute-force attack with customizable character sets and password lengths.

# Features
Dictionary Attack: Try passwords from a provided wordlist.

Brute-force Attack: Generate and try all possible passwords based on your character set and length constraints.

Progress Bar: Visual feedback during cracking.

Customizable: Choose character sets, minimum and maximum password lengths.

Simple CLI: Easy to use from the command line.

# Installation
```
git clone https://github.com/kexwin/PDF-Cracker.git
cd PDF-Cracker
```
# Usage
### Dictionary Attack
Crack the password from a wordlist file:
```
python cracker.py your_doc.pdf -w wordlist.txt
```
- your_doc.pdf: Path to the password-protected PDF.

- -w wordlist.txt: Path to your wordlist file (one password per line).

### Brute-force Attack
Generate and try all possible passwords using a custom character set and length:
```
python cracker.py your_doc.pdf -g -min MIN_LENGTH -max MAX_LENGTH -c CHAR_SET
```
- -g: Enable brute-force mode.

- -min MIN_LENGTH: Minimum password length.

- -max MAX_LENGTH: Maximum password length.

- -c CHAR_SET: Characters to use for generating passwords.

# Command-Line Flags
<table>
  <tr>
    <td>Flag</td>
    <td>Description</td>
    <td>Example</td>
  </tr>
  <tr>
    <td>-w <file></td>
    <td>Path to wordlist for dictionary attack</td>
    <td>-w wordlist.txt</td>
  </tr>
  <tr>
    <td>-g</td>
    <td>Enable brute-force (generate) mode</td>
    <td>-g</td>
  </tr>
  <tr>
    <td>-min / -max <int></td>
    <td>Minimum & Maximum password length for brute-force</td>
    <td>-min 1 -max 4</td>
  </tr>
  <tr>
    <td>-c <chars></td>
    <td>Characters to use for brute-force</td>
    <td>-c 1234567890</td>
  </tr>
</table>

# Example 
- Dictionary Attack:
```
python cracker.py my_doc.pdf -w wordlist.txt
```
- Brute-force Attack:
```
python cracker.py my_doc.pdf -g -min 4 -max 4 -c 0123456789
```
