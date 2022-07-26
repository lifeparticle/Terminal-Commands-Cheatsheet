# 

```shell
# List all available shells in macOS X
cat /etc/shells

# To see which shell you’re running.
echo $0

echo $BASH_VERSION

echo $ZSH_VERSION

# To change to bash shell.
chsh -s /bin/bash

# To change to zsh shell.
chsh -s /bin/zsh
```

# Variables

## Bash

```shell
hw='Hello, World!'
echo "$hw"

# output of a command
first_line=$(head -1 version.txt)
echo "$first_line"
```

# String

## Bash

```shell
num='01234567'
echo "${num:0:3}"
# 012
```

```shell
hw='hello, world!'
echo "${hw^}"
# Hello, world!
echo "${hw^^}"
# HELLO, WORLD!

hw='Hello, World!'
echo "${hw,}"
# hello, World!
echo "${hw,,}"
# hello, world!
```

```shell
majorVersion=$(echo "1.2.3" | cut -d "." -f 1)
minorVersion=$(echo "1.2.3" | cut -d "." -f 2)
buildNumber=$(echo "1.2.3" | cut -d "." -f 3)

echo "${majorVersion} ${minorVersion} ${buildNumber}"
buildNumber=$(echo "$(($buildNumber + 1))")
echo "${majorVersion} ${minorVersion} ${buildNumber}"
newPackageVersion=$majorVersion.$minorVersion.$buildNumber
```

## Zsh
```shell
hw='hello, world!'
echo "${(U)hw}"
echo "${hw:u}"

hw='Hello, World!'
echo "${(L)hw}"
echo "${hw:l}"
# hello, world!
```


# Read

```shell
read name
echo "Hello, $name"  
```

# Last 100 commands

## Zsh

```shell
history -1 -100
```

# Resources
1. [17 Terminal Commands Every Programmer Should Know](https://medium.com/towards-data-science/17-terminal-commands-every-programmer-should-know-4fc4f4a5e20e)
