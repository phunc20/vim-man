
- 4 spaces to 2 spaces
  - `%s;^\(\s\+\);\=repeat(' ', len(submatch(0))/2);g`
  - More precisely, the above demands to divide the number of spaces by 2.
    Similarly, one can demand to multiply the number of spaces by, say 3, through
    `%s;^\(\s\+\);\=repeat(' ', len(submatch(0))*3);g`

- There are many ways to delete all the blank lines, e.g.
  - `%s/^$\n//g`

