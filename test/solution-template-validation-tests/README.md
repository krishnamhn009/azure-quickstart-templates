# Run static validation checks for solution templates

This folder contains mocha tests, that runs static checks against a solution template folder containing mainTemplate.json, createUiDefinition.json and other template artifacts like nested templates, etc. A sample solution template folder named "sample-solution-template" is included, that can be used to run the checked in tests under the "test" folder.

## Prerequisites

- [Install](https://nodejs.org/en/) nodejs with npm

## Setup

- navigate to the "solution-template-validation-tests" folder
- npm install

## Running all tests

To run all tests
- npm --folder=/path/to/solutiontemplatefolder run all. For instance,
```
npm --folder=sample-solution-template run all
```

## Running createUiDefinition tests

To run just the tests for createUiDefinition.json file
```
npm --folder=sample-solution-template run createUi
```

## Running template tests

To run just the tests for template files (mainTemplate.json and any nested template json files included in the folder)
```
npm --folder=sample-solution-template run template
```

## Other miscellaneous files in this folder

buildpackage.zip, Gruntfile.js, CreateBuildPackage.ps1 and SetBranchNameVariable.ps1 files are NOT required to run tests locally. These are files used by an internal VSTS repository to run the mocha tests as part of a CI pipeline, the scope of which is beyond the solution template validation repository.