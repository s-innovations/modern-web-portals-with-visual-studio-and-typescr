# First Project

## Bower, NPM and Grunt



## Si-Portal
Installing the [S-Innovtions Portal Framework](https://github.com/s-innovations/S-Innovations.PortalFramework) using bower will pull in knockout,requires and other utility libraries needed to create web portals using the techniques and design principals of this book.

`bower install s-innovations/s-innovations.portalframework --save`

The typescript definitions are not pulled in as a dependency as of now, but using TSD described below will cover this.

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
together with a folder `typings` where modules are installed as sub-folders and a `tsd.d.ts` file that keep references to all the added files. In visual studio the tsd.d.ts file is not strictly needed due to the virtual TypeScript Project that finds all .ts and .d.ts files and helps with reference tracking. 
We will later explore how to properly use `tsd.d.ts` correctly as its how other typescript editors or if you want to compile from commandline using tsc (notice the difference, tsd vs tsc).
