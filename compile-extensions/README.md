# compile extensions

A library which provides extra functions and overrides for Cloud
Foundry Buildpack compile scripts.

This is included a git submodule in all the official Cloud Foundry buildpacks.

## check\_stack\_support

Print out a lovely error message when the current `stack` is not supported by the buildpack.

### Usage

```bash
./compile-extensions/bin/check_stack_support
```

## download\_dependency

Translates the URL given in `ARGV[0]` by matching the URL to a corresponding entry in `manifest.yml` and downloads the translated file with `curl`.

### Usage

```bash
./compile-extensions/bin/download_dependency [URI] [INSTALL_DIR]
```

## is\_cached

Returns an exit status of `0` if the current buildpack is a cached buildpack.

### Usage

```bash
./compile-extensions/bin/is_cached
```

## default\_version\_for

Returns the default version in the manifest (if specified) for a given dependency

### Usage

```bash
./compile-extensions/bin/default_version_for [MANIFEST_FILE] [DEPENDENCY_NAME]
```
