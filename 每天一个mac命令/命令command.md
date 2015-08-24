#command命令

<!-- create time: 2015-08-24 14:30:14  -->

<!-- This file is created from $MARBOO_HOME/.media/starts/default.md
本文件由 $MARBOO_HOME/.media/starts/default.md 复制而来 -->

BUILTIN(1)                BSD General Commands Manual               BUILTIN(1)

###名称

     builtin, !, %, ., :, @, {, }, alias, alloc, bg, bind, bindkey, break,
     breaksw, builtins, case, cd, chdir, command, complete, continue, default,
     dirs, do, done, echo, echotc, elif, else, end, endif, endsw, esac, eval,
     exec, exit, export, false, fc, fg, filetest, fi, for, foreach, getopts,
     glob, goto, hash, hashstat, history, hup, if, jobid, jobs, kill, limit,
     local, log, login, logout, ls-F, nice, nohup, notify, onintr, popd,
     printenv, pushd, pwd, read, readonly, rehash, repeat, return, sched, set,
     setenv, settc, setty, setvar, shift, source, stop, suspend, switch,
     telltc, test, then, time, times, trap, true, type, ulimit, umask,
     unalias, uncomplete, unhash, unlimit, unset, unsetenv, until, wait,
     where, which, while -- shell built-in commands

概括

     builtin [-options] [args ...]

DESCRIPTION
     
     Shell builtin commands are commands that can be executed within the run-
     ning shell's process.  Note that, in the case of csh(1) builtin commands,
     the command is executed in a subshell if it occurs as any component of a
     pipeline except the last.

     If a command specified to the shell contains a slash ``/'', the shell
     will not execute a builtin command, even if the last component of the
     specified command matches the name of a builtin command.  Thus, while
     specifying ``echo'' causes a builtin command to be executed under shells
     that support the echo builtin command, specifying ``/bin/echo'' or
     ``./echo'' does not.

     While some builtin commands may exist in more than one shell, their oper-
     ation may be different under each shell which supports them.  Below is a
     table which lists shell builtin commands, the standard shells that sup-
     port them and whether they exist as standalone utilities.

     Only builtin commands for the csh(1) and sh(1) shells are listed here.
     Consult a shell's manual page for details on the operation of its builtin
     commands.  Beware that the sh(1) manual page, at least, calls some of
     these commands ``built-in commands'' and some of them ``reserved words''.
     Users of other shells may need to consult an info(1) page or other
     sources of documentation.

     Commands marked ``No**'' under External do exist externally, but are
     implemented as scripts using a builtin command of the same name.

           Command       External    csh(1)    sh(1)
           !             No          No        Yes
           %             No          Yes       No
           .             No          No        Yes
           :             No          Yes       Yes
           @             No          Yes       Yes
           {             No          No        Yes
          