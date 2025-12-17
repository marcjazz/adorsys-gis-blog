# UCC121-3: AI In Administrative Tasks

## Course Information Sheet
- **Title:** AI In Administrative Tasks
- **Code:** UCC121-3
- **Prerequisites:** **UCC121-1**. Solid shell scripting skills.
- **Duration:** 12 hours (8 sessions of 1.5 hours each).
- **Objectives:**
    - Use AI assistants to accelerate problem-solving and code generation.
    - Apply AI to concrete use cases: log analysis, security, monitoring.
    - Understand the principles of "prompt engineering" adapted to system tasks.
- **Assessment:** Continuous assessment (Practical Labs), project, final exam.

## 8-Session Breakdown

### Session 1: Introduction to AI for System Administration
- **Lesson:** What is an LLM? Overview of AI tools for the CLI. Potential, limitations, and ethical considerations.
- **Lab/Assessment:** Installation and configuration of a tool (e.g., GitHub Copilot for CLI). First simple prompts.

### Session 2: Command Generation and Explanation
- **Lesson:** The art of "prompting": how to translate a need into an effective AI query. Use cases: "explain this command," "find the command for...".
- **Lab/Assessment:** Series of challenges to be solved using AI to find and understand complex commands (`find`, `rsync`, `iptables`).

### Session 3: AI-Assisted Script Generation
- **Lesson:** From a simple command to a complete script. How to specify the logic, error handling, and desired output format to the AI.
- **Lab/Assessment:** Generate a script that automates the creation of new users (with input validation).

### Session 4: Iterative Code Refinement and Debugging with AI
- **Lesson:** Using AI as a "pair programming" partner. Submitting an existing script to improve, refactor, or debug it.
- **Lab/Assessment:** Take a simple script and ask the AI to add logging, better error handling, and comments.

### Session 5: AI-Augmented Log Analysis
- **Lesson:** Strategies for analyzing large volumes of logs. Prompts for anomaly detection, activity summarization, and event correlation.
- **Lab/Assessment:** Analyze an `auth.log` to produce a security report (brute-force attempts, successful logins by user).

### Session 6: AI for Configuration and Security
- **Lesson:** Generate configuration files (Nginx, Apache, SSH). Audit an existing configuration with AI to identify potential security vulnerabilities.
- **Lab/Assessment:** Generate a secure Nginx configuration for a static website. Ask the AI to analyze `sshd_config` and suggest improvements.

### Session 7: Concepts of Predictive Monitoring
- **Lesson:** Introduction to AIOps. How AI can analyze metrics (CPU, RAM) to anticipate problems. Designing intelligent alerts.
- **Lab/Assessment:** Use AI to write the metric collection script. Discuss data analysis strategies for this data with the AI.

### Session 8: Synthesis Project and Future of AI
- **Lesson:** Reflection on the evolution of the system administrator profession.
- **Lab/Assessment:** Workshop dedicated to a final project combining scripting and AI (e.g., an intelligent system diagnostic tool) and presentation of results.
# Detailed Course Plan: UCC121-1

This document outlines the course plan for the "Shells, Scripting, and Data Management" module.

---

# UCC121-1: Shells, Scripting, and Data Management

## Course Information Sheet
- **Title:** Shells, Scripting, and Data Management
- **Code:** UCC121-1
- **Prerequisites:** Basic proficiency with the Linux command line (UCC111 or equivalent).
- **Duration:** 12 hours (8 sessions of 1.5 hours each).
- **Objectives:**
    - Master advanced command-line tools.
    - Create robust and modular shell scripts for automation.
    - Manipulate text data and interact with a simple database.
- **Assessment:** Continuous assessment (Practical Labs), scripting project, final exam.

## 8-Session Breakdown

### Session 1: Mastering the Shell Environment
- **Lesson:** Fundamentals of the Bash shell, customizing `.bashrc`, managing aliases, functions, and environment variables (`PATH`, `PS1`).
- **Lab/Assessment:** Create useful aliases, write a function to automate a simple task (e.g., `mkcd`), and customize the command prompt.

### Session 2: Text Processing Tools: `grep`, `sed`, `awk`
- **Lesson:** Introduction to regular expressions. Using `grep` for searching, `sed` for substitution, and `awk` for column extraction.
- **Lab/Assessment:** Extract all IP addresses from a log file. Replace a string in a series of configuration files.

### Session 3: Bash Scripting Fundamentals
- **Lesson:** Anatomy of a script (shebang, permissions), variables, reading user input (`read`), handling parameters (`$1`, `$@`), command substitution `$(...)`.
- **Lab/Assessment:** Write a script that takes a filename as a parameter and displays its first 3 lines.

### Session 4: Logic and Control Structures
- **Lesson:** `if/elif/else` conditions, file and string tests `[[ ... ]]`. The `case` statement. Handling exit codes (`$?`).
- **Lab/Assessment:** Write a script that checks if a user exists in `/etc/passwd`.

### Session 5: Loops and Iteration
- **Lesson:** `for` loops (over lists, sequences, files), `while` loops (to read a file line-by-line), and `until` loops.
- **Lab/Assessment:** Write a script that bulk renames all `.jpeg` files in a folder to `.jpg`.

### Session 6: Functions and Modularity
- **Lesson:** Declaring and calling functions, variable scope (local/global), passing arguments, and returning values. Sourcing function files.
- **Lab/Assessment:** Transform a monolithic script into a modular script using functions.

### Session 7: Introduction to Data Management with SQL
- **Lesson:** Principles of relational databases. Using `sqlite3` for `CREATE TABLE`, `INSERT`, `SELECT`, `UPDATE`, `DELETE`.
- **Lab/Assessment:** Create a simple inventory database and write a shell script to query it.

### Session 8: Process Management and Automation with `cron`
- **Lesson:** Managing background jobs (`&`, `jobs`, `fg`, `bg`, `nohup`). Scheduling tasks with `cron`.
- **Lab/Assessment:** Launch a script as a background task. Schedule a backup script to run every night.

---

# Glossary of Terms

- **`awk`**: A powerful command-line tool for processing and analyzing column-based text data.
- **`alias`**: A custom shortcut for a longer command. Defined in shell configuration files.
- **`Bash` (Bourne Again SHell)**: The default command-line interpreter on most Linux systems.
- **`.bashrc`**: A script file that is executed every time a new interactive shell is started. Used for personal customizations.
- **`cron`**: A time-based job scheduler in Unix-like operating systems. Used to automate repetitive tasks.
- **`crontab`**: The file or command used to specify the schedule of cron jobs.
- **Environment Variable**: A dynamic named value that can affect the way running processes will behave on a computer. `PATH` and `HOME` are examples.
- **`grep`**: A command-line utility for searching plain-text data sets for lines that match a regular expression.
- **`function`**: A reusable block of code that is more powerful than an alias and can accept arguments.
- **`PATH`**: An environment variable specifying the set of directories where executable programs are located.
- **`PS1`**: The primary prompt string environment variable, which controls the appearance of the command prompt.
- **Regular Expression (Regex)**: A sequence of characters that specifies a search pattern in text.
- **`sed`**: A "stream editor" utility for parsing and transforming text.
- **`Shebang` (`#!`)**: The first two characters of a script, which tell the system what interpreter to use to run it (e.g., `#!/bin/bash`).
- **`Shell`**: A user interface for access to an operating system's services. In this context, a command-line interface (CLI).
- **`SQL` (Structured Query Language)**: A standard language for managing and manipulating data in relational databases.
- **`sqlite3`**: A command-line interface to a self-contained, serverless, zero-configuration, transactional SQL database engine.
# UCC121-1, Session 1: Course Content
## Topic: Mastering the Shell Environment

---

### 1. What is a Shell?

A **shell** is a program that provides the user with a direct interface to the operating system. It takes your commands, interprets them, and asks the operating system to perform the requested action.

- **Interface:** It's a Command-Line Interface (CLI).
- **Role:** Sits between you (the user) and the operating system's core (the **kernel**).
- **Default Shell:** On most Linux systems, the default shell is `bash` (the **B**ourne **A**gain **SH**ell).

You can find out what shell you are using with the command: `echo $SHELL`

### 2. The `.bashrc` File: Your Personal Toolbox

When you start an interactive shell, it automatically runs a script to set up your environment. This script is `.bashrc` (located in your home directory, `~/.bashrc`).

- **Purpose:** To store all your personal customizations: aliases, functions, and environment variables.
- **Activation:** Changes made to `.bashrc` are not applied automatically to your current session. You must load them by either:
    1.  Starting a new shell session.
    2.  Running the command `source ~/.bashrc`.

### 3. Aliases: Your Command-Line Shortcuts

An alias is a simple way to create a shortcut for a longer command. They are perfect for commands you use often.

**Syntax:** `alias shortcut_name='the_long_command'`

**Common & Useful Examples:**

```bash
# Make 'ls' more informative and colorful
alias ls='ls --color=auto'
alias ll='ls -alF'
alias la='ls -A'
alias l='ls -CF'

# Shortcuts for system updates (Debian/Ubuntu)
alias update='sudo apt update && sudo apt upgrade'

# Show open ports
alias ports='netstat -tulpn'
```

**How to add them:** Open `~/.bashrc` with a text editor (like `nano` or `vim`) and add these lines. Then run `source ~/.bashrc`.

**Removing an alias:** `unalias shortcut_name`

### 4. Functions: Super-Powered Aliases

Functions are like aliases, but they are more powerful. They can accept arguments (parameters), contain multiple commands, and use logic.

**Syntax:**
```bash
function_name() {
  # command 1
  # command 2
  # use $1, $2 for arguments
}
```

**Example: The `mkcd` function**

A common task is to create a directory and then immediately navigate into it.
- **Problem:** `mkdir new_dir` followed by `cd new_dir`.
- **Solution:** A function that does both!

```bash
# Creates a directory and changes into it
mkcd() {
  mkdir -p "$1" && cd "$1"
}
```

- `mkdir -p "$1"`: Creates the directory. `-p` ensures it doesn't fail if the directory exists and also creates parent directories if needed. `"$1"` is the first argument you provide to the function.
- `&&`: This is a logical AND. The `cd "$1"` command only runs if the `mkdir` command was successful.

### 5. Environment Variables: The Shell's Memory

Environment variables are dynamic values that affect the processes and programs running in the shell. By convention, their names are in uppercase.

**Key Variables to Know:**

#### `PATH`
- **What it is:** A colon-separated list of directories that the shell searches through when you type a command.
- **How it works:** When you type `ls`, the shell looks for an executable file named `ls` in each directory listed in `$PATH`.
- **View it:** `echo $PATH`
- **Modify it:** To add a custom scripts folder (e.g., `~/bin`) to your PATH, you would add this to `.bashrc`:
  `export PATH="$HOME/bin:$PATH"
  This tells the shell to look in `~/bin` first, then in all the other standard locations.

#### `PS1`
- **What it is:** The Primary Prompt String. This variable controls what your command prompt looks like.
- **Customization:** You can use special backslash-escaped characters to insert dynamic information.
- **View it:** `echo $PS1`
- **Common `PS1` codes:**
    - `\u`: Username
    - `\h`: Hostname (the computer's name)
    - `\w`: The current working directory
    - `\t`: The current time (HH:MM:SS)
    - `\$`: Displays a `#` if you are the root user, `$` otherwise.

**Example `PS1` Customization:**

```bash
# A prompt showing user@host:directory
export PS1='[\u@\h \w]\$ '

# A prompt with colors (this can look complex!)
export PS1='[\033[01;32m\]\u@\h[\033[00m]:[\033[01;34m\]\w[\033[00m]\$ '
```

### 6. Lab Exercises (TP/CC)

1.  **Open `~/.bashrc`:** Use a text editor like `nano ~/.bashrc`.
2.  **Add Aliases:** Add the `ll` and `update` aliases shown in the examples above.
3.  **Add a Function:** Add the `mkcd` function.
4.  **Customize your Prompt:** Add the colored `PS1` export line from the example.
5.  **Activate Changes:** Save the file and run `source ~/.bashrc`.
6.  **Test Everything:**
    - Type `ll`. Does it show a detailed file listing?
    - Type `type update`. Does it show that `update` is an alias?
    - Use your new `mkcd` function: `mkcd test_directory`. Did it create the folder and move you inside it?
    - Does your prompt look different and colorful?
# UCC121-1: Shells, Scripting, and Data Management
## Session 1: Mastering the Shell Environment

---

## What is a Shell?

A program that takes your commands and tells the operating system what to do.

**You -> Shell -> OS Kernel -> Hardware**

It is your primary interface for controlling the system. We will be using **Bash** (Bourne Again SHell).

---

## Your Toolbox: `~/.bashrc`

An essential configuration file in your home directory.

- **Purpose:** Stores your personal customizations.
- **Execution:** Runs automatically every time you open a new terminal.
- **Rule:** After editing, you must run `source ~/.bashrc` to apply changes to your current session.

---

## Aliases: Your Command-Line Shortcuts

Create short, memorable names for long, complex commands.

**Syntax:** `alias name='long_command'`

```bash
# Example
alias ll='ls -alF'
```

---

## Useful Alias Examples

```bash
# For detailed, human-readable file listing
alias ll='ls -alFh'

# For system updates (Debian/Ubuntu)
alias update='sudo apt update && sudo apt upgrade'

# To quickly show all active network ports
alias ports='netstat -tulpn'
```

---

## Functions: Super-Powered Aliases

For when an alias is not enough.

- Can contain multiple commands.
- Can accept arguments (`$1`, `$2`, etc.).
- Can include logic.

**Syntax:**
```bash
function_name() {
  commands
}
```

---

## Function Example: `mkcd`

A common workflow: create a directory, then `cd` into it.

```bash
# Add this to your ~/.bashrc
mkcd() {
  mkdir -p "$1" && cd "$1"
}
```
**Usage:** `mkcd my_new_project`

---

## Environment Variables

Dynamic, named values that programs use to configure their behavior.

- Conventionally named in `UPPERCASE`.
- View any variable with `echo $VARIABLE_NAME`.
- Set them with `export VARIABLE_NAME="value"`.

---

## The `PATH` Variable

How does the shell find commands like `ls` or `grep`? It searches the `PATH`.

- `$PATH` is a colon-separated list of directories.
- `echo $PATH`
- To add your own script directory (e.g., `~/bin`):
  `export PATH="$HOME/bin:$PATH"`
  *(Add this to `~/.bashrc`)*

---

## The `PS1` Variable: Your Prompt

This variable controls what your command prompt looks like.

**Special Characters:**
- `\u` : Username
- `\h` : Hostname
- `\w` : Current Directory
- `\$` : `$` for normal users, `#` for root.

**Example:** `export PS1='[\u@\h \w]\$ '`
**Result:** `[user@hostname ~]$`

---

## Lab Time!

1.  Open `~/.bashrc` with a text editor.
2.  Add the `ll` alias.
3.  Add the `mkcd` function.
4.  Add a custom `PS1` variable to make your prompt colorful.
    - `export PS1='[\033[01;32m\]\u@\h[\033[00m]:[\033[01;34m\]\w[\033[00m]\$ '`
5.  Run `source ~/.bashrc`.
6.  Test that your alias, function, and new prompt all work correctly.

---

## Questions?

**Next Session:** Text Processing Tools: `grep`, `sed`, and `awk`
\n## Scripting Session 1\n
# UCC121-1, Session 1: Course Content
## Topic: Mastering the Shell Environment

---

### 1. What is a Shell?

A **shell** is a program that provides the user with a direct interface to the operating system. It takes your commands, interprets them, and asks the operating system to perform the requested action.

- **Interface:** It's a Command-Line Interface (CLI).
- **Role:** Sits between you (the user) and the operating system's core (the **kernel**).
- **Default Shell:** On most Linux systems, the default shell is `bash` (the **B**ourne **A**gain **SH**ell).

You can find out what shell you are using with the command: `echo $SHELL`

### 2. The `.bashrc` File: Your Personal Toolbox

When you start an interactive shell, it automatically runs a script to set up your environment. This script is `.bashrc` (located in your home directory, `~/.bashrc`).

- **Purpose:** To store all your personal customizations: aliases, functions, and environment variables.
- **Activation:** Changes made to `.bashrc` are not applied automatically to your current session. You must load them by either:
    1.  Starting a new shell session.
    2.  Running the command `source ~/.bashrc`.

### 3. Aliases: Your Command-Line Shortcuts

An alias is a simple way to create a shortcut for a longer command. They are perfect for commands you use often.

**Syntax:** `alias shortcut_name='the_long_command'`

**Common & Useful Examples:**

```bash
# Make 'ls' more informative and colorful
alias ls='ls --color=auto'
alias ll='ls -alF'
alias la='ls -A'
alias l='ls -CF'

# Shortcuts for system updates (Debian/Ubuntu)
alias update='sudo apt update && sudo apt upgrade'

# Show open ports
alias ports='netstat -tulpn'
```

**How to add them:** Open `~/.bashrc` with a text editor (like `nano` or `vim`) and add these lines. Then run `source ~/.bashrc`.

**Removing an alias:** `unalias shortcut_name`

### 4. Functions: Super-Powered Aliases

Functions are like aliases, but they are more powerful. They can accept arguments (parameters), contain multiple commands, and use logic.

**Syntax:**
```bash
function_name() {
  # command 1
  # command 2
  # use $1, $2 for arguments
}
```

**Example: The `mkcd` function**

A common task is to create a directory and then immediately navigate into it.
- **Problem:** `mkdir new_dir` followed by `cd new_dir`.
- **Solution:** A function that does both!

```bash
# Creates a directory and changes into it
mkcd() {
  mkdir -p "$1" && cd "$1"
}
```

- `mkdir -p "$1"`: Creates the directory. `-p` ensures it doesn't fail if the directory exists and also creates parent directories if needed. `"$1"` is the first argument you provide to the function.
- `&&`: This is a logical AND. The `cd "$1"` command only runs if the `mkdir` command was successful.

### 5. Environment Variables: The Shell's Memory

Environment variables are dynamic values that affect the processes and programs running in the shell. By convention, their names are in uppercase.

**Key Variables to Know:**

#### `PATH`
- **What it is:** A colon-separated list of directories that the shell searches through when you type a command.
- **How it works:** When you type `ls`, the shell looks for an executable file named `ls` in each directory listed in `$PATH`.
- **View it:** `echo $PATH`
- **Modify it:** To add a custom scripts folder (e.g., `~/bin`) to your PATH, you would add this to `.bashrc`:
  `export PATH="$HOME/bin:$PATH"
  This tells the shell to look in `~/bin` first, then in all the other standard locations.

#### `PS1`
- **What it is:** The Primary Prompt String. This variable controls what your command prompt looks like.
- **Customization:** You can use special backslash-escaped characters to insert dynamic information.
- **View it:** `echo $PS1`
- **Common `PS1` codes:**
    - `\u`: Username
    - `\h`: Hostname (the computer's name)
    - `\w`: The current working directory
    - `\t`: The current time (HH:MM:SS)
    - `\$`: Displays a `#` if you are the root user, `$` otherwise.

**Example `PS1` Customization:**

```bash
# A prompt showing user@host:directory
export PS1='[\u@\h \w]\$ '

# A prompt with colors (this can look complex!)
export PS1='[\033[01;32m\]\u@\h[\033[00m]:[\033[01;34m\]\w[\033[00m]\$ '
```

### 6. Lab Exercises (TP/CC)

1.  **Open `~/.bashrc`:** Use a text editor like `nano ~/.bashrc`.
2.  **Add Aliases:** Add the `ll` and `update` aliases shown in the examples above.
3.  **Add a Function:** Add the `mkcd` function.
4.  **Customize your Prompt:** Add the colored `PS1` export line from the example.
5.  **Activate Changes:** Save the file and run `source ~/.bashrc`.
6.  **Test Everything:**
    - Type `ll`. Does it show a detailed file listing?
    - Type `type update`. Does it show that `update` is an alias?
    - Use your new `mkcd` function: `mkcd test_directory`. Did it create the folder and move you inside it?
    - Does your prompt look different and colorful?
# UCC121-1: Shells, Scripting, and Data Management
## Session 1: Mastering the Shell Environment

---

## What is a Shell?

A program that takes your commands and tells the operating system what to do.

**You -> Shell -> OS Kernel -> Hardware**

It is your primary interface for controlling the system. We will be using **Bash** (Bourne Again SHell).

---

## Your Toolbox: `~/.bashrc`

An essential configuration file in your home directory.

- **Purpose:** Stores your personal customizations.
- **Execution:** Runs automatically every time you open a new terminal.
- **Rule:** After editing, you must run `source ~/.bashrc` to apply changes to your current session.

---

## Aliases: Your Command-Line Shortcuts

Create short, memorable names for long, complex commands.

**Syntax:** `alias name='long_command'`

```bash
# Example
alias ll='ls -alF'
```

---

## Useful Alias Examples

```bash
# For detailed, human-readable file listing
alias ll='ls -alFh'

# For system updates (Debian/Ubuntu)
alias update='sudo apt update && sudo apt upgrade'

# To quickly show all active network ports
alias ports='netstat -tulpn'
```

---

## Functions: Super-Powered Aliases

For when an alias is not enough.

- Can contain multiple commands.
- Can accept arguments (`$1`, `$2`, etc.).
- Can include logic.

**Syntax:**
```bash
function_name() {
  commands
}
```

---

## Function Example: `mkcd`

A common workflow: create a directory, then `cd` into it.

```bash
# Add this to your ~/.bashrc
mkcd() {
  mkdir -p "$1" && cd "$1"
}
```
**Usage:** `mkcd my_new_project`

---

## Environment Variables

Dynamic, named values that programs use to configure their behavior.

- Conventionally named in `UPPERCASE`.
- View any variable with `echo $VARIABLE_NAME`.
- Set them with `export VARIABLE_NAME="value"`.

---

## The `PATH` Variable

How does the shell find commands like `ls` or `grep`? It searches the `PATH`.

- `$PATH` is a colon-separated list of directories.
- `echo $PATH`
- To add your own script directory (e.g., `~/bin`):
  `export PATH="$HOME/bin:$PATH"`
  *(Add this to `~/.bashrc`)*

---

## The `PS1` Variable: Your Prompt

This variable controls what your command prompt looks like.

**Special Characters:**
- `\u` : Username
- `\h` : Hostname
- `\w` : Current Directory
- `\$` : `$` for normal users, `#` for root.

**Example:** `export PS1='[\u@\h \w]\$ '`
**Result:** `[user@hostname ~]$`

---

## Lab Time!

1.  Open `~/.bashrc` with a text editor.
2.  Add the `ll` alias.
3.  Add the `mkcd` function.
4.  Add a custom `PS1` variable to make your prompt colorful.
    - `export PS1='[\033[01;32m\]\u@\h[\033[00m]:[\033[01;34m\]\w[\033[00m]\$ '`
5.  Run `source ~/.bashrc`.
6.  Test that your alias, function, and new prompt all work correctly.

---

## Questions?

**Next Session:** Text Processing Tools: `grep`, `sed`, and `awk`
