# npmdoc-validate-commit-msg

#### api documentation for  [validate-commit-msg (v2.12.1)](https://github.com/kentcdodds/validate-commit-msg#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-validate-commit-msg.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-validate-commit-msg) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-validate-commit-msg.svg)](https://travis-ci.org/npmdoc/node-npmdoc-validate-commit-msg)

#### Script to validate a commit message follows the conventional changelog standard

[![NPM](https://nodei.co/npm/validate-commit-msg.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/validate-commit-msg)

- [https://npmdoc.github.io/node-npmdoc-validate-commit-msg/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-validate-commit-msg/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-validate-commit-msg/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-validate-commit-msg/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-validate-commit-msg/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-validate-commit-msg/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "validate-commit-msg",
    "description": "Script to validate a commit message follows the conventional changelog standard",
    "main": "index.js",
    "version": "2.12.1",
    "scripts": {
        "add-contributor": "all-contributors add",
        "generate-contributors": "all-contributors generate",
        "commit": "git-cz",
        "commitmsg": "opt --in commitmsg --exec \"node ./lib/cli.js\"",
        "precommit": "opt --in precommit --exec \"npm run validate\"",
        "check-coverage": "istanbul check-coverage --statements 100 --branches 90 --functions 100 --lines 100",
        "report-coverage": "cat ./coverage/lcov.info | codecov",
        "test:watch": "istanbul cover -x test/**/*.test.js node_modules/mocha/bin/_mocha -- -R spec -w test/**/*.test.js",
        "test": "istanbul cover -x test/**/*.test.js node_modules/mocha/bin/_mocha -- -R spec test/**/*.test.js",
        "validate": "npm t && npm run check-coverage",
        "semantic-release": "semantic-release pre && npm publish && semantic-release post"
    },
    "bin": {
        "validate-commit-msg": "./lib/cli.js"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/kentcdodds/validate-commit-msg.git"
    },
    "keywords": [
        "githook",
        "commit",
        "message",
        "git",
        "conventional",
        "changelog"
    ],
    "author": "Kent C. Dodds <kent@doddsfamily.us> (http://kentcdodds.com/)",
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/kentcdodds/validate-commit-msg/issues"
    },
    "homepage": "https://github.com/kentcdodds/validate-commit-msg#readme",
    "devDependencies": {
        "all-contributors-cli": "3.0.7",
        "chai": "3.4.1",
        "codecov.io": "0.1.6",
        "commitizen": "2.5.0",
        "cz-conventional-changelog": "1.1.5",
        "husky": "0.12.0",
        "istanbul": "0.4.2",
        "mocha": "2.3.4",
        "opt-cli": "1.5.1",
        "semantic-release": "^6.3.2",
        "sinon": "1.17.2"
    },
    "config": {
        "commitizen": {
            "path": "node_modules/cz-conventional-changelog"
        },
        "validate-commit-msg": {
            "helpMessage": "\nPlease fix your commit message (and consider using http://npm.im/commitizen)\n",
            "types": [
                "feat",
                "fix",
                "docs",
                "style",
                "refactor",
                "perf",
                "test",
                "chore",
                "revert",
                "custom"
            ],
            "warnOnFail": false,
            "autoFix": false
        }
    },
    "dependencies": {
        "conventional-commit-types": "^2.0.0",
        "find-parent-dir": "^0.3.0",
        "findup": "0.1.5",
        "semver-regex": "1.0.0"
    },
    "files": [
        "index.js",
        "lib"
    ]
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
