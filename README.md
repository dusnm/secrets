# Secrets

A bash script that aims to simplify the encryption and decryption of text messages using GPG

## Requirements
The script supports Linux and MacOS

General dependencies: `gpg`, `base64`

On MacOS you need to install the `coreutils` package
```shell
brew install coreutils
```

On Linux, `xorg-xclip` is required, install it with your distribution's package manager.

## Usage

Place the script in your `$PATH` and then invoke it with the following options:
```shell
Simplify the encryption and decryption of text messages with GPG

Copyright (C) 2023 <dusan@dusanmitrovic.xyz>
Licensed under the terms of the GNU GPLv3 or, at your option, any later version

Usage: secrets [OPTIONS] [ARGUMENT]

Options:
  -e [secret string] Whatever is passed to this option will be encrypted
  -i [file] Same as e, but uses a file as input instead
  -d [file] Decrypt a message encrypted by this utility
  -o Save the encrypted output as a file
  -c Copy the encrypted output to clipboard
  -h Print this help message
```

### Examples

#### Encrypt text from `stdin`
```shell
secrets -e "super secret message" -o
```

#### Encrypt text from file
```shell
secrets -i /path/to/text/file -o
```

### Decrypt a message
```shell
secrets -d /path/to/encrypted/file.gpg
```

## Licensing
This program is licensed under the terms of the GNU GPLv3 or, at your option, any later version.
