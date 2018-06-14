
This repository has been moved to https://gitlab.com/robhicks/ob-stata.el.  Please track progress and report issues there.

# ob-stata.el
Modified version of `ob-stata.el` from the EMACS repository that
1. strips most commands in org-mode src output (see remaining issues below)
2. refines the regex replace to avoid deleting output from some stata commands
3. supports line continuation (`///`) for stata commands

The description of what this does and how to use it is [found here](http://rlhick.people.wm.edu/posts/stata-and-literate-programming-in-emacs-org-mode.html).

The modifications described above only work with src blocks with `:results output` and for stata sessions invoked by `:session`. 

## Remaining issues
While this code does a pretty good job of eliminating commands in results output, there are some instances with line continuation and long commands where commands may not be stripped from output.
