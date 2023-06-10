## Refs
- <https://github.com/junegunn/fzf.vim>
- <https://github.com/junegunn/fzf/blob/master/README-VIM.md>
    - In particular, once set `:set rtp+=system("which fzf")`,
      you can do basic fuzzy file search in Vim via `:FZF [dir]`, e.g.
        - `:FZF ~/Documents/`
        - `:FZF` is equiv. to `:FZF .`
