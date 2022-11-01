filegroup(
  name = "files",
  srcs = glob(["*.txt"]) + [":copied_file"],
)

genrule(
  name = "copied_file",
  srcs = ["//foo:copied_file.txt"],
  outs = ["copied.txt"],
  cmd = "cp $(location //foo:copied_file.txt) $@",
)

genrule(
  name = "list_files",
  srcs = [":files"],
  outs = ["out.txt"],
  cmd = "ls -la > $@",
)
