# Web Components Development

## Loading local modules

### 1) Use local npm modules
https://www.stefanjudis.com/today-i-learned/npm-install-supports-local-modules/

### 2) Enable Symlinks and deduplication in ES-DEV-SERVER

- es-dev-server.config.js

```javascript
module.exports = {
    port: 8000,
    open: true,
    watch: true,
    nodeResolve: true,
    appIndex: 'demo/index.html',
    plugins: [],
    moduleDirs: ['node_modules'],
    compatibility: "none",
    debug: false,
    preserveSymlinks: true,
    dedupe: true
};
```
- Symbolic links are needed when developing multible projects in parallel
- Deduplication is necessary because otherwise lit-hml does not work over multible projects