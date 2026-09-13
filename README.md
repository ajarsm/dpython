# d/Python

**Python 3 for the browser, the desktop, and the 8-bit home computers d/OS runs on.**
You write ordinary Python 3; it compiles to one small program file that runs the
same way everywhere, with windows, buttons, sound, drag and drop and typed objects
as plain Python calls. No interpreter ships with your program.

- **Try it now:** https://dpython.kallinnovations.com/playground/
- **Guide, tutorials, what works today:** https://dpython.kallinnovations.com/
- **Downloads:** the [Releases](../../releases) page on this repository

This repository holds the downloadable releases only. The source is not published.

## Downloads

Each release carries:

| Archive | What it is |
| --- | --- |
| `dpython-<version>-macos-universal.zip` | the `dpython` compiler and command line and the `dbasic` window host, universal (Apple silicon and Intel), with compiled examples, docs and compatibility tables |
| `dpython-<version>-linux-x64.tar.gz` | the same kit for Linux x86-64 (console programs today; window hosts to come) |
| `dpython-<version>-windows-x64.zip` | the same kit for Windows x86-64 (console programs today; window hosts to come) |
| `dpython-<version>-wasm.zip` | the compiler and runtime as WebAssembly with the JavaScript loader, for embedding in your own site |

Every archive has a `manifest.json` with the source commit and the SHA-256 of every
file, and the release notes list the SHA-256 of each archive.

## Licence

Free to download and use, including commercially. **What you build with it is yours:**
no royalty, no attribution, no licence terms attach to your programs. The toolchain
itself is not open source; see [LICENSE.txt](LICENSE.txt). Third-party components
(the RustPython parser, a translation of CPython's sort, the fonts) keep their own
licences, listed in each archive's `third_party/`.

Python is a trademark of the Python Software Foundation; d/Python is not affiliated
with or endorsed by the PSF.

© 2026 Kall Innovations, LLC
