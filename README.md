# .editorconfig

A combination of,
- [RehanSaeed/EditorConfig](https://github.com/RehanSaeed/EditorConfig)
- [editorconfig - dotnet/runtime](https://github.com/dotnet/runtime/blob/main/.editorconfig)

The main difference compared to `RehanSaeed/EditorConfig` is in the following,

1. We use _camelCase for internal and private fields and use readonly where possible. Prefix internal and private instance fields with _, static fields with s_ and thread static fields with t_. When used on static fields, readonly should come after static (e.g. static readonly not readonly static). Public fields should be used sparingly and should use PascalCasing with no prefix when used.
2. We avoid this. unless absolutely necessary.

## Additional Resources
- [C# Coding Style - dotnet/runtime](https://github.com/dotnet/runtime/blob/main/docs/coding-guidelines/coding-style.md)
