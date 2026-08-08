# Repository
# Beginner Boot Sequence (Windows Edition)

A standalone Python executable that generates a digital rain animation followed by a system boot sequence. It features autonomous Windows Terminal configuration (ANSI support) and a unique sonic signature.

## 🚀 Features

*   **Autonomous Configuration:** Automatically enables ANSI escape codes in the Windows Registry/Kernel via `ctypes`.
*   **Sonic Signature:** Generates a unique 4-note "Boot Complete" arpeggio using `winsound` (no external audio files required).
*   **Matrix Rain Engine:** Randomized digital rain simulation with depth perception (variable dimming).
*   **Keep-Alive Protocol:** Prevents the terminal from closing immediately after execution.

## 📦 Installation

### Prerequisites
*   Python 3.8+
*   Windows 10/11
*   pip (Python package manager)

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/TECHaxper/Repository.git
   cd Repository
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Install the build tool (only required for compiling):
   ```bash
   pip install pyinstaller
   ```

## 🔨 Building the Executable

Once PyInstaller is installed, you can create a standalone `.exe` file:

```bash
pyinstaller --onefile --windowed boot_sequence.py
```

This will generate a single executable file in the `dist/` folder that can be run on any Windows system without requiring Python to be installed.

### PyInstaller Options

*   `--onefile`: Bundles everything into a single executable
*   `--windowed`: Hides the console window on startup
*   `-i icon.ico`: Add a custom icon to the executable (optional)
*   `--distpath ./output`: Specify custom output directory

## 🎮 Usage

### Running the Python Script
```bash
python boot_sequence.py
```

### Running the Compiled Executable
Simply double-click the `.exe` file in the `dist/` folder or run from the command line:
```bash
dist/boot_sequence.exe
```

## 📋 Requirements

Create a `requirements.txt` file with:
```
pyinstaller>=5.0.0
```

## 📝 Notes

*   The program automatically detects and configures Windows Terminal for ANSI color support on first run.
*   The executable is self-contained and can be distributed independently.
*   Sound generation uses Windows `winsound` module (Windows-only).

## 📄 License

[Add your license here]

## 👤 Author

TECHaxper
