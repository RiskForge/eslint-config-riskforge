# RiskForge ESLint Standard Config

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Usage](#usage)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Usage

1. Install dependencies

   ```sh
   npm i --save-dev \
       @typescript-eslint/eslint-plugin \
       @typescript-eslint/parser \
       eslint \
       eslint-config-airbnb \
       eslint-config-airbnb-typescript \
       eslint-plugin-eslint-comments \
       eslint-plugin-import \
       eslint-plugin-jest \
       eslint-plugin-jsx-a11y \
       eslint-plugin-lodash-fp \
       eslint-plugin-promise \
       eslint-plugin-react \
       eslint-plugin-react-hooks \
       eslint-plugin-unicorn
   ```

2. Add eslint config to `package.json`

   ```json
   "eslintConfig": {
       "extends": "riskforge",
       "parserOptions": {
           "project": "./tsconfig.json"
       }
   }
   ```

3. Consider updating `.vscode/extensions.json`

   ```json
   {
     "recommendations": [
       "esbenp.prettier-vscode",
       "editorconfig.editorconfig",
       "dbaeumer.vscode-eslint"
     ]
   }
   ```

4. Consider updating your `.vscode/settings.json`

   ```json
   {
     "cSpell.words": ["riskforge"],
     "eslint.enable": true,
     "tslint.enable": false,
     "editor.formatOnSave": true,
     "editor.formatOnType": true,
     "editor.formatOnPaste": true,
     "editor.codeActionsOnSave": {
       "source.fixAll.eslint": true,
       "source.organizeImports": false
     },
     "eslint.lintTask.enable": false,
     "eslint.codeAction.showDocumentation": {
       "enable": true
     },
     "eslint.codeActionsOnSave.mode": "all",
     "eslint.packageManager": "npm",
     "eslint.run": "onType",
     "eslint.quiet": false,
     "eslint.probe": [
       "typescript",
       "markdown",
       "javascript",
       "typescriptreact",
       "javascriptreact"
     ],
     "files.exclude": {
       "**/.eslintcache": true
     },
     "search.exclude": {
       "**/.eslintcache": true
     },
     "javascript.preferences.importModuleSpecifier": "auto",
     "typescript.preferences.importModuleSpecifier": "auto",
     "javascript.preferences.quoteStyle": "single",
     "typescript.preferences.quoteStyle": "single",
     "editor.defaultFormatter": "esbenp.prettier-vscode",
     "[javascript]": {
       "editor.defaultFormatter": "dbaeumer.vscode-eslint"
     },
     "[javascriptreact]": {
       "editor.defaultFormatter": "dbaeumer.vscode-eslint"
     },
     "[typescript]": {
       "editor.defaultFormatter": "dbaeumer.vscode-eslint"
     },
     "[typescriptreact]": {
       "editor.defaultFormatter": "dbaeumer.vscode-eslint"
     },
     "eslint.lintTask.options": "--ext .js,.jsx,.ts,.tsx ."
   }
   ```
