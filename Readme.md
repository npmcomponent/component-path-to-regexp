*This repository is a mirror of the [component](http://component.io) module [component/path-to-regexp](http://github.com/component/path-to-regexp). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-path-to-regexp`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# Path-to-RegExp

  Turn an Express-style path string such as `/user/:name` into a regular expression.

## Usage

```javascript
var pathToRegexp = require('path-to-regexp');
```
### pathToRegexp(path, keys, options)

 - **path** A string in the express format, an array of such strings, or a regular expression
 - **keys** An array to be populated with the keys present in the url.  Once the function completes, this will be an array of strings.
 - **options**
   - **options.sensitive** Defaults to false, set this to true to make routes case sensitive
   - **options.strict** Defaults to false, set this to true to make the trailing slash matter.
   - **options.end** Defaults to true, set this to false to only match the prefix of the URL.

```javascript
var keys = [];
var exp = pathToRegexp('/foo/:bar', keys);
//keys = ['bar']
//exp = /^\/foo\/(?:([^\/]+?))\/?$/i
```

## Live Demo

You can see a live demo of this library in use at [express-route-tester](http://forbeslindesay.github.com/express-route-tester/).

## License

  MIT