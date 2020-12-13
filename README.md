# Installation

```
npm i @robinblomberg/nps
```

# Usage

```javascript
const { scripts } = require('@robinblomberg/nps')(exports);

scripts.coverage = {
  description: 'Analyzes test code coverage.',
  script: 'nyc --all npm test'
};

scripts.list = {
  description: 'Lists all scripts.',
  script: 'echo; && nps --help --help-style basic && echo;'
};

scripts.test = {
  description: 'Runs all tests.',
  script: 'mocha'
};

scripts.testWatch = {
  description: 'Runs all tests in watch mode.',
  script: 'mocha --watch --parallel'
};
```
