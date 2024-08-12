Cf. `:help usr_28`

- `zf`: Create fold
- `zo`: Open fold
- `zc`: Close fold
- `zr`: Reduce fold
- `zm`: More fold
- `zR`: Reduce fold (for nested folds)
- `zM`: More folds (for nested folds)
- `zn`: No fold
- `zN`: Undo `zn`
- `za`: Toggle btw `zn` and `zN`
- `zd`: Delete fold
    - Prefer `zo`, `zc` and `za` to `zd`, which once deleted cannot recover
      with redundant texts
        - Another level downwards
          with redundant texts
- `zO`: Open all folds (at the cursor line)
- `zC`: Close all folds (at the cursor line)
- `zD`: Delete all folds (at the cursor line)


Folds will open when
- entering insert mode
- jumping around, e.g. by using `/`
- moving cursor left or right, e.g. `0`, `$`, `l` or `r`


Folding is local to windows. This allows one to open two windows
on the same buffer, one with folds and one without.
