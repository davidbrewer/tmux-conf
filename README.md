tmux-conf
=========

My tmux configuration. Built upon the excellent foundation provided by Brian P. Hogan's excellent book "tmux". Actually. to be perfectly honest there's not much here yet EXCEPT that foundation.

This version supports the version of Tmux found in Ubuntu Bionic, which is 2.6. If you want to use it with an older version, check the branches of this repository.


Additional Notes
================

Make sure to add the following to the end of .bashrc to get full color support under Linux:

  [ -z "$TMUX" ] && export TERM=xterm-256color

For support for system clipboard, make sure to install "xclip" package.
