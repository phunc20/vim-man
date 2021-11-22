# Indentation and Tab

## Interchange btw `indent=2` and `indent=4`
Cf.
- <https://stackoverflow.com/questions/16888658/change-2-space-indent-to-4-space-in-vim>
- <https://vim.fandom.com/wiki/Indenting_source_code>

Correct answers:


Incorrect answers:

- `gg=G`. This won't work for, e.g. the following Python code. (It only indent for the first line.)
  ```python
  def normalize(points: list, width: int, height: int) -> list:
    x0, y0, x2, y2 = [int(p) for p in points]
  
    x0 = int(1000 * (x0 / width))
    x2 = int(1000 * (x2 / width))
    y0 = int(1000 * (y0 / height))
    y2 = int(1000 * (y2 / height))
  
    return [x0, y0, x2, y2]
  ```


## A Few Concepts and Keywords
- `expandtab`, boolean (default off/false)
    - can be set in a vim session by `:set expandtab` or, more briefly, `:set et`
    - once set (to true), vim will not write `<Tab>` when you type the Tab key; instead, vim will start to write some number of spaces in place of `<Tab>` depending on your setting
- `>` and `<` in visual mode
- Check the current `tabstop` value (cf. <https://stackoverflow.com/questions/2078271/get-current-value-of-a-setting-in-vim>)
    - The same as setting it but append with a question mark: `:set tabstop?`
- `shiftwidth`

##

ts := tabstop, sts := softtabstop and [no]et := [no]expandtab
:retab
ins-expandtab


:%s/^\s*/&&
Simply replaces leading space (spaces or tabs) with twice as much leading space (& is substituted with the matched expression).


It may be possible with :set shiftwidth=4 and gg=G.

