# ob-stata.el
Modified version of `ob-stata.el` from the [a mirror of the EMACS repository](https://github.com/Fuco1/org-mode/blob/master/contrib/lisp/ob-stata.el) 
that
1. strips commands in org-mode src output
2. refines the regex replace to avoid deleting output from some stata commands

The description of what this does and how to use it is [found here](http://rlhick.people.wm.edu/posts/stata-and-literate-programming-in-emacs-org-mode.html).

The modifications described above only works with src blocks with `:results output` and for stata sessions invoked by `:session`. 
