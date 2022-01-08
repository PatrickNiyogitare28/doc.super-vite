
### Module

As Super Vite is based on typescript, Vite provides custom module resolvers.
This means you can use absolute imports with custom namespaces by default for the following modules:

You can define a new alias resolver in `vite.config.json` & `config-overrides.js`

For the jest to be able to recogonize the alias import, you should also define it under `jest.config.json`

```js
/* import common library */
import lib from '@common/<folder>/<lib>'
/* import component */
import Counter from '@components/counter'
/* import views/pages */
import CounterView from '@views/counter'
/* import interface */
import ICounterAction from '@interfaces/ICounterActionCounter'
/* import enum */
import ECounterEventType from '@enums/ECounterEventType'
/* import layout */
import DashboardLayout from '@layouts/DashboardLayout'
/* import assets */
import GithubIcon from '@assets/icons/github.png'
/* import enum */
import ECounterEventType from '@interfaces/ECounterEventType'

```