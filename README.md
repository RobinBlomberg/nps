# Installation

```
npm i -D @robinblomberg/nps
```

# Usage

Create a file called **package-scripts.js**:

```javascript
const nps = require('@robinblomberg/nps')(exports);

nps.checkCoverage = 'nyc --all npm test';

nps.test = 'mocha';

nps.testWatch = {
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

# ESM support

If you're using ESM modules, rename your script file to package-scripts.**cjs**.

Then, create a file called **.npsrc.json**:

```json
{
  "config": "./package-scripts.cjs"
}
```
