# Minimal_OS
This is a minimal OS built with Assembly language. It can be scaled up and connected to main source `C`/`C++`, `Python` or `Bash`/`Zsh` files.
<hr />

## Pre-requesites for project

The project requires a `UNIX`-like environment. If you're on `Windows`, there're various ways of setting one up. You can use `WSL` (`Windows Subsystem for Linux`), a `Linux Virtual Machine`, `Cygwin` or `MSYS2`. But, I most-likely recommend you to setup `WSL` which is the easiest to setup among other techniques. [Read the documentation](https://learn.microsoft.com/en-us/windows/wsl/install). If you're on `macOS`, then it can be very easy to install the required packages by [`Homebrew'](https://formulae.brew.sh/).

For this project, you need to install the following tools and softwares below -

- `make`
- `nasm`
- `qemu-system-x86` for testing
- Your preferred source code editor (e.g., [`Visual Studio Code`](https://code.visualstudio.com), `NeoVim` or `Vim`)

## Tools installation

### For Linux based OSes
```
# Ubuntu, Debian:
sudo apt install make nasm qemu-system-x86 -y

# Fedora:
sudo dnf install make nasm qemu-system-x86 -y

# Arch & Arch-based:
paru -S make nasm qemu-system-x86

```
`NOTE` - To install all the required packages on `Arch Linux` or `Arch-based Linux distributions`, you need an [AUR Helper](https://wiki.archlinux.org/title/AUR_helpers).

### For macOS

```
brew install make nasm qemu-system-x86
```

## Guide on writing the code

You can either clone this repository or create your own by following the steps below.

- Create a source directory named whatever you want (e.g., "`src`" or "`kernel`").
- Then create a `build` directory (outside of the source directory).
- Navigate to the source directory and inside there, create a `Assembly language` file named "`main.asm`".
- Copy and paste the code from this repository to your "`main.asm`" file and save it.
- Outside of the source directory, create a file for building the `Assembly` runnable OS, must be named "`Makefile`".

## Building the OS Assembly code

- To `build` a `Floppy Image` and a `Binary` file, run the command in the terminal -

```
make
```

## Testing on a Virtual Machine

- To test your `OS` in a `Virtual Machine`, run -

```
qemu-system-i386 -fda build/main_floppy.img
```

## Output

After running `Qemu Virtual Emulator`, you can see similar screen like mine -

![assembly_os](https://github.com/devsujay19/Minimal_OS/assets/132755939/41f68490-2efd-4390-94cb-2e84357c0b9a)
