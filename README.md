# weex-vue-bundle-util

This tool is for weex-vue-render to bundle the components and modules which you have used in your projects. You can just use the export function to analyse the used built-in components and modules, which returns a object includes `components` and `modules` fields. You just packing up them with the render-core (`weex-vue-render/dist/index.core.js`) in your project's entry file. By doing this you can pack up your render in the minimum size without all the irrelative codes of components and mdoules you haven't used in your project.

## how to use

just use the module as a function, pass in the webpack config and webpack it self, and run it before your compiling process.

```javascript
const webpack = require('webpack')
const config = require('your-projects-webpack-config.js')
const scan = require('weex-vue-bundle-util')
const { components, modules } = scan(webpack, config)
packYourProjectWith(components, modules)
// if you are using @ali/weex-vue-render, please pass a options with 'ali' set like the codes below.
// scan(webpack, config, { ali: true })
```

## components and modules

Here is a list about components and modules you can pack into your project. The aliweex only built packages list should be found in gitlab repo of @ali/weex-vue-render.

#### components

| npm module name | component name |
| --- | --- |
| weex-vue-a | a |
| weex-vue-input | input |
| weex-vue-slider | slider / slider-neighbor |
| weex-vue-switch | switch |
| weex-vue-textarea | textarea |
| weex-vue-video | video |
| weex-vue-web | web |

#### modules

| npm module name | API module name |
| --- | --- |
| weex-vue-animation | animation |
| weex-vue-clipboard | clipboard |
| weex-vue-dom | dom |
| weex-vue-event | event |
| weex-vue-geolocation | geolocation |
| weex-vue-global-event | globalEvent |
| weex-vue-modal | modal |
| weex-vue-navigator | navigator |
| weex-vue-storage | storage |
| weex-vue-stream | stream |
| weex-vue-websocket | websocket |
| weex-vue-webview | webview |

Enjoy happy building!