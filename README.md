tmux-conf
=========

My tmux configuration. Built upon the excellent foundation provided by Brian P. Hogan's excellent book "tmux". Actually. to be perfectly honest there's not much here yet EXCEPT that foundation.

This version supports the version of Tmux found in Ubuntu Bionic, which is 2.6. If you want to use it with an older version, check the branches of this repository.

Additional Install Notes
========================

Make sure to add the following to the end of .bashrc to get full color support under Linux:

  [ -z "$TMUX" ] && export TERM=xterm-256color

For support for system clipboard on Linux, make sure to install "xclip" package.

Using on OS X
=============

This works on OS X in addition to Linux. If installing on OS X, make sure you have Homebrew installed and then:

```
brew install tmux
git clone https://github.com/davidbrewer/tmux-conf.git ~/.tmux-conf
ln -s ~/.tmux-conf/tmux/conf ~/.tmux.conf
```

(It assumes you’re using Linux, but the config works on Mac. You just have to brew install tmux, and then place the file tmux.conf at ~/.tmux.conf ) (edited) 

Starting tmux
=============

You'll start tmux from the terminal in one of the following ways:

```
# Start a default session with no special name
tmux

# Start a new session with a defined name
tmux new -s SessionName

# Get a list of running sessions
tmux ls

# Attach to an existing session
tmux attach -t SessionName
```

Keybindings
===========

This isn't complete documentation of the keybindings, but to get you started...

All tmux commands start with a "prefix" which you hit to go into "tmux command mode". You do the prefix, let go of it, and then hit the command listed below You can change this in the configuration, but by default the prefix is `control-a`.

Commands (following prefix):
* `|`: split a pane into two side by side panes (that's "prefix-verticalpipe")
* `-`: split a pane into two vertically stacked panes. (that's prefix-minus)
* `h`: select the pane to the left of the current pane
* `j`: select the pane under the current pane
* `k`: select the pane above the current pane
* `l`: select the pane to the right of the current pane
* `shift-H`: resize panes, moving the vertical divider to the left
* `shift-J`: resize panes, moving the horizontal divider down
* `shift-K`: resize panes, moving the horizontal divider up
* `shift-L`: resize panes, moving the vertical divider to the right
* `c`: create a new "window" inside tmux
* `NUM`: jump to the window indicated by NUM (an integer)
* `[`: turn on vertical buffer scrolling in a pane (can use arrows or pageup/pagedown to scroll, ESC then return to exit scrolling)
* `SPACE`: cycle through layout options for tabs
* `CTRL-o`: rotate the contents of the panes, moving the contents of the current pane to another pane
* `,`: rename the current window (adding a label at the bottom)
* `d`: "detach" from the current session (going back to the terminal that you launched tmux from)
* `x`: kill the current pane
* `z`: ZOOM into the current pane, enlarging it to the full terminal. Repeat the command to zoom back out
* `w`: display a neat menu of all the panes you have open 
