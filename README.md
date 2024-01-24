## Steps to reproduce

Using npm 10.3.0 (see volta config in `package.json`)

1. `npm ci`
2. `npm ls` <- 0.8.1
3. `npm i -w front --save-exact react-roi@0.9.0`
4. `npm ls` <- 0.9.0
5. `npm i -w front --save-exact react-roi@0.11.0`
6. `npm ls` <- still 0.9.0!! (should be 0.11.0)

## Comments

- If `overrides` is removed from `package.json` then the bug does not exist.
- If the dependency is not installed in a workspace but at the root the bug does not exist.