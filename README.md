# d/Python

**Python 3 for the browser, the desktop, and the 8-bit home computers d/OS runs on.**
You write ordinary Python 3; it compiles to one small program file that runs the
same way everywhere, with windows, buttons, sound, drag and drop and typed objects
as plain Python calls. No interpreter ships with your program.

- **Try it now:** https://dpython.kallinnovations.com/playground/
- **Guide, tutorials, what works today:** https://dpython.kallinnovations.com/
- **Downloads:** the [Releases](../../releases) page on this repository

This repository holds the downloadable releases only. The source is not published.

## Quick start

Download the kit for your machine from [Releases](../../releases), unpack it, and open a
terminal inside the folder. The folder is self-contained and can live anywhere; keep
`bin/dpython` and `bin/dbasic` together (`dpython` is the compiler and the runtime,
`dbasic` beside it is the window host).

**macOS** (the kit is not yet notarized; the first command clears the download flag):

```
xattr -dr com.apple.quarantine .
./bin/dpython run examples/hello.py
./bin/dpython run examples/tictactoe.py        # opens a window
```

**Linux** (the runtime links ALSA for sound):

```
sudo apt install libasound2t64                 # or libasound2 on older releases
./bin/dpython run examples/hello.py
```

**Windows** (PowerShell or Command Prompt):

```
.\bin\dpython.exe run examples\hello.py
```

Write `hello.py`, run it, compile it, run the compiled file:

```
./bin/dpython run hello.py                     # compile in memory and run
./bin/dpython build hello.py -o out/hello.dbc  # compile; writes out/hello.dbc and out/lib/*.dbl
./bin/dpython run out/hello.dbc                # run the compiled program
./bin/dpython check hello.py                   # compile and validate only
./bin/dpython inspect hello.py                 # sizes, capabilities, libraries (JSON)
./bin/dpython package app.py --metadata app.json -o app.dapp
```

What works where in this release: macOS has console programs, `input()`, native
windows and widgets, copy/paste, drag and drop, files, sound and network; Linux has
console programs, `input()`, files, sound and network (window host to come); Windows has
console programs, files and network (`input()` and the window host to come). Each kit's
README says the same and its `manifest.json` records what was checked.

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
