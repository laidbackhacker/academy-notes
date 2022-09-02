---
title: "Powershell"
---
Themes: [[Windows]], 

# What is PowerShell?
- A task automation and configuration framework
- Consists of the command-line shell and a scripting language
- Open source
- Very useful for automating tasks with scripts

## Commands
- Compatible with a lot of BASH commands
- `clear` to clear the terminal
- `help` or `get-help` to get help on a command
- `-online` to find the online documentation
- `get-command *X*` returns any commands containing `X`
- `Get-Member` returns an object's underlying structure including its methods and properties

## Programming in PowerShell
- use `snake_case` instead of `camelCase` because PowerShell isn't case sensitive
- `#` comment
- `<# #>` multiline comments
- `$` before a word for a variable

- `read-host` get an input
- `write-host` print a line

### Data types
- You don't need to declare a variables type, same as python
- `$var = 21` integer
- `$var = "21` string
![Pasted image 20220708111748.png](images/Pasted%20image%2020220708111748.png)
### Operators
![Pasted image 20220708113925.png](images/Pasted%20image%2020220708113925.png)
![Pasted image 20220708114009.png](images/Pasted%20image%2020220708114009.png)
![Pasted image 20220708114106.png](images/Pasted%20image%2020220708114106.png)


# Exercise 2
- `Get-ChildItem -Path * -Include *.exe | Where-Object {$_.length -gt 30000}` returns all exe files in the directory that are greater than 30kilobytes

