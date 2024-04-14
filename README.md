# Lume build

This action setup Deno, build your Lume site and cache the DENO_DIR directory so
the next builds are faster.

## Usage

```yml
name: Build site

on: push

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v4
    - uses: lumeland/build@main
```

By default runs `deno task build` command. To configure a different command:

```yml
steps:
- uses: actions/checkout@v4
- uses: lumeland/build@main
  with:
    cmd: deno task build --location=https://example.com
```
