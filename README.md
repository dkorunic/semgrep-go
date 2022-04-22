# semgrep-go

## About

This repo is holding [Semgrep](https://semgrep.dev/) patterns for finding possibly problematic code.

To run individual semgrep rule on the current Go project:

```shell
semgrep -f rule.yml .
```

To run all included semgrep rules on the current Go project:

```shell
semgrep -f path/to/semgrep-go/ .
```

To make Semgrep [skip over some](https://semgrep.dev/docs/ignoring-files-folders-code/) files (ie. go-swagger or some other auto-generated files), use either `.semgrepignore` or `.gitignore`.

## Contents

- `json-without-jsoniter`: check for stdlib _json_ `Marshal()` or `Unmarshal()` use without _jsoniter_
- `err-overwrite.yml`: check if err is being overwritten in Go routines without shadow declarations
