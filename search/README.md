## Find in Normal Mode
- Forward find in normal mode: `f` and `/` are **different**!
- Backward find in normal mode: `F` and `?`

What do we mean by different? Well, here are a few major differences:
- `f` and `F` searches **in the same line**, i.e. when there
  is no more matched patterns, they **wouldn't** further search into next line. However, `/` and `?` searches across the entire text file [and even wraps around in case of exhaustion of file]
- `f` and `F`'s repeat search shortcut keys are `;` and `,` while those of `/` and `?` are `n` and `N`


## Relationship with `sed`
Basically, `sed` and `vim` share about the same searching patterns.


## Some Common Search Patterns
- Find the next non-blank start-of-sentence line: `/^[^ ]`
  - Useful in Python scripts, for example
  - Similar patterns can be build based on this, e.g. `<SOS>` after four spaces can be achieved by either one of the following:
    - `/^ \{4\}[^ ]`
    - `/^    [^ ]`
    - `/^\s\{4\}[^ ]`
    - `/^\s\s\s\s[^ ]`
  - It might be interesting to set file type specific shortcut key combinations for such a search, e.g. for Python
- Find variable definition in the same file
  - `gd` short for **Go to definition**. First occurrence of the word under cursor in the current function
  - `gD` goes to the first occurrence of the word under cursor in the current file
  - `[I` displays all the occurrences of the word along with line number
- Exact match
  - say, you want to find the word `mode` but not `model`, `modest`, you could do **`\<mode\>`**
  - you can also `mode\>` if you only want to restrict its RHS. I did not verify the mechanism, but I think that
    this is equiv. to `mode[^a-zA-Z]`
