# `vcpkg` + `cmake` Starting Template

## Checklist

- `vcpkg` and `cmake` installed
- `$VCPKG_ROOT` configured and in `$PATH`
- Project name changed in `CMakeLists.txt`
- Packages and linked libraries updated in `CMakeLists.txt`

## Cheatsheet

Add packages:

Modify `vcpkg.json` or `vcpkg add port <package_name_here>`

Debug build:

```
cmake --preset debug
cmake --build --preset debug
```

Release build:

```
cmake --preset release
cmake --build --preset release
```

`clangd` setup:

```
cmake --preset debug
cp build/debug/compile_commands.json build/compile_commands.json
```

