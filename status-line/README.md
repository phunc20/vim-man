
`status-line` is a displaying mechanism which can be used, among other utilities, to

- display the current filename
- display the current git branch

To have a permanent setup, e.g. put in your `.vimrc` the following:
```
set laststatus=2
set statusline=
set statusline+=\ %f
```

Enter your vim editor and type `:h status` to learn more from the manual.










