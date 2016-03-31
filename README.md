# grunt-contrib-htmlmin v1.1.0 [![Build Status: Linux](https://travis-ci.org/gruntjs/grunt-contrib-htmlmin.svg?branch=master)](https://travis-ci.org/gruntjs/grunt-contrib-htmlmin) [![Build Status: Windows](https://ci.appveyor.com/api/projects/status/sn73i2qggqeolnc2/branch/master?svg=true)](https://ci.appveyor.com/project/gruntjs/grunt-contrib-htmlmin/branch/master)

> Minify HTML



## Getting Started

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-contrib-htmlmin --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-contrib-htmlmin');
```




## Htmlmin task
_Run this task with the `grunt htmlmin` command._

*Issues with the output should be reported on the `htmlmin` [issue tracker](https://github.com/kangax/html-minifier/issues/new).*

### Options

See the `html-minifier` [options](https://github.com/kangax/html-minifier#options-quick-reference).

#### Example

```js
grunt.initConfig({
  htmlmin: {                                     // Task
    dist: {                                      // Target
      options: {                                 // Target options
        removeComments: true,
        collapseWhitespace: true
      },
      files: {                                   // Dictionary of files
        'dist/index.html': 'src/index.html',     // 'destination': 'source'
        'dist/contact.html': 'src/contact.html'
      }
    },
    dev: {                                       // Another target
      files: {
        'dist/index.html': 'src/index.html',
        'dist/contact.html': 'src/contact.html'
      }
    }
  }
});

grunt.registerTask('default', ['htmlmin']);
```


## Release History

 * 2016-03-31   v1.2.0   Updated to `html-minifier` to 1.4.0.
 * 2016-03-18   v1.1.0   Updated to `html-minifier` 1.3.0.
 * 2016-03-04   v1.0.0   Updated to `html-minifier` 1.2.0. Point main to task. Drop peerDeps.
 * 2015-10-28   v0.6.0   Updated to `html-minifier` 1.0.0.
 * 2015-09-25   v0.5.0   Updated to `html-minifier` 0.8.0.
 * 2015-02-06   v0.4.0   Updated to `html-minifier` 0.7.0.
 * 2014-05-05   v0.3.0   Drop Node.js 0.8 support. Updated to `html-minifier` 0.6.0.
 * 2014-02-09   v0.2.0   Rewrite task. Drop concat support.
 * 2013-04-06   v0.1.3   Fail target when minify encounters an error.
 * 2013-04-05   v0.1.2   Update `html-minifier` which fixes IE conditional comments and prefixed HTML elements `<ng-include>`, `<ng:include>`.
 * 2013-02-18   v0.1.1   First official release for Grunt 0.4.0.
 * 2013-01-30   v0.1.1rc7   Updating grunt/gruntplugin dependencies to rc7. Changing in-development grunt/gruntplugin dependency versions from tilde version ranges to specific versions.
 * 2013-01-09   v0.1.1rc5   Updating to work with grunt v0.4.0rc5. Switching to `this.filesSrc` API.
 * 2012-11-01   v0.1.0   Initial release.

---

Task submitted by [Sindre Sorhus](http://github.com/sindresorhus)

*This file was generated on Thu Mar 31 2016 17:12:08.*
