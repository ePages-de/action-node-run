# action-node-run

GitHub Action for installing Node/Yarn packages on development environment and running commands. It caches dependencies for reduced execution times.

## Inputs

| Name           | Description                                               | Default | Required |
| -------------- | --------------------------------------------------------- | ------- | -------- |
| `node_version` | The node version to be used.                              | `18`    | `true`   |
| `cache_key`    | The cache key to be checked. Can be one of `npm`, `yarn`. | `yarn`  | `true`   |
| `cmd`          | The command to be executed.                               | `nil`   | `true`   |

## Usage

```yml
jobs:
  eslint:
    runs-on: ubuntu-latest
    steps:
      - uses: ePages-de/action-node-run@v1
        with:
          node_version: 18
          cache_key: yarn
          cmd: npx eslint
```
