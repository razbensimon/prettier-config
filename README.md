# `@razbensimon/prettier-config`

> Raz's [Prettier](https://prettier.io) config.

## Usage

**Install**:

```bash
$ npm install --save-dev husky lint-staged prettier
$ npm install --save-dev @razbensimon/prettier-config
```

**Edit `package.json`**:

```jsonc
{
  "scripts": {
    // ...
    "prettier": "prettier --write \"src/**/*.{js,jsx,ts,tsx,json,css,scss,md}\"",
    "prettier-check": "prettier -c \"src/**/*.{js,jsx,ts,tsx,json,css,scss,md}\""
  },
  // ...
  "prettier": "@razbensimon/prettier-config",
  "lint-staged": {
    "src/**/*.{js,jsx,ts,tsx,json,css,scss,md}": [
      "prettier --write",
      "git add"
    ]
  },
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged"
    }
  },
  // ...
}
```
