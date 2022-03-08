###	Shell, init files, variables and expansions 

In this folder we are going to put down all that there is to know about the followin:

- The general understanding of this command => ls -l *.txt
	- The **ls** command helps us to list all the files and directories in our current directories.
	- The **-l** option signifies the long list format, which gives more information eg. the number of links, owner's name, file size, time of last modification etc.
	- The '*' is a wildcard expansion. It is a special character that expands to match any character or multiple characters before the command is run. Its position in the argument is important.
	- All together, **ls -l *.txt** since '*' comes before ‘.txt’, that means the bash will expand the `*` to match all filenames, and then match only those filenames that end in ‘.txt’.

- Shell initialization files
	- A shell initialization file is a shell script that runs automatically each time the shell executes. The initialization file sets up the “work environment” and “customizes” the shell environment for the user. 
	- Shell modes => Before understanding shell initialization files, first understand shell initialization files are dependent on the “combination of shell modes” in which a particular shell process runs. The shell can be run in three possible modes:
	- Interactive login 
	- Interactive non-login 
	- Non-interactive 
	Two types of SIF
	- System-wide startup files
	These are the initialization files that contain configurations that applied to the whole system irrespective of a specific user, which means all users can share the same configuration which applied in system-wide startup files. System-wide startup files are:

	The /etc/profile file – It stores system-wide environment configurations and startup programs for login setup. All configurations that you want to apply to all system users’ environments should be added in this file.
	The /etc/bashrc or /etc/bash.bashrc file – It contains system-wide functions and aliases including other configurations that apply to all system users.

	- User-specific startup files
	These are the initialization files which contain configuration which applied to the specific user, means all users can have their own configuration which applied in user-specific startup files. User-specific startup files are located in home directory of the user and files are .profile, .bash_profile, .bashrc and .bash_login.

~/.bash_profile file – Stores user-specific environment and startup programs configurations. 
~/.bashrc file – Stores user-specific aliases and functions.
~/.bash_login file – Contains specific configurations that are normally only executed when you log in to the system. When the ~/.bash_profile is absent, this file will be read by bash.
~/.profile file – It is read in the absence of ~/.bash_profile and     ~/.bash_login; it can store the same configurations, which are can also be accessible by other shells on the system. Because we have mainly talked about bash here, take note that other shells might not understand the bash syntax.
~/.bash_history file – Bash maintains a history of commands that have been entered by a user on the system. This list of commands is kept in a user’s home directory in the ~/.bash_history file.
~/.bash_logout file – it’s not used for shell startup, but stores user specific instructions for the logout procedure. It is read and executed when a user exits from an interactive login shell.


- Variables
	- A variable is a character string to which we assign a value. The value assigned could be a number, text, filename, device, or any other type of data.
	- A variable is nothing more than a pointer to the actual data. The shell enables you to create, assign, and delete variables.
	- The name of a variable can contain only letters (a to z or A to Z), numbers ( 0 to 9) or the underscore character ( _). By convention, Unix shell variables will have their names in UPPERCASE.
	- Variables are defined as variable_name = variable_value
	 **Types of variables**
	 - **Local Variables** − A local variable is a variable that is present within the current instance of the shell. It is not available to programs that are started by the shell. They are set at the command prompt.
	 - **Environment Variables** − An environment variable is available to any child process of the shell. Some programs need environment variables in order to function correctly. Usually, a shell script defines only those environment variables that are needed by the programs that it runs.
	 - **Shell Variables** − A shell variable is a special variable that is set by the shell and is required by the shell in order to function correctly. Some of these variables are environment variables whereas others are local variables.

- Expansions 
	- When a command is entered in the command line, it expands into its output which is displayed. This is called expansion. The command you're typing will be printed with the help of echo command on the terminal. This command will be useful when you want to check what your command is doing in the shell.
- Shell Arithmetic
- **alias** command
