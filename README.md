To reproduce issue run:
```
yarn install
cd a
yarn start
```

**Expected:** No output
**Actual:**
```
jkim@jkim-2MBFH05 a (master) $ yarn start
yarn run v1.19.1
$ node index.js
/Users/jkim/code/next-css-peer-deps-issue-example/.pnp.js:5177
    throw firstError;
    ^

Error: Package "mini-css-extract-plugin@0.4.3" (via "/Users/jkim/Library/Caches/Yarn/v6/npm-mini-css-extract-plugin-0.4.3-98d60fcc5d228c3e36a9bd15a1d6816d6580beb8-integrity/node_modules/mini-css-extract-plugin/dist/index.js") is trying to require the package "webpack" (via "webpack") without it being listed in its dependencies (loader-utils, schema-utils, webpack-sources, mini-css-extract-plugin)
    at makeError (/Users/jkim/code/next-css-peer-deps-issue-example/.pnp.js:55:17)
    at Object.resolveToUnqualified (/Users/jkim/code/next-css-peer-deps-issue-example/.pnp.js:4915:17)
    at Object.resolveRequest (/Users/jkim/code/next-css-peer-deps-issue-example/.pnp.js:4986:31)
    at Function.Module._resolveFilename (/Users/jkim/code/next-css-peer-deps-issue-example/.pnp.js:5168:30)
    at Function.Module._load (/Users/jkim/code/next-css-peer-deps-issue-example/.pnp.js:5084:31)
    at Module.require (internal/modules/cjs/loader.js:692:17)
    at require (internal/modules/cjs/helpers.js:25:18)
    at Object.<anonymous> (/Users/jkim/Library/Caches/Yarn/v6/npm-mini-css-extract-plugin-0.4.3-98d60fcc5d228c3e36a9bd15a1d6816d6580beb8-integrity/node_modules/mini-css-extract-plugin/dist/index.js:7:16)
    at Module._compile (internal/modules/cjs/loader.js:778:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:789:10)
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```

