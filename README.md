# `Commit Message Validator`

A tool for validate commit message.

## `usage`

This tool dependencies on `yorkie`.

So we can add follow code in `package.json`:

```json
{
    "gitHooks": {
        "commit-msg": "cmv"
    }
}
```

## `Rules`

Every commit message must match the following `RegExp`:

```js
const regexp = /^(revert: )?(feat|fix|docs|style|refactor|perf|test|workflow|build|ci|chore|types|release|merge)(\(.+\))?: .{1,50}/;
```

## `Types`

| type     | description            |
| -------- | ---------------------- |
| feat     | new feature            |
| fix      | fix bug                |
| docs     | documentation          |
| style    | styles                 |
| refactor | refactor               |
| test     | add or change test     |
| chore    | daily change           |
| perf     | imporove performance   |
| workflow | workflow change        |
| build    | build                  |
| ci       | continuous integration |
| merge    | code merge             |
| types    | typescript declaration |
| release  | version update         |

## `Example`

We can use following format with commit message:

```
`type(socpe): commit message`
```

There are some examples:

```
//feature
feat(package): add a new function.

//daily change
chore(root): update package.json.
```
