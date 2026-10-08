# Inject Markdown CLI

Inject Markdown CLI tool that can be used with pre-commit hooks

## Setup [pre-commit](https://pre-commit.com) Hook

This repository enables using [inject-markdown](https://github.com/streetsidesoftware/inject-markdown) as a [pre-commit](https://pre-commit.com) hook.

<!-- x-release-please-start-version -->

```yaml
# .pre-commit-config.yaml
repos:
  - repo: https://github.com/streetsidesoftware/inject-markdown-cli
    rev: v3.1.2
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
  files                          Files to scan for injected content.

Options:
  --no-must-find-files           No error if files are not found.
  --output-dir <dir>             Output Directory
  --cwd <dir>                    Current Directory
  --allow-outside-root <dir>     Allow local @@inject references to resolve into
                                 <dir>, outside the injection root (cwd).
                                 Repeatable.
  --value <name=val>             Set a run-wide {@ name @} placeholder value.
                                 Repeatable; the last --value, --values-file or
                                 --value-alias defining a name wins.
  --values-file <[prefix:]path>  Add a run-wide JSON file of {@ name @}
                                 placeholder values, resolved relative to --cwd.
                                 Repeatable.
  --allow-env <name>             Allow a directive to reference the OS
                                 environment variable <name> via {@ env.name @}.
                                 Repeatable.
  --value-alias <new=target>     Resolve the {@ new @} placeholder as if it were
                                 {@ target @}. Repeatable; ordered with --value
                                 and --values-file.
  --strict-vars                  Treat an unresolved {@ name @} placeholder as a
                                 directive error.
  --no-rebase-links              Keep relative links in injected Markdown as
                                 written instead of rebasing them.
  --clean                        Remove the injected content.
  --no-inject-only               Update the whole file.
  --verbose                      Verbose output.
  --silent                       Only output errors.
  --no-stop-on-errors            Do not stop if an error occurs.
  --write-on-error               write the file even if an injection error
                                 occurs.
  --color                        Force color.
  --no-color                     Do not use color.
  --no-summary                   Do not show the summary
  --dry-run                      Process the files, but do not write.
  -V, --version                  output the version number
  -h, --help                     display help for command
```

<!--- @@inject-end: static/help.txt --->
