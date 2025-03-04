# eslint-config-godaddy-es5

Configuration for React _and_ non-React ES5 JavaScript applications officially used at GoDaddy. There are many useful features:

- **Standard. No configuration.** – Stop worrying about style and focus on your work.
- **Modern** – Uses modern linting tools like `eslint`.
- **Auto-fix** – Auto-fix is enabled by-default through in `eslint`. Many rules will fix themselves!

This styleguide is used by dozens of product teams at GoDaddy. Have a question or comment? [Open an issue!](https://github.com/godaddy/javascript/issues/new)

## Installation

``` sh
# Legacy ES5 (including React rules)
npm i eslint-config-godaddy-es5 --save-dev
```

## Usage

There are two ways to use this styleguide depending on your own tooling preference: directly using pre-included binaries or running `eslint` yourself with a custom `.eslintrc` config.

##### 1. Use the pre-included binaries.

These use _exactly_ the configuration defined in this  package (`eslint-config-godaddy-es5`) **with auto-fix enabled automatically.**

``` js
{
  "scripts": {
    "lint": eslint-godaddy-es5 files/ you/ want-to/ lint/",
    "lint-react": "eslint-godaddy-es5-react files/ you/ want-to/ lint/"
  }
}
```

##### 2. Define your local `.eslintrc.js` and run `eslint` yourself:

``` js
module.exports = {
  // Or for ES5 + React:
  // extends: 'godaddy-es5-react',
  extends: 'godaddy-es5',
  rules: {
    //
    // Put any rules you wish to override here.
    //
  }
}
```

The `--fix` option in `eslint` is [**only** available as a CLI option](https://github.com/eslint/eslint/issues/8041). Auto-fix will *NOT be enabled* unless you run `eslint --fix` in your `package.json`.

``` js
{
  "scripts": {
    "lint": "eslint --fix files/ you/ want-to/ lint/"
  }
}
```
