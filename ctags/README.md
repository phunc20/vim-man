`ctags` is one way to allow `vim` users to jump back and forth
btw function/variable definitions and their appearances in
a code base.

To taste the power of `ctags` in `vim`, one has to
1. install `ctags` -- Usually the installation can be easily done
   via your system's package manager if you use some Unix/Linux distro.
2. Run `ctags` once to parse all the related files in your code base.  
   Usually, people run `ctags` as follows from the upmost directory level
   of their code base (or their repo):
   ```sh
   ctags -R .
   ```
   However, it is possible that one has populated one's repo with miscellaneous
   files that are not code, e.g. model weight file, image/text data files, etc.
   Tagging such files would deteriorate the performance.  
   The following is one quick workaround for this:
   ```sh
   ctags $(git ls-files)
   ```
   Both of the above commands will generate for you a file named `tags`, based
   on which `vim` could help users jump btw files.
3. Once equipped with a `tags` file, one can press
   - `^]` (i.e. `Ctrl` plus **closed bracket**) to **jump to the definition** of the entity on which
     their cursor is currently on
   - `^t` (i.e. `Ctrl` plus **t**) to **undo the above**, i.e. to jump backward in the tag stack


For more info, one could consult
- `man ctags`
- `man ctags-lang-python` (for Python users)

