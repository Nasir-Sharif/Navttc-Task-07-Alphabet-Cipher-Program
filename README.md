# Navttc-Task-07-Alphabet-Cipher-Program

# Caesar Cipher Program

## Description

This Python script implements a Caesar Cipher for encryption and decryption of text. It allows you to encode or decode messages using a specified shift value.

## Code

```python
alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm',
            'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z',
            'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm',
            'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z',
            'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm',
            'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

def caesar(start_text, shift_amount, cipher_direction):
    end_text = ""
    if cipher_direction == "decode":
        shift_amount *= -1
    for char in start_text:
        if char in alphabet:
            position = alphabet.index(char)
            new_position = position + shift_amount
            end_text += alphabet[new_position]
        else:
            end_text += char
    print(f"Here's the {cipher_direction} result: {end_text}")

should_end = False
while not should_end:
    print("Cipher by Nasir Sharif")
    direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n")
    text = input("Type your message:\n").lower()
    shift = int(input("Type the shift number:\n"))

    shift = shift % 26

    caesar(start_text=text, shift_amount=shift, cipher_direction=direction)

    restart = input("Type 'yes' if you want to go again. Otherwise type 'no'.\n")
    if restart == "no":
        should_end = True
        print("Goodbye")
```

## Steps

1. **Define the Alphabet List:**
   - Create a list containing all letters of the alphabet repeated to handle shifts.

2. **Define the `caesar` Function:**
   - This function performs the Caesar Cipher operation by shifting characters in the `start_text` based on the `shift_amount` and `cipher_direction` (either "encode" or "decode").

3. **Get User Input:**
   - Prompt the user for the direction of operation (`encode` or `decode`), the message to be processed, and the shift number.

4. **Normalize the Shift Value:**
   - Ensure the shift value is within the range of 0 to 25 using modulo operation.

5. **Call the `caesar` Function:**
   - Process the message with the given shift and direction.

6. **Allow User to Restart:**
   - Ask the user if they want to perform another operation or exit the program.

## How to Run

1. **Ensure Python is Installed:**
   - Ensure Python is installed on your system. You can download it from [python.org](https://www.python.org/downloads/).

2. **Save the Script:**
   - Save the provided Python code into a file named `07 - Alphabet Cipher Program-Encoded-Decoded (Nasir Sharif).py`.

3. **Execute the Script:**
   - Open a terminal or command prompt.
   - Navigate to the directory where `07 - Alphabet Cipher Program-Encoded-Decoded (Nasir Sharif).py` is saved.
   - Run the script using the following command:
     ```bash
     python 07 - Alphabet Cipher Program-Encoded-Decoded (Nasir Sharif).py
     ```

4. **Follow Prompts:**
   - Enter the desired operation (encode/decode), message, and shift number as prompted.

5. **View Output:**
   - The encoded or decoded result will be displayed in the terminal or command prompt.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or feedback, please contact Nasir Sharif at nasirsharifqasoori786@gmail.com
