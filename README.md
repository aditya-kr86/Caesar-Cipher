# Caesar Cipher Game 🔐

Welcome to the **Caesar Cipher Game**! This project features a fun twist on the classic cipher technique, allowing you to encode and decode secret messages with an added layer of randomness.

## Project Description

The **Caesar Cipher Game** is a simple Python application that lets you encode and decode messages using a modified Caesar cipher technique. The project uses ASCII art for a visual appeal and provides a unique way to shuffle and protect your secret messages.

## Features

- **Encode Messages**: Transforms your input message into a ciphered text with random characters for extra obfuscation.
- **Decode Messages**: Reverts the encoded message back to its original form.
- **Interactive Gameplay**: Offers a user-friendly input interface with clear options for encoding and decoding.
- **Visual ASCII Art**: Displays a logo using ASCII art for a polished look.

## How It Works

### Encoding Process

1. **Reverse Short Words**: Words with 2 or fewer characters are simply reversed.
2. **Shuffle Longer Words**:
   - Adds 3 random lowercase letters to both the beginning and end of the word.
   - Moves the first character of the word to the end.
   - Combines these steps to form the encoded word.
   
### Decoding Process

1. **Reverse Short Words**: Simply reverse the word back.
2. **Reconstruct Longer Words**:
   - Removes the first and last 3 random characters.
   - Moves the last character to the front to reconstruct the original word.

### Example

```
 $$$$$$\                                                                    $$\           $$\                           
$$  __$$\                                                                   \__|          $$ |                          
$$ /  \__| $$$$$$\   $$$$$$\   $$$$$$$\  $$$$$$\   $$$$$$\         $$$$$$$\ $$\  $$$$$$\  $$$$$$$\   $$$$$$\   $$$$$$\  
$$ |       \____$$\ $$  __$$\ $$  _____|$$  __$$\ $$  __$$\       $$  _____|$$ |$$  __$$\ $$  __$$\ $$  __$$\ $$  __$$\ 
$$ |       $$$$$$$ |$$$$$$$$ |\$$$$$$\  $$$$$$$$ |$$ |  \__|      $$ /      $$ |$$ /  $$ |$$ |  $$ |$$$$$$$$ |$$ |  \__|
$$ |  $$\ $$  __$$ |$$   ____| \____$$\ $$   ____|$$ |            $$ |      $$ |$$ |  $$ |$$ |  $$ |$$   ____|$$ |      
\$$$$$$  |\$$$$$$$ |\$$$$$$$\ $$$$$$$  |\$$$$$$$\ $$ |            \$$$$$$$\ $$ |$$$$$$$  |$$ |  $$ |\$$$$$$$\ $$ |      
 \______/  \_______| \_______|\_______/  \_______|\__|             \_______|\__|$$  ____/ \__|  \__| \_______|\__|      
                                                                                $$ |                                    
                                                                                $$ |                                    
                                                                                \__|                                    
```

```
Enter Which Action You want to Perform - ENCODE/DECODE or Enter EXIT to skip this: encode
Enter the message: hello world
Encoded message is: rsihelolx ocgwrldzwj
```

```
Enter Which Action You want to Perform - ENCODE/DECODE or Enter EXIT to skip this: decode
Enter the message: rsihelolx ocgwrldzwj
Decoded message is: hello world
```

## Prerequisites

- Python 3.x installed on your system.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/aditya-kr86/Caesar-Cipher.git
   ```

2. **Navigate to the project folder**:
   ```bash
   cd Caesar-Cipher
   ```

3. **Run the script**:
   ```bash
   python caesar_cipher.py
   ```

## Project Files

The project includes the following files:

- **`caesar_cipher.py`**: The main game logic for encoding and decoding messages.
- **`ascii.py`**: Contains the ASCII art logo for visual display.

### Project Structure

```
Caesar-Cipher/
├── README.md
├── caesar_cipher.py
└── ascii.py
```

## Code Explanation

1. **Message Encoding**:
   - Splits the message into words.
   - Reverses words with 2 or fewer characters.
   - For longer words, it appends random characters and shuffles the word.
2. **Message Decoding**:
   - Reverses the short words.
   - Removes added random characters and reconstructs the original word.
3. **User Input**:
   - Allows the user to choose between encoding, decoding, or exiting the program.

### Example Code Snippet

```python
if len(word) <= 2:
    word = word[::-1]
else:
    random_chars1 = ''.join(random.choices(string.ascii_lowercase, k=3))
    random_chars2 = ''.join(random.choices(string.ascii_lowercase, k=3))
    word = word[1:] + word[0]
    word = random_chars1 + word + random_chars2
```

## Contributing

Contributions are welcome! If you have any ideas for improvements or new features, feel free to fork the repository and submit a pull request.

## Author

- [Aditya Kumar](https://github.com/aditya-kr86)

## License

This project is open-source and available under the MIT License.

## Feedback

For any feedback or suggestions, please reach out to me at [adityakumargupta082003@gmail.com](mailto:adityakumargupta082003@gmail.com).
