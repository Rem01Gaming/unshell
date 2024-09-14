![unshell_hero](./unshell-banner.png)
# Unshell
> The Script Kiddies Nighmare

Effortlessly deobfuscate shell scripts back into source code even with heavenly and multi layered obfuscation.

## Features
- Zero configuration: There's no need for any configuration
- Penetrate: Multiple layered obfuscation is not a problem
- Easy to use: just `unshell encrypted1 encrypted2` in cmd

## Supported obfuscation method
<details>
<summary>Shell Script Compiler (SHC)</summary>
SHC works internally called execve to shell, it decrypted at runtimes and visible via command line args process

eg: `/bin/sh -c "decrypted shell"`
</details>

<details>
<summary>Simple Script Compiler (SSC)</summary>
It works almost the same as SHC but this one uses C++ and shell reads from file descriptor `3`. It visible via `fd` number 3 on the process.
</details>

<details>
<summary>bash-obfuscate (Node.js CLI)</summary>
bash-obfuscate works by randomize the script with random variables then execute it in `eval` command.
</details>

<details>
<summary>Bashrock</summary>
Bashrock works almost the same way as bash-obfuscate.
</details>

<details>
<summary>BashProtector</summary>
Bashrock randomize the script with random variables layered by single `base64` encryption, then execute it in single `eval` command.
</details>

<details>
<summary>base64</summary>
Not too crazy, just classic `echo "c29tZSBiYXNlNjQgZW5jcnlwdGVkIHNoaXQK" | base64 -d | sh`.
</details>

## Usage
```shell
# Installation
spath=$(echo $PATH | cut -d: -f1) && curl -sLo $spath/unshell https://github.com/Rem01Gaming/unshell/raw/main/unshell && chmod +x $spath/unshell

# Deobfuscate!
unshell encrypted1 encrypted2 # multi file input ins supported
```

## Special Credits
- [kawaii-ghost](https://github.com/kawaii-ghost/deshc) for decsh (shc and ssc deobfucator).
- [RiProG-id](https://github.com/RiProG-id/Universal-Shell-Dec.git) for universal-shell-dec, the inspiration and foundation of this project.
