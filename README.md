# Assignment_1_BSDSF22A027
<UNIX Shell Assignment>
<Project Description>
This project is a custom UNIX shell developed to provide experience with UNIX system calls, process management, and command-line interpreters. It replicates core functionalities of standard UNIX shells, allowing users to execute commands with various features like I/O redirection, background processing, command history, and built-in commands.

<Features by Version>
<Version 01:> Basic Shell Functionality
<Prompt:> Displays a prompt (e.g., PUCITshell:/home/user/-).
<Command Execution:> Parses and executes commands entered by the user.
<Exit:> Supports shell termination with <CTRL+D>.
<Implementation:> Tokenizes input commands, forks a new process, and executes using exec functions.

<Version 02: I/O Redirection and Piping>
<Input/Output Redirection:> Allows redirecting standard input and output using < and >.
<Example:> mycmd < infile > outfile.
<Piping:> Supports chaining commands with pipes (e.g., cat /etc/passwd | wc).
<Implementation:> Uses dup2 for file descriptor redirection.

<Version 03: Background Execution>
<Background Processes:> Allows running commands in the background by appending &.
<Example>: find / -name f1.txt &
<Implementation:> The prompt immediately returns, and the process runs in the background.

<Version 04: Command History>
<Command History:> Maintains the last 10 commands and allows re-execution with !number.
<Example:> !-1 repeats the last command.
<giImplementation:> Stores commands in a history list, accessible through the shell.

<Version 05: Built-in Commands>
<Built-in Commands:>
<cd:> Changes the current working directory.
<exit:> Exits the shell.
<jobs:> Lists background processes.
<kill:> Terminates a specified background process.
<help:> Lists available built-in commands and their syntax.
<Implementation:> Built-in commands are implemented directly in the shell without forking.

<Version 06 (BONUS): Variable Management>
<User-Defined and Environment Variables:> Supports setting and retrieving variable values.
<Implementation:> Stores variables in a structure and distinguishes between local and environment variables.