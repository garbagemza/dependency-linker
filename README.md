[![cdlinker](https://github.com/garbagemza/dependency-linker/actions/workflows/go.yml/badge.svg)](https://github.com/garbagemza/dependency-linker/actions/workflows/go.yml)

# cdlinker
This tool attempts to link compiled objects and create libraries. Use it in combination of dependency-checker and dependency-compiler.

## dependencies

This tool depends on `ar` to perform creation of libraries.

## build

`go build -v ./...`

`cdlinker` is created for you.

## run

This tool is intended for use with command line on global scope

Put this binary on your bin/ directory and use.

## usage

1. Use dependency-checker `cdcheck` first, as it will download your required dependency. The file output and directory structure is used by `cdcompiler`.
2. Use dependency-compiler `cdcompiler`, it will create the objects and directory structure that `cdlinker` needs.
3. Run `cdlinker`. That's it.

- After the archive is done. You will find new files created for you.
Your new libraries will be located here:
`build` > `output` > `<library name>` > `output`.

4. Use the libraries to link executables.
