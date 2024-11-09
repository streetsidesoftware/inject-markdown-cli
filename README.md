# Inject Markdown CLI

Inject Markdown CLI tool that can be used with pre-commit hooks

## Setup [pre-commit](https://pre-commit.com) Hook

This repository enables using [inject-markdown](https://github.com/streetsidesoftware/inject-markdown) as a [pre-commit](https://pre-commit.com) hook.

<!-- x-release-please-start-version -->

```yaml
# .pre-commit-config.yaml
repos:
  - repo: https://github.com/streetsidesoftware/inject-markdown-cli
    rev: v3.0.0
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
