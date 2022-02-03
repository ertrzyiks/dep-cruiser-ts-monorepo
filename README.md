# Dependency cruiser monorepo TS

Demo project using [dependency-cruiser](https://github.com/sverweij/dependency-cruiser/) in a monorepo
with typescript aliases not being resolved.



```
yarn
yarn test
```

Inspect modules.json and see that the aliased module is not properly resolved.
```json
{
  "source": "packages/a/src/index.ts",
  "dependencies": [
    {
      "module": "~core/test",
      "moduleSystem": "es6",
      "dynamic": false,
      "exoticallyRequired": false,
      "resolved": "~core/test",
      "coreModule": false,
      "followable": false,
      "couldNotResolve": true,
      "dependencyTypes": [
        "unknown"
      ],
      "matchesDoNotFollow": false,
      "circular": false,
      "valid": false,
      "rules": [
        {
          "severity": "error",
          "name": "not-to-unresolvable"
        }
      ]
    }
  ],
  "orphan": false,
  "valid": true
},
```
