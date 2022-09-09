### Web pack Config
> Loading
### Testing ES6 modues

By default, Jest uses CommonJS notation. You have already seen it in the examples provided above. CommonJS modules are exported with `module.exports`: 
```javascript  
module.exports = someModule;
```
and imported with `require()`:
```javascript  
const someModule = require('./someModule');
```
So to make Jest understand ES6 native modules and notation like:
```javascript  
export default someModule;
```
and
```javascript  
import someModule from './someModule';
```
we need to *transform* all ES6 modules into CommonJS notation. Luckily it is very easy to automate this job with the use of [**Babel** compiler](https://babeljs.io/). 
All we'd need to do is to install Babel plugin:

```npm install --save-dev @babel/plugin-transform-modules-commonjs```

and create a new file in the project root directory called: `.babelrc` with the following code in it:

```javascript
{
  "env": {
    "test": {
      "plugins": ["@babel/plugin-transform-modules-commonjs"]
    }
  }
}
```

That's it! With Babel compiler configured, it is now possible to use `import` instead of `require` and write tests for ES6 modules.
