# karma-nodeunit
Adapter for the Nodeunit testing framework.  For more information on Karma see the [homepage](http://karma-runner.github.com).

Currently supports Karma 0.10.x

[![Build Status](https://travis-ci.org/karma-runner/karma-nodeunit.svg)](https://travis-ci.org/karma-runner/karma-nodeunit)
[![Dependency Status](https://gemnasium.com/karma-runner/karma-nodeunit.svg)](https://gemnasium.com/karma-runner/karma-nodeunit)

## Usage
1. `npm install karma-nodeunit` or add it to your `package.json`.
2. Include nodeunit and the karma adapter in your `karma.conf.js`:

```js
frameworks = ['nodeunit'];

files = [
  'lib/*.js' // files to test
  'test/*.js' // test files
];
browsers = ['Chrome'];
```

3. Write your nodeunit tests:

```js
nodeunit.run({
  testSomething: function(test) {
    test.expect(1);
    test.ok(true, "this assertion should pass");
    test.done();
  },
  'test something else': function(test) {
    test.ok(false, "this assertion should fail");
    test.done();
  }
});
```

## Release history
* 2014-08-29    v0.2.0    Fix #12, #16.  Work with karma v0.12
* 2013-11-18    v0.1.1    Fix #8, #9, and #10. Bump nodeunit to v0.8.2.
* 2013-10-11    v0.1.0    Migration to karma 0.10.x. Travis CI.
* 2013-03-21    v0.0.3    Linked to official karma plugins
* 2013-03-21    v0.0.2    Usage examples, renamed from https://github.com/testacular/testacular-jasmine
