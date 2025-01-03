# OTHER INSTRUCTIONS - THESE INSTRUCTIONS HAVE BEEN USED TO SETUP THE PROJECT FROM SCRATCH

### create a root folder on your laptop for backend codebase (e.g. vcs-backend)

### install `NVM, NODE JS, NPM` on your laptop as per need - verify it using (note: we are using nodejs - 20 as of now)

nvm --version

node --version

npm --version

### instead of using NPM, we will use `YARN` (this is just for our convenience, but you can also use `NPM` if you want). Ensure you have `YARN` installed on your laptop - verify it using

yarn --version

### instantiate a nodejs project, this will create `package.json` file

yarn init -y

### install dependencies and dev-dependencies - refer [TECHNOLOGY-STACK](TECHNOLOGY-STACK.md)

#### install dev-dependencies for typescript (note: some dependencies are based on nodejs version)

yarn add -D typescript ts-node @types/node @tsconfig/node20

#### create typescript configuration file `tsconfig.json` using following command and edit the contents as per need (or copy paste the whole `tsconfig.json` file from this git)

#### NOTE: if you see any error in `tsconfig.json` like `no inputs were found in config file` - create a src folder and a sample `sample.ts` file, refer: https://stackoverflow.com/a/41211721

tsc --init

#### install dev-dependencies for jest

yarn add -D jest ts-jest @types/jest

#### create jest configuration file `jest.config.js` file using following command and edit the contents as per need (or copy paste the whole `jest.config.js` file from this git). Note later we have convert `jest.config.js` to `jest.config.ts` file

yarn create jest

#### create `src/samples/sample.ts`, `tests/samples/sample.test.ts` and `tests/tsconfig.json` files

#### update `package.json` with `test` target script and test it using `yarn run test`

#### install dev-dependencies for eslint, this will create `eslint.config.mjs` file

yarn create @eslint/config OR npm init @eslint/config@latest

#### install dev-dependencies for eslint jest

yarn add -D eslint-plugin-jest

#### update the contents of `eslint.config.mjs` as per need (or just copy paste the whole `eslint.config.mjs` file from this git)

#### install dev-dependencies for prettier and prettier-eslint

yarn add -D eslint-plugin-prettier eslint-config-prettier

yarn add -D prettier

#### install vscode extension: `prettier-code formatter` and update vscode settings: `default formatter` and `format on save`

#### update package.json - add script target for lint

#### run from terminal and you will see bunch of lint errors, fix it.

yarn run lint or npm run lint

yarn run lint --fix

#### Note: if you are getting module-not-defined error on jest config file, refer this: https://stackoverflow.com/questions/64914701/jest-module-not-defined

#### Note: if you are getting `Expect must have a corresponding matcher call  jest/valid-expect` error on test file, refer this: https://stackoverflow.com/questions/63191622/jest-and-eslint-expect-must-have-a-corresponding-matcher-call

#### Github Actions Workflow

TBD
