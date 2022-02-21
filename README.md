# devbook-envs

This repo contains two custom environments for [Devbook](https://usedevbook.com).

[How to build custom environments](https://github.com/devbookhq/devbookctl).

Two custom envs:
## [banana-node](./banana-node/) environment

Contains preinstalled Nodejs 16 and globally installed `@banana-dev/banana-dev` package.

### Usage with [Devbook SDK](https://github.com/DevbookHQ/sdk)
```jsx
import { useDevbook } from '@devbookhq/sdk'

const { runCmd, stdout, stderr } = useDevbook({ env: 'banana-node' })
```

## [banana-python](./banana-python/) environment
Contains preinstalled Python3 and pip3 with `banana-dev` package installed.

### Usage with [Devbook SDK](https://github.com/DevbookHQ/sdk)
```jsx
import { useDevbook } from '@devbookhq/sdk'
const { runCmd, stdout, stderr } = useDevbook({ env: 'banana-python' })
```


