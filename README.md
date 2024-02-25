# nw-vue-devtools-5

Vue DevTools (v5) for NW.js

This is a, hard coded, extracted copy of the last release of Version 5 of the Vue DevTools Chrome Extension. It is modified to work with NW.js. Version 6, at the time of writing is buggy. So I'm publishing this as an easy way to get to version 5. If you are in the future you are probably better off using [nw-vue-devtools-prebuilt](https://github.com/DimPaDev/nw-vue-devtools-prebuilt) (assuming the bugs in Vue DevTools get fixed).


## Instructions

1. `npm install nw-vue-devtools-5`
1. Add this to your `package.json` of your NW.js app:
   ```js
   "chromium-args": "--load-extension='./node_modules/nw-vue-devtools-5/extension'"
   ```
1. Vue.js must be in use in your app, and cannot be minified (`vue.js` not `vue.min.js`).

You may need to add `Vue.config.devtools = true;` to your `main.js` file.

If you are using `nwjs-builder-phoenix` then add in `"chromium-args"` to your `package.json` `build.strippedProperties` array ([more info](https://github.com/evshiron/nwjs-builder-phoenix/blob/master/docs/Options.md#build---buildconfig)).
