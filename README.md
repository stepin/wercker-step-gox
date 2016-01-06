Wercker step gox [![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](https://github.com/tcnksm/wercker-step-gox/blob/master/LICENCE)
====

[![wercker status](https://app.wercker.com/status/5c756560b605b20ad2330182431657b9/s/master "wercker status")](https://app.wercker.com/project/bykey/5c756560b605b20ad2330182431657b9)

This is [wercker](http://wercker.com/) step for [mitchellh/gox](https://github.com/mitchellh/gox), cross-compile golang project.

## Usage

In the `wercker.yml` of your application use the following step definition:

```
steps:
    - tcnksm/gox
```

This step will generate binaries to `${WERCKER_OUTPUT_DIR}/pkg/{{.OS}}_{{.Arch}}/{{.Dir}}`.

## Options

You can control build with some option from `wercker.yml`:

```yaml
steps:
   - tcnksm/gox:
     os: "darwin linux windows" # OS to cross-compile
     arch: "386 amd64"          # ARCH to cross-compile
```

## Author

[tcnksm](https://github.com/tcnksm)
