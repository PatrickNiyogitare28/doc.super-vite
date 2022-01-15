# Services

The boiler plate provides the **services** directory for handling service based computations 
> A function that calls a third party API is one of the functions that can be handled under services

The alias for services `src/services` is `@services`

Example

```ts
/*src/services/counter.service.ts*/
const onIncrement = (count: number): Number => {
    return count++;
}

const onDecrement = (count: number): Number => {
    return count--;
}

const onReset = (): Number => {
    return 0;
}

export const counterService = { onIncrement, onDecrement, onReset }
```

After building your service, the services are packaged together under `src/services/index.ts`
```ts
/*src/services/index.ts*/
export * from './counter.service';
```

## Utilizing a service

Using a service in a view
```tsx
/*src/views/counter.tsx*/
import {counterService} from '@services';
...
const onIncrement = () => {
    counterService.onIncrement(1);
}
...
```