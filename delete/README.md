




## `g`
A few examples:
```
# Delete all empty lines
:g/^$/d
# Delete all empty lines or lines with spaces only
:g/^\s*$/d
# Exclamation mark can be used to invert. So does :v, i.e.
# Both of the following lines delete those lines that does not contain foo
:g!/foo/d
:v/foo/d

```










