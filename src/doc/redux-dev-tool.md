
# Redux dev tool
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