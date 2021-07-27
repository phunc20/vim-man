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


