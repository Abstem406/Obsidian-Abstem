

Se utilizara un proyecto de Astro para ilustrar su configuración:

Astro:
```shell

	pnpm dlx create-astro@latest My-app --template with-tailwindcss --install --add react --git
```

Eslint + prettier:
```shell

	pnpm install --save-dev eslint prettier eslint-plugin-astro eslint-config-prettier eslint-plugin-prettier prettier-plugin-astro globals @eslint/js typescript-eslint
```


config files:

.prettierrc.mjs

```js


// prettier.config.js, .prettierrc.js, prettier.config.mjs, or .prettierrc.mjs

  

/**

 * @see https://prettier.io/docs/configuration

 * @type {import("prettier").Config}

 */

const config = {

    trailingComma: 'es5',

    tabWidth: 4,

    semi: false,

    singleQuote: true,

    plugins: ['prettier-plugin-astro'], // ← this line is mandatory

    overrides: [

        {

            files: '*.astro',

            options: { parser: 'astro' },

        },

    ],

}

  

export default config
```

 
eslint.config.mjs:
```js
// eslint.config.mjs

import globals from 'globals'

import pluginJs from '@eslint/js'

import tseslint from 'typescript-eslint'

import eslintPluginAstro from 'eslint-plugin-astro'

import eslintPluginPrettierRecommended from 'eslint-plugin-prettier/recommended'

  

/** @type {import('eslint').Linter.Config[]} */

export default [

    {

        ignores: ['**/.astro/**', 'dist/**', 'node_modules/**', '.git/**'],

    },

  

    { files: ['**/*.{js,mjs,cjs,ts,astro}'] },

    { languageOptions: { globals: { ...globals.browser, ...globals.node } } },

    pluginJs.configs.recommended,

    ...tseslint.configs.recommended,

    eslintPluginPrettierRecommended,

    ...eslintPluginAstro.configs.recommended,

]
```