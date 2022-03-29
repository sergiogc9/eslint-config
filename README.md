![](https://badgen.net/npm/v/@sergiogc9/eslint-config?icon=npm&label)
![](https://github.com/sergiogc9/eslint-config/workflows/Github%20Pipeline/badge.svg?branch=master)

Eslint personal config

## Table of contents

- [Table of contents](#table-of-contents)
- [Configurations available](#configurations-available)
- [Installation](#installation)
  - [Install package](#install-package)
  - [Peer dependencies](#peer-dependencies)
- [Usage](#usage)

## Configurations available

This package contains some different eslint configurations:

- `@sergiogc9/eslint-config`:

  Contains the base rules for `typescript` and `javascript` with the recommended ones together with `airbnb` rules, as well as with `prettier` rules.

- `@sergiogc9/eslint-config/react`:

  Contains `react` specific rules together with react `hooks` rules defined by Airbnb. React v16.8 must be used at least.

- `@sergiogc9/eslint-config/jest`:

  Contains settings related to `jest` testing. Don't use it if not using jest.

- `@sergiogc9/eslint-config/all`:

  Contains all the available configurations together.

## Installation

#### Install package

Using yarn:

```
yarn add -D @sergiogc9/eslint-config
```

Using npm:

```
npm install -D @sergiogc9/eslint-config
```

#### Peer dependencies

Install all needed plugins and configs:

```
npx install-peerdeps --dev @sergiogc9/eslint-config
```

ℹ️ The command above will install all needed dependencies from all eslint configs. If you don't use react, jest or don't want to install some of these configs, install only dependencies related to each package:

- Dependencies for base config (and the others config):

```
yarn add -D \
    eslint \
    @typescript-eslint/eslint-plugin \
    eslint-plugin-eslint-comments \
    eslint-plugin-import \
    eslint-plugin-prettier \
    prettier
```

- Dependencies for react config:

```
yarn add -D \
    eslint-plugin-jsx-a11y \
    eslint-plugin-react \
    eslint-plugin-react-hooks
```

- Dependencies for jest config:

```
yarn add -D eslint-plugin-jest
```

## Usage

Add the wanted configuration(s) inside the `.eslintrc` file in extends option:

```
{
    ...,
    extends: [
        "other_config",
        "@sergiogc9/eslint-config"
    ]
}
```

E.g. if you want react rules but not jest ones:

```
{
    ...,
    extends: [
        "other_config",
        "@sergiogc9/eslint-config",
        "@sergiogc9/eslint-config/react"
    ]
}
```

E.g. if you want all rules available in this package:

```
{
    ...,
    extends: [
        "other_config",
        "@sergiogc9/eslint-config/all"
    ]
}
```
