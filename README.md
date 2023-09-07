# ember-3x-codemods

[![Build Status](https://travis-ci.org/ember-codemods/ember-3x-codemods.svg?branch=master)](https://travis-ci.org/ember-codemods/ember-3x-codemods) 
[![Coverage Status](https://coveralls.io/repos/github/ember-codemods/ember-3x-codemods/badge.svg?branch=master)](https://coveralls.io/github/ember-codemods/ember-3x-codemods?branch=master)
[![npm version](http://img.shields.io/npm/v/ember-3x-codemods.svg?style=flat)](https://npmjs.org/package/ember-3x-codemods "View this project on npm")
[![dependencies Status](https://david-dm.org/ember-codemods/ember-3x-codemods/status.svg)](https://david-dm.org/ember-codemods/ember-3x-codemods)
[![devDependencies Status](https://david-dm.org/ember-codemods/ember-3x-codemods/dev-status.svg)](https://david-dm.org/ember-codemods/ember-3x-codemods?type=dev)



A [jscodeshift](https://github.com/facebook/jscodeshift) Codemod with a collection of transforms to address the list of [deprecations](https://deprecations.emberjs.com/v3.x) introduced to Ember during the 3.x cycle

## Usage
To run a specific codemod from this project, you can:

Easily run the codemod on your project using the [Intuita VS Code extension](https://marketplace.visualstudio.com/items?itemName=Intuita.intuita-vscode-extension):

<a href="https://tinyurl.com/ember-codemods" target="_blank"> ![Open in Intuita](https://raw.githubusercontent.com/intuita-inc/intuita-docs/master/static/img/intuita-badge.svg) </a>

> To learn more about using the extension, [read the docs here](https://docs.intuita.io/docs/vs-code-extension/quickstart). If you encounter any issues, please [let us know.](https://www.intuita.io/community)


Alternatively, you can run the codemod with jscodeshift CLI:

```
npx ember-3x-codemods <TRANSFORM NAME> path/of/files/ or/some**/*glob.js

# or

yarn global add ember-3x-codemods
ember-3x-codemods <TRANSFORM NAME> path/of/files/ or/some**/*glob.js
```

## Transforms

### Deprecations & Transforms
| Introduced in | id | Transform |
| ------------- | -- | --------- |
| 3.1           | use-notifypropertychange... | [notify-property-change](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/notify-property-change) |
| 3.3           | jquery-event| [jquery-event](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/jquery-event) |
| 3.3           | jquery-event| [ember-jquery-legacy](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/ember-jquery-legacy) |
| 3.6           | ember-polyfills.deprecate-merge | [ deprecate-merge ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/deprecate-merge) |
| 3.6           | deprecate-router-events| [ deprecate-router-events ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/deprecate-router-events) |
| 3.6           | array.new-array-wrapper | [ new-array-wrapper ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/new-array-wrapper) |
| 3.6           | array.new-array-wrapper | [ array-wrapper ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/array-wrapper) |
| 3.6           | object.new-constructor | [ object-new-constructor ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/object-new-constructor) |
| 3.9           | computed-property.property | [ cp-property ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/cp-property) |
| 3.9           | computed-property.volatile | [ cp-volatile ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/cp-volatile) |
| 3.9           | computed-property.property | [ cp-property-map ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/cp-property-map) |
| 3.9           | jquery-apis| [ jquery-apis ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/jquery-apis) |
| 3.10           | application-controller.router-properties| [ app-controller-router-props ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/app-controller-router-props) |
| 3.11          | function-prototype-extensions.observes | [ fpe-observes ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/fpe-observes) |
| 3.11          | function-prototype-extensions.on | [ fpe-on ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/fpe-on) |
| 3.11          | function-prototype-extensions.property | [ fpe-computed ](https://github.com/ember-codemods/ember-3x-codemods/tree/master/transforms/fpe-computed) |


For more details, please visit the main Ember 3.x [deprecations](https://deprecations.emberjs.com/v3.x) page

## Contributing

### Installation

* clone the repo
* change into the repo directory
* `yarn`

### Running tests

* `yarn test`

### Update Documentation

* `yarn update-docs`
