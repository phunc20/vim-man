# Buffers
A buffer is like an itermediate step/place to hold text that we type in before saving to a file.
When we `:w`, Vim simply copies the buffer to the filename we give to Vim.

When you type `vim` in the command line without specifying a filename to edit, Vim opens an _empty_
buffer for you to edit text; eventually, you may save the edited text to a file by `:w` or just discard
it by `:q!` if you find your text useless at the end.

If you have already open a file in Vim, say, by inputting `vim mem_hog.py` in the command line, and that
you want an empty buffer, then you can

- `new`: This is like a `:sp`/`:split` but opens an empty new buffer
- `vnew`: This is like a `:vsp`/`:vsplit` but opens an empty new buffer

Other related commands include

- `:ls`
- `:b2`, `:b#`, etc.
- `:e another_file.py`


