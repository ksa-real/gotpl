# Sprig command line tool

Command line for [Sprig](https://github.com/Masterminds/sprig). Works with YAML and for JSON as part of YAML.

## Install

```bash
go install github.com/ksa-real/gotpl@latest
```

## Usage

### Data from argument

```bash
gotpl -t /path/to/template -i /path/to/data.yaml
gotpl "{{ .a }}" "a: vvv"
gotpl '{{ .a.b }}' '{ a: { b: "ccc" }}'
gotpl '{{ .a.b }}' -i /path/to/data.yaml
```

### Data from stdin

```bash
gotpl '{{ uuidv4 }}'
cat test/my-data.yaml | gotpl "{{ .root.key1 }}"
```

## Build
```bash
go build
```

