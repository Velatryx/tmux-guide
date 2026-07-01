## Let's get started with sessions.

### Creating sessions:
> Start a new session with:

```bash
tmux new-session
```
or if you want to customize the session name:

```bash
tmux new -s mysession
```
This creates a new session and attaches the session instantly named "mysession". Adding `-n` in the end of it will name the window of your choice.

> Attaching to an existing session called "main", if not, creating a new one named "main"

```bash
tmux new -A -s main
```

[tmux creating sessions](tmux.info/docs/commands/new-session)

---

## Attaching to sessions

Let's say you accidentally closed the terminal, and don't know how to open the session you created. You can use the command:

```bash
tmux attach -t main
```
And get back to your work on "main" session.

Similarly, you can attach or create (if doesn't exist) to a session by adding `-A` option.


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

If you're in an active session, you can also list the existing sessions using: 'Ctrl + b' + s. This opens a small, and interactive window and lets you choose a session.

> NOTE: This .md file has contents heavily based on, but paraphrased in simpler language, and given context to core utilities, instead of everything as in the specified resource. Feel free to check it out for more options.
[tmux.info](tmux.info/docs/commands)
