# VSCode - ESLint, Prettier & Airbnb Setup

### 1. Install ESLint & Prettier extensions for VSCode

Optional - Set format on save and any global prettier options

### 2. Install Packages
```
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node
```

```
npx install-peerdeps --dev eslint-config-airbnb
```

### 3. Create .prettierrc for any prettier rules (semicolons, quotes, etc)

### 4. Create .eslintrc.json file (You can generate with eslint --init if you install eslint globally)

### 5. Create config eslint use npx `npx eslint --init`

#### 6.a .eslintrc.json
```
{
    "env": {
        "commonjs": true,
        "es2020": true,
        "node": true
    },
    "extends": ["airbnb", "prettier"],
    "plugins": ["prettier"],
    "rules": {
        "no-unused-vars": "warn",
        "no-console": "off",
        "indent": ["error", 4],
        "linebreak-style": ["error", "windows"],
        "quotes": ["error", "single"],
        "func-names": "off",
        "prefer-const": [
            "error",
            {
                "destructuring": "all"
            }
        ],
        "max-len": ["error", { "code": 200 }],
        "no-process-exit": "off",
        "object-shorthand": "off",
        "eol-last": "error",
        "class-methods-use-this": "off"
    }
}
```
#### 6.b .prettierrc
```
{
    "singleQuote": true,
    "tabWidth": 4,
    "endOfLine": "lf",
    "useTabs": false
}
```

### Note if you have an error "linebreaks to be 'LF' but found 'CRLF'" use this syntax bellow
```
npm run lint -- --fix
```
https://github.com/diegohaz/arc/issues/171

### Reference
* ESLint Rules - https://eslint.org/docs/rules/
* Prettier Options - https://prettier.io/docs/en/options.html
* Airbnb Style Guide - https://github.com/airbnb/javascript
