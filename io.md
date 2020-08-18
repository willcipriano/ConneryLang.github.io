# File IO

### file
Builtin 
{: .label .label-purple }
The file builtin takes either an operation type, filename and perhaps a string depending on the operation. Then reads or writes the file.

| Operation Type             | Purpose                                           |
|:---------------------------|:--------------------------------------------------|
| READ                       | Reads a file, returning it as a string            |
| WRITE                      | Writes to a file, overwriting if it already exists|
| APPEND                     | Appends string to a file                          |

The syntax is as follows:
```
; Read a file
file READ "testfile.txt"

; Write to a file (overwrite if already exists)
file WRITE "testfile.txt" "file content"

; Append to a file
file APPEND "testfile.txt" "this is appended to the file"
```

## Helper functions

### file_read
StdLib
{: .label .label-green }
file_read is an easier way to read a file, it simply takes a string containing the filename.
```
file_read "filename.file"
```

### file_write
StdLib
{: .label .label-green }
file_write, like file_read makes it easier to write files. It takes a string containing the filename and the file content.
```
file_write "filename.file" "this is the content"
```

### file_append
StdLib
{: .label .label-green }
file_append is similar to file write, but appends to files as opposed to overwriting them.
```
file_append "filename.file" "this will be appended"
```
