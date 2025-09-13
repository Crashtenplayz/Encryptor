# File Encryptor/Decryptor

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
- Simply use the files in the `dist` folder: `encrypted_gui.exe` and `appicon.ico` (if required by the app).
- Double-click `encrypted_gui.exe` to run the app.
- No Python installation or setup is required.

### 2. For Developers (Building the .exe)
- Requirements:
  - Windows OS
  - Python 3.8+
  - The following Python packages:
    - cryptography
    - tkinter (usually included with Python)
    - pyinstaller (for building .exe)
- Place `encrypted_gui.py` and `appicon.ico` in the same folder.
- Make sure `appicon.ico` is a valid Windows icon file (multi-size recommended).
- Install dependencies:
  ```powershell
  python -m pip install cryptography pyinstaller
  ```
- Build the .exe:
  ```powershell
  python -m PyInstaller --onefile --windowed --icon appicon.ico encrypted_gui.py
  ```
  The `.exe` will be in the `dist` folder. Place `appicon.ico` next to the `.exe` if needed.

### 3. Usage
- Click "Encrypt Files" to select and encrypt files (they will get a `.loc` extension).
- Click "Decrypt Files" to select and decrypt `.loc` files.
- The secret key is saved as `.secret_key` in your Documents folder. Do not delete this file or you will lose access to your encrypted files.

## Security Notes
- Each file is encrypted with a unique salt and a key derived from your secret key.
- Only this app (with your `.secret_key`) can decrypt your files.
- Keep your `.secret_key` safe!

## Customization
- To change the app icon, replace `appicon.ico` with your own valid `.ico` file and rebuild the `.exe`.

## License
MIT License
