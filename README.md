# doc.super-vite
The super-vite documentation

## Quick start

✅ clone repo 

✅ run `yarn install`

## Running 
```sh
$ yarn dev
```

## Building
```sh
$ yarn build
```

### Adding a page

To be able to add a guide to this documentain

Create an `md` file add locate it under `/src/doc`

Then locate to be able to render the documentation file slightly modify  `src/.vuepress/config` to add in your own file name

```js
...
 sidebar: {
      '/doc/': [
        {
          title: 'Documentation',
          collapsable: false,
          children: [
            '',
            'quick-start',
            'layout',
            'routing',
            'linters',
            'tests',
            'modules',
            'styles',
            'redux-dev-tool',
            'i18n',
            'services',
            'helpers',
            'enums',
            'interfaces',
            'types',
            'assets',
            'plugins'
          ]
        }
      ],
    }
```

## Contributing

We welcome contribution via either PRs or Issues and ideas as well. Before contributing make sure you revise our [CODE OF CONDUCT](https://github.com/PatrickNiyogitare28/doc.super-vite/blob/master/CODE_OF_CONDUCT.md)

## Maintainer 

patrickniyogitare28@gmail.com

## LICENSE

[MIT](https://github.com/PatrickNiyogitare28/doc.super-vite/blob/master/LICENSE)