# minimal-reproduction-template

First, read the [Renovate minimal reproduction instructions](https://github.com/renovatebot/renovate/blob/main/docs/development/minimal-reproductions.md).

Renovate Issue/Discussion number: [36329](https://github.com/renovatebot/renovate/discussions/36329).

## Current behavior

Renovate creates update PRs using `uv`'s latest version regardless of what
version is specified in the `pyproject.toml` in `tool.uv.required-version`.

It leads to an error message in a renovate comment and a fail to update
the lockfile:
```
Required uv version `==0.7.0` does not match the running version `0.7.11`. Update `uv` by running `uv self update 0.7.0`.
```

Example [PR](https://github.com/tanguylefloch-veesion/renovate-repro-uv-version-detection/pull/3).

## Expected behavior

Renovate to pickup the expected uv version, otherwise the
`required-version` feature of `uv` is unsable unless `uv` is always up to
date.

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/36329
