# setup-yq

Sets up [YQ](https://github.com/mikefarah/yq) for use in your CI jobs. (And it caches it, too!)

By default, it installs `yq==4.34`.

## Usage

```
# in your job:
name: MY GREAT JOB
on:
  push:
    branches:
      - '*'
jobs:
  yq-example:
    name: YQ example!
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v1
    - uses: infovista-opensource/setup-yq4@latest
    - name: Show folks how to run YQ:
      run: |
        yq --help

```

## Hacking

After you've made changes, you must run `npm run build` and commit the
`dist/index.js`, or else your changes won't take effect!

## History

- Forked from https://github.com/chrisdickinson/setup-yq - thanks @chrisdickinson !

## License

Apache-2.0
