```vim
:reg[isters]
```

```
Type Name Content
  l  ""   ^J
  c  "0   kbd
  l  "1   ^J
  l  "2   #np.fill_diagonal(rel_err, 1)^J
  l  "3   ^J
  l  "4   end^J
  l  "5     mktempdir()^J
  l  "6   function a()^J
  l  "7     #folder = mktempdir()^J
  l  "8         end^J
  l  "9           write(io, data)^J
  c  "e   0v/:^MhS<M<80>kbcode>j
  c  "g   ggg/dq
  c  "j   j
  c  "l   <80>kb
  c  "o   0yss<code>I- ^[j
  c  "p   v$hS<code>^[<80><fd>aj
  c  "q
  c  "r   ysw"/,^Mll
  c  "t   cs'"jjkk
  c  "-
  c  "*   asjidfjaijf
  c  "+   asjidfjaijf
  c  ".   ^@```
  c  ":   q
  c  "%   README.md
  c  "/   etc
Press ENTER or type command to continue
```

To paste text from one of these registers, say from `"9`, it
suffices to type `"9p` in normal mode.

See more at `:h reg`


## Refs
- <https://stackoverflow.com/questions/1497958/how-do-i-use-vim-registers>
- <https://www.baeldung.com/linux/vim-registers>
- <https://www.brianstorti.com/vim-registers/>
