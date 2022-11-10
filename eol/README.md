## Stop `vim` from Adding Newline
1.
:set nofixendofline

2.
vim -b file
:set noeol
:wq

3.
:set binary
:set noeol
:wq

Ref.
<https://stackoverflow.com/questions/1050640/how-to-stop-vim-from-adding-a-newline-at-end-of-file>
<https://stackoverflow.com/questions/16222530/why-do-i-need-vim-in-binary-mode-for-noeol-to-work>
