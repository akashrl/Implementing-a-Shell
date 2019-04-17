# Implementing-a-Shell

To begin, a scanner and parser for the shell has been written using the open source versions of Lex and Yacc (Flex and Bison).  It is mostly written in C++.

The file command.h implements a data structure that represents a shell command. The struct SimpleCommand implements an argument list for a simple command (i.e. a command of the form mycmd arg1 arg2 arg3). When pipes are used, a command will be composed of multiple SimpleCommands. The struct Command represents a list of simple commands. Additionally, Command has fields which allow the user to specify files to use for input, output, and error redirection.

The various parts of the program:

1B.1: Simple command process creation and execution

1B.2: File redirection

1B.3: Pipes

1B.4: isatty()

Part 2: Signal Handling, More Parsing, and Subshells

In Part 2, you will begin to add features that make your shell more useful and fully featured.
2.1: Ctrl-C

2.2: Zombie Elimination

2.3: Exit

2.4: Quotes

2.5: Escaping

2.6: Builtin Functions

printenv
Prints the environment variables of the shell. The environment variables of a process are stored in the variable char **environ;, a null-terminated array of strings. Refer to the man page for environ.

setenv A B
Sets the environment variable A to value B.

unsetenv A
Un-sets environment variable A

source A
Runs file A line-by-line, as though it were being typed into the shell by a user. See Multiple Input Buffers

cd A
Changes the current directory to A. If no directory is specified, default to the home directory. See the man page for chdir().

2.7: Creating a Default Source File: “.shellrc”

2.8: Subshells

2.9: Process Substitution

Part 3: Expansions, Wildcards, and Line Editing
The final part of the lab involves adding a few major usability features to your shell. You will allow for your parser to expand a few types of input, handle wildcards, and implement a line editor that allows you to do things like fixing typos and traversing a history of previously submitted commands.

3.1: Environment variable expansion

3.2: Tilde expansion

3.3: Wildcarding

3.4: Edit mode

3.5: History

3.6: Path completion

3.7: Variable prompt



