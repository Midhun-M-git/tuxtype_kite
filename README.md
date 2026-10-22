# TuxType Packaging and Compilation Suite

<div align="center">

[![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)](https://isocpp.org)
[![Tux4Kids](https://img.shields.io/badge/Project-Tux4Kids-FF6F00?style=for-the-badge)](https://github.com/tux4kids)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

</div>

Source code integration, packaging configuration, and compilation environment for TuxType (touch typing tutor) and the shared `t4k_common` library.

---

## Build Architecture

```mermaid
graph TD
    T4K[t4k_common Shared Library] --> BuildT4K[Compile Common Utilities & Font Engines]
    BuildT4K --> SharedObj[libt4k_common Shared Objects]
    
    SharedObj --> TuxType[TuxType Typing Tutor Engine]
    TuxType --> TypingGame[Educational Typing Game Binary]
```

---

## Overview

TuxType is an open-source educational typing tutor designed for children and beginners to develop touch-typing agility through interactive arcade mini-games.

---

## Compilation

```bash
# Compile shared library
cd t4kcommon
./configure
make

# Compile TuxType binary
cd ../tuxtype
./configure
make
./src/tuxtype
```

---

## License

This compilation repository is licensed under the MIT License. See [LICENSE](LICENSE) for details. TuxType itself is licensed under GNU General Public License v2.0.
