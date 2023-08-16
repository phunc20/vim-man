## Copy and Paste
- X
    - Primary selection: `Shift-Insert`
    - Secondary selection
    - Clipboard selection: `Ctrl-v`
    - What you copy in X either by, say, `Ctrl-v` in browser, or by, say,
      `Ctrl-Shift-v` in the terminal will be saved into **both the primary
      and the clipboard selections**
- Vim
    - In Vim, the concept of copy/paste or clipboard is called **register**.
      Vim has multiple registers, which you can see by typing `:register` or
      more briefly `:reg` inside a Vim session. Notably,
        - `""` is what normally will be pasted when you press `p` in normal
          mode in Vim. This is the same as pressing `""p`. As an extra example,
          say, you want to paste the content of the 4th register, you could
          accomplish this by `"4p`
            - When you yank in Vim, Vim will usually save the yanked content
              into both the `""` and `"0` registers
            - But there's a but. When you set in your `.vimrc`
              ```
              set clipboard=unnamedplus
              ```
              The following behaviours will take place
                - When you paste using `p` in Vim, the content from `"+` will get
                  pasted
                - When you yank in Vim, all four registers `"", "0, "*, "+` will save
                  the yanked content
                - When you copy in X (either `Ctrl-c` or `Ctrl-Shift-c`), only the
                  registers `"*, "+` get the copied content, not `"", "0`
        - `"*` corresponds to the **primary** selection
        - `"+` corresponds to the **clipboard** selection

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
