# j
Jump to commonly used directories

## Installation

```bash
$ stack install
```

And then add the following code to your .bashrc/.zshrc, etc, depending on your shell

### Zsh or Bash

```bash
j () {
	eval `.j $@`
}
```

### Others

TODO

## Usage

### List all jumpers

```bash
~ $ j
lab -> ~/Lab
p -> ~/Lab/personal
n -> ~/Lab/Netis
t -> ~/Lab/tospio
c -> ~/Chest
~ $ 
```

### Jump

```bash
~ $ j p
~/Lab/personal $ 
```

### Add a jumper (or overwrite an existing one)

```bash
~/Lab/personal $ j -s log /var/log
~/Lab/personal $ j log
/var/log $ 
```

### Delete a jumper

```bash
~ $ j -u log
~ $ j log
No such jumper: log
~ $ 
```

### Print a jumper destination

Might be useful as a quoted expression

```bash
~ $ j -p c
~/Chest
~ $ 
```

## Notes

The jumpers are saved as `~/.j`. It's a simple csv file of k/v pairs. You can easily modify it with your favorite editor as you wish.
