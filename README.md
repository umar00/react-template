# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

 prettier: Formats our code automatically according to a defined code style
 eslint: Analyzes our code and enforces best practices
 eslint-config-react: Enables rules in ESLint relevant to React projects
 eslint-config-prettier: Disables rules relating to code style in ESLint so that Prettier can handle them instead
 eslint-plugin-jsx-a11y: Allows ESLint to check for accessibility (a11y) issues in our JSX code

run this:
    npx eslint src
    eslint src --fix
    npx eslint src

running this in the package:
    npm pkg set scripts.lint="eslint src"

Setting up Husky for commit proper code
    we might miss some of these errors and accidentally commit code. Husky and lint-staged setup
-npm install --save-dev husky@8.0.3 \
    lint-staged@15.1.0
    
    -adding to package.json
    "lint-staged": {
  "**/*.{js,jsx}": [
    "npx prettier --write",
    "npx eslint --fix"
    ]
    }
