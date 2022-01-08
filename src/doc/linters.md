
## Linters

The boilerplate provides a couple of linters to help you keep an eye on code consistency and type safety. There are three linters: one for CSS, one for TypeScript and one for type safety. You can use each of them separately using the following commands:

With `npm`
```sh
$ npm run lint:css
$ npm run lint:ts
$ npm run lint:types
```


With `yarn`
```sh
$ yarn lint:css
$ yarn lint:ts
$ yarn lint:types
```

TIP: To get the most out of your linters install the corresponding (Stylelint, TSLint) plugins for your editor or IDE

## Prettier

Prettier helps you to enforce consistent (opinionated) code style. If possible, you can tell your editor to format you code when you save a file. If you are not able to do this, you can run prettier manually using:

With `npm`
```sh
$ npm run prettier
```

With `yarn`
```sh
$ yarn prettier
```