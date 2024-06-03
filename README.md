
# 🐚 Minishell

In collaboration with @smclacke :heart:
Minishell is a simple shell program developed as part of the Codam curriculum. This project involves creating a functional shell that can execute commands, manage processes, handle environment variables, and implement various shell features. The project emphasizes understanding and implementing core concepts of operating systems, processes, and user interaction.

## 📑 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Usage](#usage)
- [Built-in Commands](#built-in-commands)
- [Installation](#installation)
- [Makefile](#makefile)
- [External Functions](#external-functions)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## 🌟 Overview

The Minishell project involves developing a simple command-line shell that mimics the behavior of the Bash shell. It includes features like command execution, input/output redirection, pipelines, signal handling, and built-in commands. The goal is to understand how a shell works and to gain experience with system-level programming in C.

## 🚀 Features

- **Prompt Display**: Displays a prompt when waiting for a new command.
- **Command History**: Maintains a history of executed commands.
- **Command Execution**: Searches and launches executables based on the `PATH` variable or using relative/absolute paths.
- **Signal Handling**: Handles signals with a single global variable for received signal indication.
- **Quote Handling**: Properly handles single (`'`) and double (`"`) quotes.
- **Redirections**:
  - `<` for input redirection.
  - `>` for output redirection.
  - `<<` for heredoc input until a delimiter is reached.
  - `>>` for output redirection in append mode.
- **Pipes**: Implements pipelines where the output of one command is the input to the next.
- **Environment Variables**: Expands environment variables (`$VAR`).
- **Special Variables**: Handles `$?` to expand to the exit status of the last executed command.
- **Interactive Mode**: Handles `ctrl-C`, `ctrl-D`, and `ctrl-\` with specific behaviors.

## 💻 Usage

Upon running Minishell, you'll be presented with a prompt where you can type commands similar to how you would in Bash. The shell supports:

- Executing binaries found in the `PATH`.
- Using relative or absolute paths for executables.
- Redirecting input and output.
- Creating pipelines with the `|` operator.
- Utilizing environment variables.
- Handling built-in commands directly.

## 📋 Built-in Commands

Minishell implements the following built-in commands:

- `echo` with option `-n`
- `cd` with a relative or absolute path
- `pwd` with no options
- `export` with no options
- `unset` with no options
- `env` with no options or arguments
- `exit` with no options
```

## 🛠️ Installation

To install and run Minishell, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/minishell.git
    cd minishell
    ```

2. Build the project using the provided Makefile:
    ```sh
    make
    ```

3. Run the shell:
    ```sh
    ./minishell
    ```

## 📄 Makefile

The Makefile for Minishell supports the following targets:

- **NAME**: Builds the Minishell executable.
- **all**: Builds the project.
- **clean**: Removes object files.
- **fclean**: Removes object files and the executable.
- **re**: Rebuilds the project.

## 📦 External Functions

Minishell utilizes the following external functions:

- `readline`, `rl_clear_history`, `rl_on_new_line`, `rl_replace_line`, `rl_redisplay`, `add_history`
- `printf`, `malloc`, `free`, `write`, `access`, `open`, `read`, `close`, `fork`, `wait`, `waitpid`, `wait3`, `wait4`
- `signal`, `sigaction`, `sigemptyset`, `sigaddset`, `kill`, `exit`
- `getcwd`, `chdir`, `stat`, `lstat`, `fstat`, `unlink`, `execve`, `dup`, `dup2`, `pipe`
- `opendir`, `readdir`, `closedir`
- `strerror`, `perror`, `isatty`, `ttyname`, `ttyslot`, `ioctl`
- `getenv`, `tcsetattr`, `tcgetattr`, `tgetent`, `tgetflag`, `tgetnum`, `tgetstr`, `tgoto`, `tputs`

## 📂 Project Structure

The project is organized into the following files:

- **Makefile**: Build configuration.
- **\*.h**: Header files.
- **\*.c**: Source files.

