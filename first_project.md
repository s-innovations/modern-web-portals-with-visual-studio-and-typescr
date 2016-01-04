# First Project

## TSD

From [DefinitelyTyped/tsd](https://github.com/DefinitelyTyped/tsd) a tool is provided that can be installed using the following command using the node package manager NPM.

`npm install tsd -g`

After installed one can pull in the type definitions for many popular JavaScript libraries using tsd.

`tsd install require --save`

In the above command the type definitions for RequireJS is installed which mean a `tsd.json` file is created to keep state informatio.

```
{
  "version": "v4",
  "repo": "borisyankov/DefinitelyTyped",
  "ref": "master",
  "path": "typings",
  "bundle": "typings/tsd.d.ts",
  "installed": {
    "requirejs/require.d.ts": {
      "commit": "0d66537e353802f996a3f67ca1b711f63835f9e7"
    }
  }
}

```
together with a folder `typings` where modules are installed as subfolders and a `tsd.d.ts` file that keep references to all the added files. In visual studio the tsd.d.ts file is not stricly needed due to the virtual TypeScript Project that finds all .ts and .d.ts files and helps with reference tracking. 
We will later explore how to properly use `tsd.d.ts` correctly as its how other typescript editors or if you want to compile from commandline using tsc (notice the difference, tsd vs tsc).