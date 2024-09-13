# Unshell
Unshell is an absolute script kiddies nighmare that deobfuscate some popular shell script obfuscation easily.

## Supported obfuscation method
- Shell Script Compiler (SHC)
- Simple Script Compiler (SSC)
- Bashrock
- BashProtector
- bash-obfuscate (Node.js CLI)
- base64

## Usage
```shell
# Installation
spath=$(echo $PATH | cut -d: -f1) && cp ./unshell $spath && chmod +x $spath/unshell

# Deobfuscate!
unshell encrypted1 encrypted2 # multi file input ins supported
```

## Special Credits
[kawaii-ghost](https://github.com/kawaii-ghost/deshc) for decsh (shc and ssc deobfucator).
[RiProG-id](https://github.com/RiProG-id/Universal-Shell-Dec.git) for universal-shell-dec, the inspiration and foundation of this project.
