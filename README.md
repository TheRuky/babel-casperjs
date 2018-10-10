# babel-casperjs

**⚠ IMPORTANT ⚠** 
- The runner assumes **you have already installed PhantomJS and CasperJS globally**. If not, go to [PhantomJS](http://phantomjs.org/) and [CasperJS](http://casperjs.org/) respective websites for detailed instructions on how to install them globally or locally and modify `package.json` scripts as necessary.

- The runner, by default, uses [Yarn](https://yarnpkg.com/en/), so if you want to use [npm](https://www.npmjs.com/) to run scripts, change `package.json` scripts from `yarn` to `npm run`. For example, `build` script would become `npm run clean && npm run babel`.

### How to run?

To run Babel and/or CasperJS, use scripts from `package.json`.

| Script        | Description   | Arguments     |
| ------------- |:-------------:|:-------------:|
| `babel`      | Runs Babel and transpiles the code to destination folder (`bin` by default). | - |
| `build`      | Runs `clean` and `babel` scripts. | - |
| `clean` | Deletes destination folder (`bin` by default). | - |
| `start` | Runs `clean`, `babel` and `test` scripts. | File to run (e.g. `bin/index.js`) |
| `test` | Runs CasperJS. | File to run (e.g. `bin/index.js`) |

Example: `yarn start bin/index.js`.

**TL;DR** Use `build` to build without running and `test` to run, or `start` for both.
