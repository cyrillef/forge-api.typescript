# Installation
> `npm install --save @types/forge-apis`

# Usage

After installing the definitions, there's no need to explicitly reference them if you use TypeScript >= 2.0 and ES6 modules - the transpiler will look for the definitions (so long as the typeRoots contains node_modules/@types) when you import the dependencies as ES6 modules.

You can install the type definitions separately without the Forge Node.js SDK, just in case you do not require the SDK client or you just need the typings for Viewer.js. See below for steps to manually reference the definitions.

- Prerequisites

  Install the type definitions for [THREE.js](https://www.npmjs.com/package/@types/three). If you'd like to reference this dependency by path instead of global types, change the reference comments in ```src/viewer.d.ts```.

- TypeScript 2.*

  If you have installed the types using NPM, to tell your transpiler to look for the type definitions of this package, specify the below in your ```tsconfig.json```:
  ```json
  {
    "typeRoots": ["node_modules/@types"],
    "types": ["forge-apis", "yourOtherTypes"]
  }
  ```
  Otherwise specify the path to our definitions in your ```tsconfig.json```:
  ```json
  "files": [    
    "path/to/forge-apis/index.d.ts"
  ]
  ```

- TypeScript >= 1.5

  To tell your transpiler to look for the type definitions of this package, specify the below in your ```tsconfig.json```:
  ```json
  {
    "compilerOptions": {
      ...
    },
    "include": [
       "path/to/forge-apis/index.d.ts"
   ]
  }
  ```

- All TypeScript Versions **(Ignore this if you have done any of the above)**

  Add reference comments at the top of your script:
  ```JavaScript
  /// <reference path="path/to/forge-apis/index.d.ts" />
  ```

# Publishing

1. Follow the project structure below:

| File | Purpose |
| --- | --- |
| index.d.ts | This indexes the type definitions of this package. |
| forge-apis-tests.ts | This contains sample code which tests the typings. This code does *not* run, but it is type-checked. |
| tsconfig.json | This allows you to run `tsc` within the package. |
| tslint.json | Enables linting. |
| src/*.d.ts  | Type definitions.  |
| README.md   | This file **but be sure to follow the template below*  |

2. Make sure ```README.md``` follow the template [here](https://github.com/dukedhx/DefinitelyTyped/blob/master/types/forge-apis/README.md)
3. Fork [DefinitelyTyped](https://github.com/DefinitelyTyped/DefinitelyTyped)
4. Commit the project to ```DefinitelyTyped/types/forge-apis``` and make a PR to [DefinitelyTyped](https://github.com/DefinitelyTyped/DefinitelyTyped)
5. After the PR is merged, the typings will be available as ```@types/forge-apis```

See details at https://github.com/DefinitelyTyped/DefinitelyTyped#make-a-pull-request

# Contents

This package contains type definitions for the following:
- Forge-apis
- Viewer.js
- Viewer.js Built-in Extensions

# Summary
This package contains type definitions for Forge Node.js SDK (https://github.com/Autodesk-Forge/forge-api-nodejs-client).

# Details
Files were exported from https://github.com/DefinitelyTyped/DefinitelyTyped/tree/master/types/forge-apis

Additional Details
 * Last updated: Fri, 11 Jan 2019 10:39:13 GMT
 * Dependencies: @types/three
 * Global values: none

# Credits
<a href="mailto:forge.help@autodesk.com">Forge Partner Development</a>
