# Motivation

I typically use [tmux](https://www.ocf.berkeley.edu/~ckuehl/tmux/) when working on remote servers, but sometimes I don't remember keybindings or commands for some functions that I rarely use.

Since I find the tmux help/manpage rather confused, I usually revert to [this cheatsheet](https://tmuxcheatsheet.com/), which is very well organized.
However, I'd want to avoid to rely on a webpage for documentation that I would better checkout in the terminal, maybe using grep.

For this reason I packaged a text file with the same content reported in [the above mentioned cheatsheet](https://tmuxcheatsheet.com/), with a format that is terminal friendly.

This is an excerpt of the file:

# Organization for effective search

I organized the content so that every explanation is on the same line of the corresponding keybinding.
Moreover, the "action" (e.g., open, kill, start, etc.) precedes the "target object" (e.g., window, pane, etc.).

In this way, it is possible to grep the cheatsheet with a pattern like

```
$ grep "close.*window" tmux-cheatsheet.txt 
Ctrl + b &                 close current window
```
or

```
$ grep "resize.*pane" tmux-cheatsheet.txt 
Ctrl + b + up-arrow            resize current pane height (holding second key is optional)
Ctrl + b Ctrl + up-arrow       resize current pane height (holding second key is optional)
Ctrl + b + down-arrow          resize current pane height (holding second key is optional)
Ctrl + b Ctrl + down-arrow     resize current pane height (holding second key is optional)
Ctrl + b + right-arrow         resize current pane width (holding second key is optional)
Ctrl + b Ctrl + right-arrow    resize current pane width (holding second key is optional)
Ctrl + b + left-arrow          resize current pane width (holding second key is optional)
Ctrl + b Ctrl + left-arrow     resize current pane width (holding second key is optional)
```


