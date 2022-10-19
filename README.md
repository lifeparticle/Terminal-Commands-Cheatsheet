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

# Examples

```bash
echo \# 5. Number Generation        > Number\ Generation.md
echo \# 6. Fibonacci Series         > Fibonacci\ Series.md
echo \# 7. Combinatorics            > Combinatorics.md
echo \# 8. Dynamic Programming      > Dynamic\ Programming.md
echo \# 9. Greedy                   > Greedy.md
echo \# 10. Algorithm               > Algorithm.md
echo \# 11. Number Theory           > Number\ Theory.md
echo \# 12. Numerical Methods       > Numerical\ Methods.md
echo \# 13. Basics of Numbers       > Basics\ of\ Numbers.md
echo \# 14. Java                    > Java.md
echo \# 15. Computational Geometry  > Computational\ Geometry.md
echo \# 16. Math                    > Math.md
echo \# 17. Physics                 > Physics.md
echo \# 18. ASCII Table             > ASCII\ Table.md
```


```bash
for i in {15..50}; do
  mkdir "$i. "
done
```

```bash
declare -a array=("Number Generation" "Fibonacci Series" "Combinatorics" "Algorithm" "Number Theory" "Numerical Methods" "Basics of Numbers" "Java" "Computational Geometry" "Math" "Physics" "ASCII Table")

for ((i=1; i<${#array[@]}+1; ++i));
do
  echo "# $i. ${array[$i]}" > ${array[$i]}.md
done
```

# Resources
1. [17 Terminal Commands Every Programmer Should Know](https://medium.com/towards-data-science/17-terminal-commands-every-programmer-should-know-4fc4f4a5e20e)
