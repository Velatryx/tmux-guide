## Splitting windows

> In this guide, I will only provide shortcuts instead of commands (which are not practical) unless it's necessary. Remember, `Ctrl + b` is the core prefix, and your friend! Play around with these as you go, and you will eventually get better.

*To split the window into two vertical panes, use: `Ctrl + b` then `%`.

*To split the window into two horizontal panes, use: `Ctrl + b` then `"`.

---

## Selecting panes

> To select a pane in any direction, you can again use a shortcut: `Ctrl + b` then `any arrow key` on your keyboard. For instance, `Ctrl + b` then `→' to switch to pane on right of current pane.

More on here: [tmux selectp](https://tmux.info/docs/commands/split-window)

---

## Resizing panes

Resizing is pretty similar to selecting panes. You should hit `Ctrl + b` and `any arrow key` at the same time, hold the prefix while doing so, until it's resized to your liking. Note that resizing of the window will depend on its position. If you have to panes divided horizontally, you will use 'up_arrowkey', or 'down_arrowkey'.

More on here: [tmux resizep](https://tmux.info/docs/commands/resize-pane)

---

## Killing panes

Simply choose the pane you wish to kill wit `Prefix + arrowkey`, and press `Ctrl + b` then `x`. 

---

## Respawning panes

> Reuse a pane to run a command, restarting it in place without changing the layout. Handy for re-running a dead or crashed pane.

This one does not have a direct shortcut. You will have to use:

```bash
tmux respawnp -t 1 'top'
```

This respawns pane 1 running top.

Detailed [here](https://tmux.info/docs/commands/respawn-pane)

---

>TIP: If you're lost, use `Ctrl + b` then `?` for built-in help

