- across all opened files, e.g.
  ```
  bufdo %s/string/replacement/g
  ```
- 4 spaces to 2 spaces
  - `%s;^\(\s\+\);\=repeat(' ', len(submatch(0))/2);g`
  - More precisely, the above demands to divide the number of spaces by 2.
    Similarly, one can demand to multiply the number of spaces by, say 3, through
    `%s;^\(\s\+\);\=repeat(' ', len(submatch(0))*3);g`

- There are many ways to delete all the blank lines, e.g.
  - `%s/^$\n//g`
- comma-separated odd numbers.
  - One use case for this is when one uses an old printer which cannot flip the
    printed papers, in which case one needs to
    1. print first the odd pages
    2. flip them
    3. print the even pages (on the back of those odd pages)
    
    In Vim, for example, one could use `:put=range(1,10,2)` to generate
    ```
    1
    3
    5
    7
    9
    ```
    Then, usually, the printer's interface would ask for `1,3,5,7,9`, i.e.
    a comma-separated line of page numbers. To obtain this, **use**
    `:%s/\n/,/g` and **don't use** `:%s/$/,/g`, the latter resulting in
    ```
    1,
    3,
    5,
    7,
    9,
    ```
