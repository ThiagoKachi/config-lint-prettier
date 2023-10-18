## Iniciar o ESLint
```
yarn create @eslint/config
```
	- To check syntax and find problems
	- JavaScript modules (import/export)
	- React
	- Does your project use TypeScript? no
	- Browser
 	- Use a popular style guide
  	- Airbnb: https://github.com/airbnb/javascript
	- JSON


<h3>Instalar libs necessárias</h3>

```
yarn add -D @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-import-resolver-typescript
```
<h3> Arquivo .eslint.json</h3>

```
{
    "env": {
        "browser": true,
        "es2021": true
    },
    "extends": [
      "airbnb",
      "plugin:react-hooks/recommended",
      "prettier"
    ],
    "parser": "@typescript-eslint/parser",
    "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module"
    },
    "plugins": [
      "@typescript-eslint",
      "prettier"
    ],
    "settings": {
      "import/resolver": {
        "typescript": {}
      }
    },
    "rules": {
      "prettier/prettier": "error",
      "react/react-in-jsx-scope": "off",
      "react/jsx-filename-extension": [1, { "extensions": [".tsx"] }],
      "react/jsx-props-no-spreading": "off",
      "react/jsx-no-bind": "off",
      "no-empty": ["error", { "allowEmptyCatch": true }],
      "import/extensions": [
        "error",
        "ignorePackages",
        {
          "ts": "never",
          "tsx": "never"
        }
      ],
      "import/order": [
        "error",
        {
          "groups": ["builtin", "external", "internal", "parent", "sibling", "index"],
          "alphabetize": {
            "order": "asc",
            "caseInsensitive": true
          },
          "newlines-between": "always"
        }
      ]
    }
}

```

## Iniciar o Prettier

```
yarn add -D prettier eslint-config-prettier eslint-plugin-prettier
```

<h4>Na raiz do projeto criar arquivo .prettierrc e colocar o código a seguir dentro</h4>

```
{
  "singleQuote": true
}
```
