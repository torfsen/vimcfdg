vimcfdg
=======

A Vim Syntax File for CFDG
--------------------------
This is a syntax highlighting file [Vim](http://www.vim.org) which adds support for the [Context Free](http://www.contextfreeart.org) language (CFDG).


Installation
------------
Installing this syntax file works the same as installing any syntax file for Vim. It's descibed in [chapter 44.11](http://vimdoc.sourceforge.net/htmldoc/usr_44.html#44.11) of the Vim documentation (use `:help 44.11` inside Vim). The following installation instruction is for Linux/Unix/etc.:

* Create the directory `~/.vim/syntax` if it doesn't exist
* Copy the file `cfdg.vim` into that directory

This is a good time to configure the syntax file to suit your needs (path to image viewers, etc.). Read the comments in the file for details. You can then enable the syntax file for the current buffer using `:set syntax=cfdg`. If you want the syntax file to be enabled automatically for all files with a `.cfdg` ending, add the following lines to your `~/.vimrc` and restart Vim:

    augroup filetypedetect
    au BufNewFile,BufRead *.cfdg setf cfdg
    augroup END
    filetype plugin on


Usage
-----
In addition to pure syntax highlighting, this syntax file provides some basic commands to run `cfdg` on the file you are currently editing. They are accessible via different keyboard shortcuts:

* `\cc`: Compiles the current file. Note that any changes since the last save are not taken into account.
* `\cv`: Same as `\cc`, but asks for a variation code first.
* `\cd`: Displays the last image produced by `\cc` or `\cv`.
* `\cb`: Like `\cc` followed by `\cd`.
* `\ca`: Like `\cv` followed by `\cd`.

Note that you may have to configure some settings (e.g. paths to image viewers) before everything works. See the comments in `cfdg.vim` for details.

