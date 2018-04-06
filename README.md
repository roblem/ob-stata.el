# ob-stata.el
Modified version of `ob-stata.el` from the EMACS repository that
1. strips most commands in org-mode src output (see remaining issues below)
2. refines the regex replace to avoid deleting output from some stata commands

The description of what this does and how to use it is [found here](http://rlhick.people.wm.edu/posts/stata-and-literate-programming-in-emacs-org-mode.html).

The modifications described above only works with src blocks with `:results output` and for stata sessions invoked by `:session`. 

## Remaining issues
While this code does a pretty good job of eliminating commands in results output, there are issues with long commands (commands greater than 77 characters).  This code (as well as the original code this was forked from) does not currently handle line continuation syntax (using `///`) and will throw a syntax error if you try to use it.  Long commands can only be run from single lines of code and these are not eliminated in the src output.
