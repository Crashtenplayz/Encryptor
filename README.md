# Encryptor/Decryptor

A simple and secure file encryption/decryption tool with a graphical user interface (GUI) built using Python and Tkinter. The app uses strong encryption (Fernet with PBKDF2 and per-file salt) and a secret key stored in your Documents folder. The app icon is customizable.

## Features
- Encrypt and decrypt any file with a single click
- Uses a unique salt for each file for extra security
- Secret key is generated and stored automatically in your Documents folder
- Encrypted files use the `.loc` extension
- Simple drag-and-select GUI (no command line needed)
- Custom app icon for both the executable and the window


## How to Use

### 1. For End Users (No Python Needed)
- Double-click `encryptor.exe` to run the app.
- No Python installation or setup is required.

### 2. Usage
- Click "Encrypt Files" to select and encrypt files (they will get a `.loc` extension).
- Click "Decrypt Files" to select and decrypt `.loc` files.
- The secret key is saved as `.secret_key` in your Documents folder. Do not delete this file or you will lose access to your encrypted files.

## Security Notes
- Each file is encrypted with a unique salt and a key derived from your secret key.
- Only this app (with your `.secret_key`) can decrypt your files.
- Keep your `.secret_key` safe!

## License
MIT License
