# Repository
# Beginner Boot Sequence (Windows Edition)

A standalone Python executable that generates a digital rain animation followed by a system boot sequence. It features autonomous Windows Terminal configuration (ANSI support) and a unique sonic signature generated via the Windows Sound API.

## 🚀 Features

*   **Autonomous Configuration:** Automatically enables ANSI escape codes in the Windows Registry/Kernel via `ctypes`.
*   **Sonic Signature:** Generates a unique 4-note "Boot Complete" arpeggio using `winsound` (no external audio files required).
*   **Matrix Rain Engine:** Randomized digital rain simulation with depth perception (variable dimming).
*   **Keep-Alive Protocol:** Prevents the terminal from closing immediately after execution.

## 📦 Installation

### Prerequisites
*   Python 3.8+
*   Windows 10/11

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/matrix-boot.git
