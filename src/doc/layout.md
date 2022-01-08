# Layout
Directory `src/layouts` is used package the app layouts like **Dashboard Layout**

The alias path for layout is `@src/layout`

e.g:
```js
   /*src/layout/dashboard-layout.tsx*/
   import React from 'react'
   import Sidebar from '@components/sidebar'
   import Navbar from '@components/navbar'
   import Footer from '@components/footer'
   
   /*props interface*/
   export interface IProps{
      readonly children: JSX.Element
   }
   export const Layout: React.FC<IProps> = ({children}) => {
       return (
           <div className="layout-container">
             <div className="nav-wrapper">
               <Navbar/>
             </div>
              <div className="content-wrapper">
               <Sidebar/>
               {children}
             </div>
             <div className="footer-wrapper">
               <Footer/>
             </div>
           <div>
       )
   }
```

## Views
A typical view serve as a combination of different components to come up with a presentable page.

To create a react page to be rendered, the pages are placed under `/src/views`

The alias path for views is `@views`

eg: Let's have a page `counter.tsx`, It's directory path will be `src/views/counter.tsx`

The **counter** page will be called like
```js
   /*src/config/routes.ts*/
   ...
   import Counter from '@views/counter'
   ...
```

After declaring you view file. Add it to the **views** package by exporting from `sr/views/index.tsx`
```js
    /*src/views/index.tsx*/
   export * from './counter';
```

## Components
Component are referenced under `src/components`

`@components` is the alias path for `src/components`

eg: let's have a component file `button.tsx`
This component director path will be `src/components/button.tsx`

Employing the component will be like
```js
   /*src/views/counter.tsx*/
   ...
   import Button from '@components/button';
```