# trial-typescript
play with typescript and node js

# TODO:

### Initialize node js program to create a package.json file, which will manage all dependencies:
- npm init --yes

### Install typescript as a development dependnecy in the node js program:
- npm install --save-dev typescipt 
or
- npm i typescript -D

(two commands above are identical)

### Give configuration below into tsconfig.json 

```json
{
    "compilerOptions": {
        "target": "es6",
        "module": "commonjs",
        "rootDir": "./src",
        "outDir": "./dist",
        "esModuleInterop": true,
        "strict": true
    },
    "include": ["src/**/*"],
    "exclude": ["node_modules", "**/*.spec.ts"]
}
```
compilerOptions: This section is used to specify various options to configure the behavior of the TypeScript compiler (tsc):

target: Specifies the ECMAScript target version for the compiled JavaScript. For example, "es6", "es2015", or an even newer version like "es2020". This determines which JavaScript features are available and how they are implemented in the output JavaScript.

module: Specifies the module system for the project. In Node.js, this is commonly set to "commonjs" since that is the module system used by Node.js. Other options include "amd", "es2015", "es2020", etc.

rootDir: This sets the root directory of your TypeScript source files. This is typically where your main application TypeScript files are located (e.g., a "src" directory).

outDir: Specifies the output directory for the compiled JavaScript files. It's a good practice to separate source files from compiled output (e.g., using a "dist" directory).

esModuleInterop: Allows default imports from modules with no default export. This setting is needed to import commonjs modules in a way that is compatible with es6 modules.

strict: Enables a wide range of type checking behavior that results in more robust code but can also be more verbose to write. This includes strictNullChecks, strictFunctionTypes, strictPropertyInitialization, and others.

include: Specifies an array of filename patterns that should be included in the program. These typically match the files that you want the TypeScript compiler to process.
src/**/*: Includes every file in the src directory and its subdirectories.

exclude: Specifies files or directories that the compiler should ignore. This is often used to avoid compiling test files or external libraries that do not need to be compiled.

node_modules: Excludes the node_modules directory to prevent TypeScript from trying to compile your installed packages.
**/*.spec.ts: Excludes all files that end with .spec.ts, which are typically test files.

### Handle warnings below:
- warning: in the working copy of 'package-lock.json', LF will be replaced by CRLF the next time Git touches it
- warning: in the working copy of 'package.json', LF will be replaced by CRLF the next time Git touches it