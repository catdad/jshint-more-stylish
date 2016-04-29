# jshint-more-stylish

[![Build][1]][2] [![Downloads][7]][8] [![Version][9]][8]

[1]: https://travis-ci.org/catdad/jshint-more-stylish.svg?branch=master
[2]: https://travis-ci.org/catdad/jshint-more-stylish

[7]: https://img.shields.io/npm/dm/jshint-more-stylish.svg
[8]: https://www.npmjs.com/package/jshint-more-stylish
[9]: https://img.shields.io/npm/v/jshint-more-stylish.svg

![](assets/screenshot.png)

Compared to the default reporter:

![](assets/screenshot-default-reporter.png)


## Install

```
$ npm install --save-dev jshint-more-stylish
```

## Usage

### JSHint CLI

```
$ jshint --reporter=node_modules/jshint-more-stylish file.js
```

### [gulp-jshint](https://github.com/spalger/gulp-jshint)

```js
gulp.task('default', function () {
	gulp.src(['file.js'])
		.pipe(jshint('.jshintrc'))
		.pipe(jshint.reporter('jshint-more-stylish'));
});
```

### [grunt-contrib-jshint](https://github.com/gruntjs/grunt-contrib-jshint)

```js
grunt.initConfig({
	jshint: {
		options: {
			reporter: require('jshint-more-stylish')
		},
		target: ['file.js']
	}
});

grunt.loadNpmTasks('grunt-contrib-jshint');
grunt.registerTask('default', ['jshint']);
```
