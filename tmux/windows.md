## Window Management

After you attach to a session, you will have only 1 window, with index of 0, and a name (either you assigned with `-n`, or default name - bash).

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


## Killing Windows

> To kill a window, 
