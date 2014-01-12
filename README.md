shell-prompt
============

Shell prompt for bash.

Bash Shell Prompt
-----------------

Define functions can be used to bash shell prompt (e.g. PS1).

Current two functions are defined:

    # Get the virtualenv name, if available.
    __virtualenv_name()

This function can used to detect python `virtualenv` name. It will give the base name of virtualenv. For example the
virtualenv path is `~/myenvs/django`, it will produce `django`


    # Get the git head name, if available.
    __git_head()

This function can used to detect git's head name, if current directory is in a git repo.

How to use it:

    . /path/to/.bash_prompt

You can even customize it, e.g.

    . /path/to/.bash_prompt
    PS1="\$(__virtualenv_name)\h:\w \$(__git_head)$ "


Here is an example of default PS1:

    (django_env)MacBook-Air:~/Projects/Foo/src (master)
    $


