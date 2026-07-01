## Window Management

After you attach to a session, you will have only 1 window, with index of 0, and a name (either you assigned with `-n`, or default name - bash).


## Creating windows 

> To create a new window inside your current session:

```bash
tmux neww -n logs
```

<img width="388" height="69" alt="image" src="https://github.com/user-attachments/assets/eaba4bd5-b4b6-4d6f-bf52-2b8eae779fd1" />


This creates a new window named logs (with the help of `-n`, and neww (new-window))

> Or you can create a new window to run a process:

```bash
tmux neww 'htop'
```

This will create a new window running 'htop'.

> If you want to run this process in the background:

```bash
tmux neww -d -n background 'make build'
```
--- 

## Selecting windows

> You can select windows with `tmux selectw -n (or -l)` -n being next and -l being last, but more practical way is just using a shortcut.

### `Ctrl + b then [0-9]` to choose a window with prefix of your choice. This is the recommended way, as it is the fastest. `Ctrl + b then l` selects the last window. 

---

## Killing windows

> To kill a window, use:

```bash
tmux killw -t 1
```

This kills the window with the *INDEX* of 1.

Similarly, you can kill all windows but current one with: 

```bash
tmux killw -a
```

---

## Listing Windows
```
tmux lsw -a
```

>Example Output:


```
murcy@fedora:~$ tmux lsw -a
bye:0: bash (1 panes) [171x43] 
bye:1: bash- (1 panes) [171x43] 
bye:2: bash* (1 panes) [171x43] 
main:0: bash* (1 panes) [171x43]
```

---

## Renaming windows

```
tmux renamew -t 0 main
```

Here, '0' is the index of the window unlike in session management.

---

## Respawning windows

[Respawn guide](https://tmux.info/docs/commands/respawn-window)


---

>TIP: If you're lost, use Ctrl + b then ? for built-in help
