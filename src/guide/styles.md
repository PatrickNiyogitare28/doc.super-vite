# Styles

Styling the **components** and app **views** can achieved by  **scss module**, **css** and **tailwind**

The boiler plate provide the template with all pre-configured and very ready to use.
## Css

The boiler plate supports scss and css module,
You can use `scss` to style your **views** and **components**

```js
/*.tsx*/
import { classNames } from 'classnames-generics'
import styles from './styles.module.scss'

return (
    <div className={styles.appContainer}>
      <p className={classNames(styles.wrapper)}>Scss styling</p>
    </div>
)
```
```css
/*.scss*/
  .appContainer{
      width: 100%;
      .wrapper{
          background: #ffe1ee;
      }
  }
```

## Tailwind

The boiler plate has a pre-configured `tailwind` styling frame work that can be used like.

```js
/*.tsx*/
...
return (
    <div className="mt-2">
      <p className="w-100">Tailwind styling</p>
    </div>
)
```