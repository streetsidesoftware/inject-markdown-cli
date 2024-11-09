# Inject Markdown CLI

Inject Markdown CLI tool that can be used with pre-commit hooks

## Setup [pre-commit](https://pre-commit.com) Hook

This repository enables using [inject-markdown](https://github.com/streetsidesoftware/inject-markdown) as a [pre-commit](https://pre-commit.com) hook.

<!-- x-release-please-start-version -->

```yaml
# .pre-commit-config.yaml
repos:
  - repo: https://github.com/streetsidesoftware/inject-markdown-cli
    rev: v3.1.1
    hooks:
      - id: inject-markdown
```

<!-- x-release-please-end -->

## Install from GitHub

This repo also supports installing the `inject-markdown-cli` directly from GitHub:

```
npm install -g git+https://github.com/streetsidesoftware/inject-markdown-cli
```

## Usage

`inject-markdown-cli --help`:

<!--- @@inject: static/help.txt --->

```
Usage: inject-markdown [options] <files...>

Inject file content into markdown files.

Arguments:
  files                 Files to scan for injected content.

Options:
  --no-must-find-files  No error if files are not found.
  --output-dir <dir>    Output Directory
  --cwd <dir>           Current Directory
  --clean               Remove the injected content.
  --verbose             Verbose output.
  --silent              Only output errors.
  --no-stop-on-errors   Do not stop if an error occurs.
  --write-on-error      write the file even if an injection error occurs.
  --color               Force color.
  --no-color            Do not use color.
  --no-summary          Do not show the summary
  --dry-run             Process the files, but do not write.
  -V, --version         output the version number
  -h, --help            display help for command
```

<!--- @@inject-end: static/help.txt --->
