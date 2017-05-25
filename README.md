# vue2-datepicker-demo

> A vue2-datepicker demo to reproduce a bug.

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## How to reproduce

``` bash
# create an empty Vue project
vue init webpack vue2-datepicker-demo

# install dependencies
cd vue2-datepicker-demo/
npm install

# add vue2-datepicker
npm install vue2-datepicker --save

# serve with hot reload at localhost:8080
npm run dev
```

Error in the output:

```
...
 error  in ./~/vue2-datepicker/src/datepicker/index.vue

Module build failed: Error: Couldn't find preset "latest" relative to directory ".../node_modules/vue2-datepicker"
...
```
