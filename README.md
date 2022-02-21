# devbook-envs

This repo contains two custom environments for [Devbook](https://usedevbook.com) that can be published with the [Devbook CLI](https://github.com/devbookhq/devbookctl).

- [How to build custom environments](https://github.com/devbookhq/devbookctl#usage---deploying-custom-environment).
- See how The Devbook CLI `dbk` is integrated into the [GitHub Action](./.github/workflows/ci.yml).

## 1. [banana-node](./banana-node/) environment

Contains preinstalled Nodejs 16 and globally installed `@banana-dev/banana-dev` package.

### Publish the env
```sh
# Install Devbook CLI https://github.com/devbookhq/devbookctl
$ curl -L https://usedevbook.com/install.sh | sh

# Push from the dir.
$ cd ./banana-node && dbk push
```

### Usage with [Devbook SDK](https://github.com/DevbookHQ/sdk)
```jsx
import { useDevbook } from '@devbookhq/sdk'

const { runCmd, stdout, stderr } = useDevbook({ env: 'banana-node' })
```

## 2. [banana-python](./banana-python/) environment
Contains preinstalled Python3 and pip3 with `banana-dev` package installed.

### Publish the env
```sh
# Install Devbook CLI https://github.com/devbookhq/devbookctl
$ curl -L https://usedevbook.com/install.sh | sh

# Push from the dir.
$ cd ./banana-python && dbk push
```

### Usage with [Devbook SDK](https://github.com/DevbookHQ/sdk)
```jsx
import { useDevbook } from '@devbookhq/sdk'
const { runCmd, stdout, stderr } = useDevbook({ env: 'banana-python' })
```


