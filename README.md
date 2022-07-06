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
4. Prefers the use of conditional expression for assignment and return.
5. We only use `var` when the type is explicitly named on the right-hand side, typically due to either `new` or an explicit cast, e.g. `var stream = new FileStream(...)` not `var stream = OpenStandardInput()`.
    - Similarly, target-typed `new()` can only be used when the type is explicitly named on the left-hand side, in a variable definition statement or a field definition statement. e.g. `FileStream stream = new(...);`, but not `stream = new(...);` (where the type was specified on a previous line).
6. `csharp_indent_labels` set to `one_less_than_current` : [See options](https://docs.microsoft.com/en-us/dotnet/fundamentals/code-analysis/style-rules/csharp-formatting-options#csharp_indent_labels)
7. `csharp_indent_case_contents_when_block` set to `true` : [See options](https://docs.microsoft.com/en-us/dotnet/fundamentals/code-analysis/style-rules/csharp-formatting-options#csharp_indent_case_contents_when_block)
8. `csharp_space_around_declaration_statements` set to `do_not_ignore` (❔as per [this](https://docs.microsoft.com/en-us/dotnet/fundamentals/code-analysis/style-rules/csharp-formatting-options#csharp_space_around_declaration_statements), the options are `ignore`, `false` but most dotnet repos set to `do_not_ignore`).
9. We use PascalCasing to name all our constant local variables and fields.

## Additional Resources
- [C# Coding Style - dotnet/runtime](https://github.com/dotnet/runtime/blob/main/docs/coding-guidelines/coding-style.md)

[1]: https://github.com/dotnet/runtime/blob/main/.editorconfig
[2]: https://github.com/RehanSaeed/EditorConfig
