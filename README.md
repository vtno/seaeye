# SEA-EYE 👀

No frils collection of common actions and pre-made workflows for TypeScript project that uses `yarn@v1` as package manager.

## Workflows

- Build - run build, lint and test

## Actions

- Yarn Cache - cache installed deps

```yaml
- uses: vtno/seei/.github/actions/yarn-build@main
  with:
    node-version: "16" # override the default version here
    working-dir: "." # override working dir to run the command here
```

- Yarn Install - install deps and cache using Yarn Cache action

```yaml
- uses: vtno/seei/.github/actions/yarn-install@main
  with:
    node-version: "16" # override the default version here
    working-dir: "." # override working dir to run the command here
```

- Yarn Build - build with cached deps

```yaml
- uses: vtno/seei/.github/actions/yarn-build@main
  with:
    node-version: "16" # override the default version here
    working-dir: "." # override working dir to run the command here
```

- Yarn Test - test with cached deps

```yaml
- uses: vtno/seei/.github/actions/yarn-test@main
  with:
    node-version: "16" # override the default version here
    working-dir: "." # override working dir to run the command here
```

- Yarn Lint - lint with cached deps

```yaml
- uses: vtno/seei/.github/actions/yarn-lint@main
  with:
    node-version: "16" # override the default version here
    working-dir: "." # override working dir to run the command here
```

## Examples

1. Using the `build` workflow - [workflow_test.yml](https://github.com/vtno/seei/blob/main/.github/workflows/workflow_test.yml)
```yaml
jobs:
  call-build-workflow:
    uses: vtno/seei/.github/workflows/build.yml@main
    with:
      working-dir: example
```

2. Using `Yarn Test` action - [build.yml](https://github.com/vtno/seei/blob/main/.github/workflows/build.yml#L46-L48)
