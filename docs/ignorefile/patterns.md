# Patterns

Each line in the ignore file specifies a glob pattern. All patterns are evaluated relative to the solution directory. You can add comments by prefixing a line with _#_.

Here is an overview of some common patterns.

| Pattern     | Description                                                           |
|-------------|-----------------------------------------------------------------------|
| dir/        | Ignores all files in the directory _dir_ and all its subdirectories.  |
| dir/file.cs | Ignores the file _file.cs_ in the directory _dir_.                    |
| *.cs        | Ignores all files with a _.cs_ extension.                             |
| \*file\*.cs | Ignores all _.cs_ files with the word _file_ in the filename.         |
| dir/**/*.cs | Ignores all _.cs_ files in all subdirectories of the directory _dir_. |

## See Also

- [File globbing in .NET](https://docs.microsoft.com/en-us/dotnet/core/extensions/file-globbing#pattern-formats)