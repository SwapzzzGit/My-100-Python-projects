## caesar cipher part-2

# Problem Statement

write a program that converts normal text into secreat text by encoding as well as decode the encrypted text.<br />(USE : shift number to encde or decode text) 

# Example Input - 1

```
Type 'encode' to encrypt, type 'decode' to decrypt:
encode
Type your message:
hello
Type the shift number:
5

```

# Example Output 

```
The encoded text is mjqqt
```
# Example Input - 2

```
Type 'encode' to encrypt, type 'decode' to decrypt:
decode
Type your message:
mjqqt
Type the shift number:
5

```

# Example Output 

```
The encoded text is hello
```

# Solution
```
alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z','a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n")
text = input("Type your message:\n").lower()
shift = int(input("Type the shift number:\n"))

def encrypt(plain_text,amount_shift):
    cipher_text = ""
    for letters in plain_text:
        position =     alphabet.index(letters)
        new_position = position + amount_shift
        new_letter =   alphabet[new_position]
        cipher_text += new_letter
    print(f"The encoded text is {cipher_text}")

def decrypt(cipher_text,shift_amount):
    plain_text =""
    for letters in cipher_text:
        position = alphabet.index(letters)
        new_position = position - shift_amount
        plain_text += alphabet[new_position]
    print(f"The decoded text is {plain_text}")
if direction == "encode":
    encrypt(plain_text = text,amount_shift = shift)
elif direction == "decode":
    decrypt(cipher_text = text,shift_amount = shift)
```