
# nwjs-nsis-compat-updater

> Fork from https://github.com/evshiron/nwjs-builder-phoenix

> Remove electron dependencies

`nsis-compat-updater` is an auto updater implementation for NW.js, inspired by `electron-updater`.

## API

### Imports

```javascript
import { NsisCompatUpdater } from 'nsis-compat-updater';
// Or
// const { NsisCompatUpdater } = require('nsis-compat-updater');
```

### Types

```typescript

interface IInstaller {
    arch: string;
    path: string;
    hash: string;
    created: number;
}

interface IUpdater {
    arch: string;
    fromVersion: string;
    path: string;
    hash: string;
    created: number;
}

interface IVersion {
    version: string;
    changelog: string;
    source: string;
    installers: IInstaller[];
    updaters: IUpdater[];
}

interface IStreamProgress {
    percentage: number;
    transferred: number;
    length: number;
    remaining: number;
    eta: number;
    runtime: number;
    delta: number;
    speed: number;
}

```
