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

## 🎮 Usage

### Run from Source
```bash
python matrix_boot.py
```

### Compile to .exe (Standalone)

To build a single-file executable that runs without Python installed:

```bash
pyinstaller --onefile --clean --name "MatrixBoot" matrix_boot.py
```

The executable will appear in the `dist/` folder.

## 🔨 Building the Executable

Once PyInstaller is installed, you can create a standalone `.exe` file:

```bash
pyinstaller --onefile --windowed boot_sequence.py
```

This will generate a single executable file in the `dist/` folder that can be run on any Windows system without requiring Python to be installed.

### PyInstaller Options

*   `--onefile`: Bundles everything into a single executable
*   `--windowed`: Hides the console window on startup
*   `--clean`: Removes temporary build files before compilation
*   `--name "MatrixBoot"`: Sets the output executable name
*   `-i icon.ico`: Add a custom icon to the executable (optional)
*   `--distpath ./output`: Specify custom output directory

## 📂 Configuration

To run this script on Windows startup:

1. Press `Win + R` and type `shell:startup`
2. Place a shortcut to `MatrixBoot.exe` in this folder

## 📋 Requirements

See `requirements.txt` for dependencies:
```
pyinstaller
```

## 📝 Notes

*   The program automatically detects and configures Windows Terminal for ANSI color support on first run.
*   The executable is self-contained and can be distributed independently.
*   Sound generation uses Windows `winsound` module (Windows-only).

## 📄 License

MIT License

## 👤 Author

TECHaxper

## 🚀 Deployment Protocol

### Initialization Sequence

Open your terminal in the folder where you saved these files and run these commands in order:

#### 1. Initialize Git
```bash
git init
```

#### 2. Stage Files
```bash
git add .
```

#### 3. Commit Artifacts
```bash
git commit -m "Initial commit: Matrix Boot Sequence v1.0"
```

#### 4. Link & Push

Go to [GitHub.com](https://github.com), create a new repository, copy the URL, and run:

```bash
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```
