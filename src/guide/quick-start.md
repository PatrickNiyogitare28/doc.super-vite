# Getting started
Click `Use this template` to create the your own repo from the template

Before you can start developing your awesome application you need to install the project's dependencies. Make sure you have Node (>= 10.13.0)


### Development

Once all dependencies have been installed you can start development. To start a development server on [http://localhost:3000](http://localhost:3000) run:

```sh
$ npm run dev
```
or
```sh
$ yarn dev
```

### Production

To run your application in production make sure to run a build first:

```sh
$ npm run build
```
or
```sh
$ yarn build
```

And then start you application with a provided port number (defaults to 3000 if not provided):

```sh
$ PORT=8080 npm run start
```


This will render static HTML pages into `./out`


### Redux dev tool
The boiler plate has a configured global state management with redux dev tool.

### Getting started with states
- Define a state slice under `src/redux-slices` refer to `src/redux-slice/counter.slice.ts`

- Import the slice under `src/store` and declare your reducer

- To consume the state refer to `src/components/counter`

```js
import React from 'react'
import { useAppDispatch, useAppSelector } from '@store/hooks'
import {
    selectCount,
    decrement,
    increment,
    reset,
} from '@redux-slices/counter.slice'
import { ECounterEventType } from '@enums/ECounterEventType'
import styles from './styles.module.scss'

const CounterComponent = () => {
    const dispatch: any = useAppDispatch()
    const value: number = useAppSelector(selectCount)
    const handleAction = (action: ECounterEventType) => {
        switch (action) {
            case ECounterEventType.DECREMENT:
                dispatch(decrement())
                break
            case ECounterEventType.INCREMENT:
                dispatch(increment())
                break
            case ECounterEventType.RESET:
                dispatch(reset())
                break
        }
    }
    return (
        <div className={styles.counterContainer}>
            <div className={styles.counterWrapper}>
                <h2>
                    Counter: <label>{value}</label>
                </h2>
                <div className={styles.btnsWrapper}>
                    <button
                        onClick={() =>
                            handleAction(ECounterEventType.INCREMENT)
                        }
                    >
                        +
                    </button>
                    <button
                        onClick={() =>
                            handleAction(ECounterEventType.DECREMENT)
                        }
                    >
                        -
                    </button>
                    <button
                        onClick={() => handleAction(ECounterEventType.RESET)}
                    >
                        Reset
                    </button>
                </div>
            </div>
        </div>
    )
}

export default CounterComponent
```

### Todo
 The boiler plate incomming version will container a build in CLI to auto generate `components` and `views` plus connecting them to `store`

### LICENSE
[MIT LICENSED](https://github.com/PatrickNiyogitare28/super-vite/blob/master/LICENSE)
#### Maintainers
- patrickniyogitare28@gmail.com

