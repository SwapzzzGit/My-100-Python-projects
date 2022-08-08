## caesar cipher part- 3

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
alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n")
text = input("Type your message:\n").lower()
shift = int(input("Type the shift number:\n"))
 
def caeser(start_text, shift_amount, cipher_direction):
  end_text = ""
  for letters in start_text:
    position = alphabet.index(letters)
    if direction == "encode":
      new_position = position + shift_amount
    elif direction == "decode":
      new_position = position - shift_amount
    end_text += alphabet[new_position]
  print(f"The {direction}d text is {end_text}.")  

caeser(start_text=text, shift_amount=shift, cipher_direction=direction)
```