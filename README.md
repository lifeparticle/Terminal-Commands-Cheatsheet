# Variables

```shell
hw='Hello, World!'
echo "$hw"

# output of a command
first_line=$(head -1 version.txt)
echo "$first_line"
```

# String

```shell
num='01234567'
echo "${num:0:3}"
# 012
```

```shell
hw='hello, world!'
echo "${hw^}"
# 012
echo "${hw^^}"
# 012

hw='Hello, World!'
echo "${hw^}"
# 012
echo "${hw^^}"
# 012
```

```shell
# Zsh
hw='hello, world!'
echo "${(U)hw}"

hw='Hello, World!'
echo "${(L)hw}"
# hello, world!
```



# Read

```shell
read name
echo "Hello, $name"  
```


# Resources
1. [17 Terminal Commands Every Programmer Should Know](https://medium.com/towards-data-science/17-terminal-commands-every-programmer-should-know-4fc4f4a5e20e)
