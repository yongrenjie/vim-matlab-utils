# vim-matlab-utils

A Vim plugin that contains some small convenience features for working with Matlab files

----------

## Go to file

`gf` opens the Matlab file corresponding to the function under the cursor.

Note that this is still quite primitive.
It only works with simple functions, or functions placed within Matlab 'packages'.
It doesn't work with classes (yet), and there is no guarantee that it will obey Matlab's specifications for [path resolution](https://uk.mathworks.com/help/matlab/matlab_oop/scoping-classes-with-packages.html).

The solution to this is for the programmer (you) to either:

1. Not use Matlab. Since you are reading this, this is probably quite unlikely. However, if you have a choice on a different project, please try not to use it.

2. Be very careful about file naming in order to avoid clashes.


-----------

## Documentation

`K` opens a popup window at the cursor showing documentation for the function under the cursor.

The popup window can be scrolled with `<C-j>` and `<C-k>`. Pressing `K` again will close the popup window.

The same caveats as for `gf` apply here.
In addition, it should be noted that (for now) this only works with Vim 8 (and not Neovim), because it uses the `popup_...()` family of functions introduced in Vim 8.2.
