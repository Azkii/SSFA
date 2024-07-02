# Project Overview

## Get Started

Requirements:

- Node 20+

You can setup project template with following commands.

```bash
git clone https://github.com/Azkii/SSFA.git
cd SSFA/example
cp .env.example .env
npm install
npm prepare
```

## Available Scripts

##### `npm run dev`

Runs the app in the development mode.
Open http://localhost:3000 to view it in the browser.

##### `npm run build`

Builds the app for production to the dist folder.
It correctly bundles React in production mode and optimizes the build for the best performance.

##### `npm run build:local`

Runs the check command and builds the app locally, outputting to the dist folder.

##### `npm run lint`

Runs ESLint on all TypeScript and TSX files in the src directory.

##### `npm run lint:fix`

Runs ESLint with the --fix option on all TypeScript and TSX files in the src directory to automatically fix problems.

##### `npm run ls-lint`

Runs ls-lint on the src directory to ensure file and directory naming conventions.

##### `npm run stylelint`

Runs Stylelint on all CSS files in the src directory, allowing empty input files.

##### `npm run stylelint:fix`

Runs Stylelint with the --fix option on all CSS files in the src directory, allowing empty input files, to automatically fix problems.

##### `npm run prettier`

Runs Prettier to check formatting on all files in the src directory.

##### `npm run prettier:fix`

Runs Prettier with the --write option to format all files in the src directory.

##### `npm run check`

Runs prettier, stylelint, lint, and ls-lint to check for any issues in the codebase.

##### `npm run format`

Runs prettier:fix, stylelint:fix, and lint:fix to automatically fix formatting and linting issues in the codebase.

## Pre-commit Hook

This project uses Husky to run a pre-commit hook. The pre-commit hook ensures that the codebase maintains quality by running checks before allowing a commit.

```bash
# .husky/pre-commit

npm run check
```
