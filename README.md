# style-guide for Next v15 & TW v3

A Next/TS/TW style guide based on the retired Vercel Style Guide. **_This is for Next v15 and TW v3 as different setup is needed for newer versions of Next and TW_**.

This is only a framework to bootstrap linting and code formatting. More-than-likely more work will need to be done to get this working in a codebase. This style guide was created because Vercel has retired their style guide and have not updated it to work with the new eslint flat config.

## Eslint

This is based off the new eslint flat config. Use the `eslint.config.js` file inside the root of your project. This file utilizes many of the below packages recommend settings as well as custom rules.

The following eslint packages & plugins need installed as dev dependencies:

-   @eslint/eslintrc
-   @eslint/js
-   @next/eslint-plugin-next,
-   eslint
-   eslint-config-prettier
-   eslint-import-resolver-typescript
-   eslint-plugin-eslint-comments
-   eslint-plugin-import
-   eslint-plugin-jsx-a11y
-   eslint-plugin-react
-   eslint-plugin-react-hooks
-   eslint-plugin-tailwindcss
-   eslint-plugin-tsdoc
-   eslint-plugin-unicorn
-   typescript-eslint

## Prettier

Use the `prettier.config.js` & `.prettierignore` file in the root of your project.

The following Prettier packages & plugins need installed as dev dependencies:

-   prettier
-   prettier-plugin-packagejson
-   prettier-plugin-tailwindcss

## Package.json
Make sure to add `"type": "module"` to your package.json. You may need to make sure all of your config & other files are in ESM syntax but since Next v14 this is now supported.

## Typescript config

Make sure to include your config files in the `tsconfig.json`:

```
 "include": [
        "next-env.d.ts",
        "**/*.ts",
        "**/*.tsx",
        "**/*.config.js"
    ]
```

<hr />

```
pnpm i @eslint/eslintrc @eslint/js @next/eslint-plugin-next eslint eslint-config-prettier eslint-import-resolver-typescript eslint-plugin-eslint-comments eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react eslint-plugin-react-hooks eslint-plugin-tsdoc eslint-plugin-unicorn typescript-eslint prettier prettier-plugin-packagejson prettier-plugin-tailwindcss eslint-plugin-tailwindcss -D
```

## Future Additions

### eslint/css
Eslint now supports linting [CSS](https://eslint.org/blog/2025/02/eslint-css-support/) with the [@eslint/css](https://www.npmjs.com/package/@eslint/css) plugin but there are still bugs in installing it w/ pnpm and yarn as of the time of writing this. There are also a bunch of rules in the feature request pipeline. The plugin supports TW syntax as well but there is the following issue: 'The Tailwind syntax doesn’t currently provide for the theme() function. This is a limitation of CSSTree that we hope will be resolved soon.' 

Once these initial quirks are worked out, this plugin will be fully incorporated into this style guide. 