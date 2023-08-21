# Buffers
A buffer in Vim is like an itermediate place to hold text
that we type in before saving to a file. When we `:write <some_filename>`,
Vim simply copies the buffer to the filename we give to Vim.

When you type `vim` in the command line without specifying a filename to edit,
Vim opens an _empty_ buffer for you to edit text with buffer name **`[No Name]`**.
At this step, if you want, you can change the buffer name, say, to `bar` by
```vim
:file bar
```

Eventually, you may save the edited text in the buffer to a file by
`:w <some_filename>` or you may discard it by `:q!`
if you find your text useless at the end.

If you have already opened a file in Vim, say,
by inputting `vim mem_hog.py` in the command line, and that
you want an empty buffer in a split, then you can

- Horizontally
    - `new`: This is like a `:split` but opens an empty new buffer named `[No Name]`
    - `new bar`: Same as the above but with buffer name `bar`
- Vertically
    - `vnew`: This is like a `:vsplit` but opens an empty new buffer named `[No Name]`
    - `vnew bar`: Same as the above but with buffer name `bar`

Other related commands include

- `:ls`
- `:b2`, `:b#`, `:bd 2`, etc. (`:b` stands for `:buffer`)
- `:e another_file.py`


