# @erquhart/browserify-fs

**Note:**
This is [browserify-fs](https://www.npmjs.com/package/browserify-fs) with updated dependencies to fix vulnerabilities.

Security updates from commits by @joseph184.

[fs](http://nodejs.org/api/fs.html) for the browser using [level-filesystem](https://github.com/mafintosh/level-filesystem), [level.js](https://github.com/maxogden/level.js) and [browserify](https://github.com/substack/node-browserify)

	npm install @erquhart/browserify-fs

![dat](http://img.shields.io/badge/Development%20sponsored%20by-dat-green.svg?style=flat)

## Usage

To use simply require it and use it as you would fs

``` js
var fs = require('browserify-fs');

fs.mkdir('/home', function() {
	fs.writeFile('/home/hello-world.txt', 'Hello world!\n', function() {
		fs.readFile('/home/hello-world.txt', 'utf-8', function(err, data) {
			console.log(data);
		});
	});
});
```

You can also make browserify replace `require('fs')` with browserify-fs using

	browserify -r fs:browserify-fs

Using the replacement you can browserify modules like [tar-fs](https://github.com/mafintosh/tar-fs) and [mkdirp](https://github.com/substack/node-mkdirp)!

Checkout [level-filesystem](https://github.com/mafintosh/level-filesystem) and [level.js](https://github.com/maxogden/level.js) to see which browsers are supported

## License

MIT
