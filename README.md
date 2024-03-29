# eslint-prettier-vscode

POC for es-lint prettier vscode setup

https://gist.github.com/bradtraversy/aab26d1e8983d9f8d79be1a9ca894ab4

1. Install ESLint & Prettier extensions for VSCode
   Optional - Set format on save and any global prettier options
2. Install Packages
   npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node

npx install-peerdeps --dev eslint-config-airbnb

3. Create .prettierrc for any prettier rules (semicolons, quotes, etc)
4. Create .eslintrc.json file (You can generate with eslint --init if you install eslint globally)
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

To disable all styling rules imposed by eslint, install eslint-config-prettier it turns off all styling rules , and place prettier in extends in last in eslintrc file. By this way styling rules will be handled by prettier separately and eslint can check linting errors.
