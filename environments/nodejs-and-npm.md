# node.js and npm

Most of Iced Dev applications are written for the [node.js](http://nodejs.org/) platform.

To run an application using node.js, you will need:

* [node.js](http://nodejs.org/)
* [npm](https://github.com/npm/npm#super-easy-install) - a package manager that is bundled with node.js

## Dependency installation

Depenedencies are tracked in a manifest file named `package.json`.
This file is the central authority for all private and public dependencies of the application.

To install all the dependencies for the application, in the application directory, run the command:

```bash
npm install
```

This command will install the entire dependency tree and will probably take a while to run.

Once dependencies are installed, you are ready to run the application.

## Running the application

To run the application, in the application directory, you will need to run the command:

```bash
npm start
```

This command can be prefixed with private environment variables, such as database connections, as such:

```bash
DATABASE_URL=postgres://user:pass@localhost:5432 npm start
```

The application should now be running.

## Running tests

Tests can be run by being in the application directory and running the command:

```bash
npm test
```

If the tests fail, this command will exit with a status code of 1 and `npm` will report the error to you in the console.
It will also log failures to `npm-debug.log`

## Failures

All `npm` failures will be reported at the console and in the `npm-debug.log` file in the directory the command
was run in.
