## INSTALL PRETTIER

- install `npm i -D prettier`
- create .prettierrc file and paste this:

```json
{
    "semi": false,
    "trailingComma": "es5",
    "singleQuote": true,
    "printWidth": 80,
    "endOfLine": "lf",
    "tabWidth": 2
}
```

## NPM COMMAND PRETTIER

- add in package.json this command:

```json
{
    ...
    "script": {
        ...
        "prettier": "prettier --config .prettierrc \"src/**/*.ts\" --write",
        ...
    }
    ...
}
```

## INSTALL ESLINT

- install `npm i -D eslint`
- configure `npm init @eslint/config`
  - select: 
    - To check syntax, find problems, and enforce code style
    - JavaScript modules (import/export)
    - React (is use react), None of these (is use node.js)
    - Yes (use typescript)
    - Browser (if use a widget) or Node (if use a integration)
    - Use a popular style guide
    - Standard: https://github.com/standard/standard
    - File format in: JSON

## NPM COMMAND ESLINT

- add in package.json this command:

```json
{
    ...
    "script": {
        ...
        "lint": "eslint src --ext .js,.jsx,.ts,.tsx --ignore-pattern node_modules/",
        ...
    }
    ...
}
```

## CONFIG ESLINT RULES

```json
{
    ...
    "rules": {
        TODO
    }
}
```


## CONFIG PRETTIER WITH ESLINT

- install `npm i -D eslint-config-prettier eslint-plugin-prettier`
- in .eslintrc add with command:

```json
{
    ...
    "extends": [
        ...
        "prettier"
    ],
    ...
    "plugins": [
        ...
        "prettier"
    ],
    ...
    "rules": {
        ...
        "prettier/prettier": 2
    }
    ...
}
```





