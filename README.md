# VSCode ESLint, Prettier &amp; Airbnb Style Setup

### 1. Install ESLint & Prettier extensions for VSCode

Optional - set format on save and any global prettier options

### 2. Install Packages
```
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node
```

```
npx install-peerdeps --dev eslint-config-airbnb
```

### 3. Create .prettierrc for any prettier rules (semicolons, quotes, etc)

```
{
  "printWidth": 80,
  "tabWidth": 2,
  "useTabs": false,
  "semi": true,
  "singleQuote": true,
  "trailingComma": "all",
  "bracketSpacing": true,
  "jsxBracketSameLine": false,
  "arrowParens": "avoid",
  "proseWrap": "always"
}
```

### 4. Create .eslintrc.json file (You can generate with eslint --init if you install eslint globally)

```
{
  "extends": ["airbnb", "prettier", "plugin:node/recommended"],
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": "error",
    "no-unused-vars": "warn",
    "no-console": "off",
    "func-names": "off",
    "no-process-exit": "off",
    "object-shorthand": "off",
    "class-methods-use-this": "off"
  }
}
```
