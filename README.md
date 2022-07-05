# .editorconfig

A combination of,
- [RehanSaeed/EditorConfig][2]
- [editorconfig - dotnet/runtime][1]

The main differences compared to [RehanSaeed/EditorConfig][2] is in the following,

> Adapted from [dotnet/runtime][1]

1. We use `_camelCase` for internal and private fields and use `readonly` where possible. Prefix internal and private instance fields with `_`, static fields with `s_` and thread static fields with `t_`. When used on static fields, `readonly` should come after `static` (e.g. `static readonly` not `readonly static`).  Public fields should be used sparingly and should use PascalCasing with no prefix when used.
2. We avoid `this.` unless absolutely necessary.
3. Namespace imports should be specified at the top of the file, *outside* of
   `namespace` declarations, and should be sorted alphabetically, with the exception of `System.*` namespaces, which are to be placed on top of all others.

## Additional Resources
- [C# Coding Style - dotnet/runtime](https://github.com/dotnet/runtime/blob/main/docs/coding-guidelines/coding-style.md)

[1]: https://github.com/dotnet/runtime/blob/main/.editorconfig
[2]: https://github.com/RehanSaeed/EditorConfig
