# vue-typer
Vue component that simulates a user typing, selecting, and deleting text.

## Demo
TODO
Link here (also add link to github repo description at the top)
<p align="center"><img src="" alt="VueTyper demo gif"/></p>

## Getting Started

### Prerequisites
- Vue v2.x ([See here for migration instructions from Vue 1.x to 2.x.](https://vuejs.org/v2/guide/migration.html))

### Install
TODO: 
VueTyper is available on npm:
```
npm install --save vue-typer?
```

## Usage
You may register VueTyper either globally or locally. [What's the difference? See the Vue documentation here.](https://vuejs.org/v2/guide/components.html#Registration)

#### Local Registration
1. Import the VueTyper component directly from your Vue component file:
```javascript
import { VueTyper } from 'vue-typer'
// or
var VueTyper = require('vue-typer').VueTyper
```

2. Register it as a local component in your Vue component options:
```javascript
var MyComponent = {
  // ...
  components: {
    VueTyper  // ES6 property shorthand + Vue should automatically dasherize the key for us
  }
}
```

3. Use vue-typer in your Vue component's template:
```html
<vue-typer text='Hello World! I was registered locally!'></vue-typer>
```

#### Global Registration
1. Import the VueTyper plugin in your application entry point:
```javascript
import VueTyperPlugin from 'vue-typer'
// or
var VueTyperPlugin = require('vue-typer').default
```

2. Register the VueTyper plugin with Vue
```javascript
Vue.use(VueTyperPlugin)
```

3. Now you can freely use vue-typer in any Vue component template:
```html
<vue-typer text='Hello World! I was registered globally!'></vue-typer>
```

## Props
TODO

#### PropName
- type: `String | Array`
- required

Description of prop here

```html
Code sample of using prop here
```

## Events
TODO

#### EventName
- Event data:
  - (String) word that finished typing
```html
Code sample of attaching event listener in template
```
```javascript
Code sample of event handler function
```

## Styles
TODO

To keep the separation of concern between component code and styles, VueTyper can be fully styled through CSS (as opposed to props):

```css
CSS selector format here
```

## Changelog
TODO

## TODO
- Update to stable releases of:
  - [ ] webpack
  - [ ] webpack-dev-server
  - [ ] extract-text-webpack-plugin
- [ ] Revisit community discussions around the best way to obtain deterministic hashes so we can remove HashedModuleIdsPlugin
- Potential features (contributions are welcome!):
  - [ ] start typing only when VueTyper is on-screen; potentially pause typing when off-screen
  - [ ] smarter typing algorithm: erase only up to the longest common starting substring
  - [ ] is it worth it to eliminate time-drifting from setInterval? If so, it could be a self-correcting interval (implemented as a series of timeouts)

## License

[MIT](http://opensource.org/licenses/MIT)

Copyright (c) 2016 Chris Nguyen. All rights reserved.
