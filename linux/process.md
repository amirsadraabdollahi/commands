# Process

1. get the jobs in the current shell
```commandline
jobs
jobs -l # gets you the process id of that process either.
```
ctrl+z would stop the process.

2. background a job
```commandline
bg %<job_index> # bg %2
```
by using ```&``` at the end of your command, it runs in background.

3. foreground a job
```commandline
fg %<job_index> # bg %2
```

4. by default every command terminated, if the parent process terminated.
to avoid this you can use ```nohup``` command.
```commandline
nohup <command>
nohup xclock
nohup script.sh > mynohup.out 2>&1 & 
```

5. ```kill``` command use to send signal to some process. 
#### important signal ids:

- 1 HUP: informing the process that its' controlling terminal (like a ssh connection) is terminated.
- 15 TERM: normal termination request
- 9 KILL: forcefully kills the process.
```commandline
kill -SIGNAL_ID_OR_NAME process_id # by default the signal id is 15 if not provided.
kill 1500 # it equals to kill -15 1500
```

6. use ```killall``` to kill all process with a provided name.
```commandline
killall sleep
killall xeyes
```

7. ```pkill``` will send the given signal (default 15) to all the processes with a specific pattern in their name.
```commandline
pkill exey
pkill xcl
```

8. get processes
```commandline
ps # just ps of a shell
ps -e # shows all processes of the system
ps -ef # gets you more info of each ps
pgrep eyes # use this to combine ps and grep
```

9. use ```top``` to get overall state of the system and processes.

10. use ```watch``` to get result from command every desired seconds.
```commandline
watch -n 3 <command> # by default it has 2second delay
watch "command | command" # if you have pipe, you should use quotes.
```

11. to have multiple shell use ```screen```

```commandline
screen # create a screen
screen -ls # shows all screen id
screen -r screen-id # use id to reattach the screen
```
#### tips:
- use ctrl+a before using any switches
- D: detach from the current window
- K: kill current window
- |: split current window in to two vertical focuses.
- Shift+S: split current window in to two horizontal focuses.
- Tab: go to the next focus.
- C: create a window (shell) in current focus.
- N: move to next window
- P: move to previous window
- \: kill all processes windows and terminate the screen

12. be professional and use ```tmux``` :)

```commandline
tmux
tmux ls
tmux attach -t tmux-id
```
#### tips:
- use ctrl+b before using any switches
- D: detach from the current window
- C: create new window and attach to it
- &: kill current window
- %: split current window vertically
- ": split current window horizontally
- use arrows to switch between windows.
- ctrl+b then tmux-id to go to tmux-id window

## modify process priorities

1. the niceness is related to each process. the lower niceness, the high priority to obtaining cpu and memory.
```commandline
nice # the default value of niceness
nice -n 14 <command> # run the command with the niceness 14
```

2. change the niceness of a process.
```commandline
renice -n 5 <ps_id>
```
