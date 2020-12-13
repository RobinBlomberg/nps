# Installation

```
npm i @robinblomberg/nps
```

# Usage

Create a file called **package-scripts.js**:

```javascript
const scripts = require('@robinblomberg/nps')(exports);

scripts.coverage = {
  description: 'Analyzes test code coverage.',
  script: 'nyc --all npm test'
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

List all scripts:

```
nps
```

Run a script:

```
nps testWatch
```
