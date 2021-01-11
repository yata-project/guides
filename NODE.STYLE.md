# Node/JavaScript Style Guide

## Project Setup

1. `prettier` should be added to the project as a dev dependency with
   `npm install --save-dev prettier`.
1. A script called `format` should exist in `package.json` containing
   `"prettier --write \"**/*.{js,json,md,html}\"",`
1. A script called `release` should exist in `package.json` containing
   `npm run test && npm run build`.

## Development

1. Code should be formatted with `npm run format`.
