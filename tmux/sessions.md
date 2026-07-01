## Let's get started with sessions.

> 💻 **Prerequisite:** This guide expects you to be using a Unix-like terminal, preferably running `bash` or `zsh`

---

### Creating sessions:

> Open your terminal, and start a new session with:

```bash
tmux new-session
```
or if you want to customize the session name:

```bash
tmux new -s mysession
```
This creates a new session and attaches the session instantly named "mysession". Adding `-n <name>` in the end of it will name the window of your choice.

> Attaching to an existing session called "main", if not, creating a new one named "main"

```bash
tmux new -A -s main
```

[tmux creating sessions](https://tmux.info/docs/commands/new-session)

---

## Attaching to sessions

Let's say you accidentally closed the terminal, and don't know how to open the session you created. You can use the command:

```bash
tmux attach -t main
```
And get back to your work on "main" session.

Similarly, you can attach or create (if doesn't exist) to a session by adding `-A` option.


---

## Listing sessions

If you have many sessions, or you forgot your session's name, you can simply list them.

```bash
tmux ls
```

```
murcy@fedora:~$ tmux ls
hello: 1 windows (created Wed Jul  1 15:32:01 2026)
main: 1 windows (created Wed Jul  1 15:31:49 2026)
```

---

## Renaming Sessions

Choosing a name for a session might not seem really important, but for a good workflow, it makes the tracking easier. If you are not happy with the name, use: 

> Changing the session named '0' to hello.

```bash
tmux rename -t 0 hello
```

`rename`: renames a session
`-t`: specifies the target session, and '0' is the name of the session.

---

## Detaching sessions

You can use `tmux detach` to detach the current session, but it is not very practical. The best way is to use a shortcut:

> `'Ctrl + b' then d`


---

## Killing sessions

Simply detaching the sessions do not erase them. That's why we can use:

```bash
tmux kill-session -t dev
```

This kills the session named 'dev'.

> If you wish to kill all sessions except current one:

```bash
tmux kill-session -a
```

> And if you want to kill all sessions except the target session:

```bash
tmux kill-session -a -t main
```

Killing all sessions except 'main'.

---

## Switching sessions

Personally, I like just using `'Ctrl + b' then s` to list sessions, and choosing a session with arrow keys and pressing enter to choose, because it's easier, and more convenient. However, you can still find out more about switching [here](https://tmux.info/docs/commands/new-session).

---

If you're in an active session, you can also list the existing sessions using: `'Ctrl + b' then s`. This opens a small, and interactive window and lets you choose a session. Shortcuts will be discussed later. 

---

>TIP: If you're lost, use Ctrl + b then ? for built-in help

> NOTE: This .md file has contents heavily based on, but paraphrased in simpler language, and given context to core utilities, instead of everything as in the specified resource. Feel free to check it out for more options.
[tmux.info](https://tmux.info/docs/commands)
