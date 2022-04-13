
- 4 spaces to 2 spaces
  - `%s;^\(\s\+\);\=repeat(' ', len(submatch(0))/2);g`
  - More precisely, the above demands to divide the number of spaces by 2.
    Similarly, one can demand to multiply the number of spaces by, say 3, through
    `%s;^\(\s\+\);\=repeat(' ', len(submatch(0))*3);g`

- There are many ways to delete all the blank lines, e.g.
  - `%s/^$\n//g`
- comma-separated odd numbers.
  - The use case of this is when one uses an old printer which cannot flip the
    printed papers for them, in which case one needs to print first the odd
    pages, flip them, and finally print the even pages on the back of those
    odd pages.
    
    In Vim, one could use `:put=range(1,10,2)` to generate
    ```
    1
    3
    5
    7
    9
    ```
    Then, usually, the printer's API would ask for `1,3,5,7,9`, i.e.
    a comma-separated line of page numbers. To achieve this, **use**
    `:%s/\n/,/g` and <s>don't use</s> `:%s/$/,/g`, the latter resulting in
    ```
    1,
    3,
    5,
    7,
    9,
    ```
