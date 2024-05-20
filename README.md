# SEA-EYE 👀

No frils collection of common actions and pre-made workflows for TypeScript project that uses `yarn@v1` as package manager.

## Workflows

- Build - run build, lint and test

## Actions

- Yarn Cache - cache installed deps

```yaml
- uses: vtno/seaeye/.github/actions/yarn-build@v0.1.0
  with:
    node-version: "16" # override the default version here
    working-dir: "." # override working dir to run the command here
```

- Yarn Install - install deps and cache using Yarn Cache action

```yaml
- uses: vtno/seaeye/.github/actions/yarn-install@v0.1.0
  with:
    node-version: "16" # override the default version here
    working-dir: "." # override working dir to run the command here
```

- Yarn Build - build with cached deps

```yaml
- uses: vtno/seaeye/.github/actions/yarn-build@v0.1.0
  with:
    node-version: "16" # override the default version here
    working-dir: "." # override working dir to run the command here
```

- Yarn Test - test with cached deps

```yaml
- uses: vtno/seaeye/.github/actions/yarn-test@v0.1.0
  with:
    node-version: "16" # override the default version here
    working-dir: "." # override working dir to run the command here
```

- Yarn Lint - lint with cached deps

```yaml
- uses: vtno/seaeye/.github/actions/yarn-lint@v0.1.0
  with:
    node-version: "16" # override the default version here
    working-dir: "." # override working dir to run the command here
```

- Kumose Deployment - trigger for Kumose deployment
```yaml
- uses: vtno/seaeye/.github/actions/kumose-deployment@v0.4.0
  with:
    basic_auth_token: "" # Provide the basic auth token here
    kumose_app_id: "" # Provide the Kumose app ID here
    version: "latest" # Specify the version here
```

## Examples

1. Using the `build` workflow - [workflow_test.yml](https://github.com/vtno/seei/blob/v0.1.0/.github/workflows/workflow_test.yml)
```yaml
jobs:
  call-build-workflow:
    uses: vtno/seaeye/.github/workflows/build.yml@v0.1.0
    with:
      working-dir: example
```

2. Using `Yarn Test` action - [build.yml](https://github.com/vtno/seei/blob/v0.1.0/.github/workflows/build.yml#L46-L48)
