# eslint-config-hubspot

[![npm version](https://badge.fury.io/js/eslint-config-hubspot.svg)](https://badge.fury.io/js/eslint-config-hubspot)

> Forked from [Airbnb's Style Guide](https://github.com/airbnb/javascript)

This package provides HubSpot's .eslintrc as an extensible shared config.


## Usage

We export three ESLint configurations for your usage.

### eslint-config-hubspot

Our default export contains all of our ESLint rules, including EcmaScript 6+
and React. It requires `eslint`, `babel-eslint`, and `eslint-plugin-react`.

1. `npm install --save-dev eslint-config-hubspot babel-eslint eslint-plugin-react eslint`
2. add `"extends": "hubspot"` to your .eslintrc

### eslint-config-hubspot/base

Lints ES6+ but does not lint React. Requires `eslint` and `babel-eslint`.

1. `npm install --save-dev eslint-config-hubspot babel-eslint eslint`
2. add `"extends": "hubspot/base"` to your .eslintrc

### eslint-config-hubspot/legacy

Lints ES5 and below. Only requires `eslint`.

1. `npm install --save-dev eslint-config-hubspot eslint`
2. add `"extends": "hubspot/legacy"` to your .eslintrc

See [HubSpot's Javascript styleguide](https://github.com/HubSpot/javascript) and
the [ESlint config docs](http://eslint.org/docs/user-guide/configuring#extending-configuration-files)
for more information.

## Improving this config

Consider adding test cases if you're making complicated rules changes, like
anything involving regexes. Perhaps in a distant future, we could use literate
programming to structure our README as test cases for our .eslintrc?

You can run tests with `npm test`.

You can make sure this module lints with itself using `npm run lint`.

## Changelog

### 0.1.0

- switch to modular rules files courtesy the [eslint-config-default][ecd]
  project and [@taion][taion]. [PR][pr-modular]
- export `eslint-config-airbnb/legacy` for ES5-only users.
  `eslint-config-airbnb/legacy` does not require the `babel-eslint` parser.
  [PR][pr-legacy]

[ecd]: https://github.com/walmartlabs/eslint-config-defaults
[taion]: https://github.com/taion
[pr-modular]: https://github.com/airbnb/javascript/pull/526
[pr-legacy]: https://github.com/airbnb/javascript/pull/527

### 0.0.9

- add rule no-undef
- add rule id-length

### 0.0.8
 - now has a changelog
 - now is modular (see instructions above for with react and without react versions)