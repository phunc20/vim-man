## The Configuration File
Depending on your Vim, the variable `$MYVIMRC` will point to
the file path of your Vim's configuration file, e.g.
- Vim: Usually `~/.vimrc`
- NeoVim: Usually `~/.config/nvim/init.vim`

The following are a few examples of how to use `$MYVIMRC`:
- Open Vim's configuration file
  ```vim
  # Either
  :find $MYVIMRC<CR>
  # Or
  :split $MYVIMRC<CR>
  ```
- Source Vim's configuration file
  ```vim
  :source $MYVIMRC<CR>
  ```

In order to start `vim` or `nvim` with a configuration file other than
the one pointed to by `$MYVIMRC`, use the `-u` option:
```bash
$ vim -u /path/to/customed.vimrc
```


## Copy and Paste
Cf. `../registers/README.md`
