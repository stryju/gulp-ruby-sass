# [gulp](https://github.com/wearefractal/gulp)-ruby-sass [![Build Status](https://secure.travis-ci.org/sindresorhus/gulp-ruby-sass.png?branch=master)](http://travis-ci.org/sindresorhus/gulp-ruby-sass)

> Compile Sass to CSS with [Ruby Sass](http://sass-lang.com/install)

This is slower than [gulp-sass](https://github.com/dlmanning/gulp-sass), but more stable and feature-rich.


## Install

Install with [npm](https://npmjs.org/package/gulp-ruby-sass)

```
npm install --save-dev gulp-ruby-sass
```


## Example

```js
var gulp = require('gulp');
var sass = require('gulp-ruby-sass');

gulp.task('default', function () {
	gulp.src('src/app.scss')
		.pipe(sass({unixNewlines: true}))
		.pipe(gulp.dest('dist'));
});
```


## API

### sass(options)

#### options


##### sourcemap

Type: `Boolean`  
Default: `false`

Enable Source Maps.

**Requires Sass 3.3.0, which can be installed with `gem install sass --pre`**


##### trace

Type: `Boolean`  
Default: `false`

Show a full traceback on error.


##### unixNewlines

Type: `Boolean`  
Default: `false` on Windows, otherwise `true`

Force Unix newlines in written files.


##### check

Type: `Boolean`  
Default: `false`

Just check syntax, don't evaluate.


##### style

Type: `String`  
Default: `nested`

Output style. Can be `nested`, `compact`, `compressed`, `expanded`.


##### precision

Type: `Number`  
Default: `3`

How many digits of precision to use when outputting decimal numbers.


##### quiet

Type: `Boolean`  
Default: `false`

Silence warnings and status messages during compilation.


##### compass

Type: `Boolean`  
Default: `false`

Make Compass imports available and load project configuration (`config.rb` located close to the `Gruntfile.js`).


##### debugInfo

Type: `Boolean`  
Default: `false`

Emit extra information in the generated CSS that can be used by the FireSass Firebug plugin.


##### lineNumbers

Type: `Boolean`  
Default: `false`

Emit comments in the generated CSS indicating the corresponding source line.


##### loadPath

Type: `String|Array`

Add a (or multiple) Sass import path.


##### require

Type: `String|Array`

Require a (or multiple) Ruby library before running Sass.


##### cacheLocation

Type: `String`  
Default: `.sass-cache`

The path to put cached Sass files.


##### noCache

Type: `Boolean`  
Default: `false`

Don't cache to sassc files.


##### bundleExec

Type: `Boolean`  
Default: `false`

Run `sass` with [bundle exec](http://gembundler.com/man/bundle-exec.1.html): `bundle exec sass`.


## License

MIT © [Sindre Sorhus](http://sindresorhus.com)
