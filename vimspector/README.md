## FAQs
1. How to install?
    - I use vim-plug, so
        1. Put the following line in your `vim.rc` or `init.vim`
           ```vim
           Plug 'puremourning/vimspector'
           ```
1. Why Vim is complaining `require vim compiled with +python3`?
    - If you encounter this problem and that you're using Arch Linux,
      then
      ```shell
      $ pacman -S python-pynvim
      ```
