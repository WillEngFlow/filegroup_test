# Bazel `filegroup` test

Trying to grapple with how the Bazel `filegroup` rule actually works.

To demonstrate this weird behavior run:
```
bazel build //:list_files
```
and examine the output file. Note that there is a symlink to the `source_file.txt` file but not to the `copied_file.txt` or any derivative of it.

