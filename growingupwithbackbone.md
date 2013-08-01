# Growing up with Backbone

## Structure

* Seperate your code from third party code.
* Linting and cleaning
* grunt-processhtml
  * Directives inside comments
* Source maps with javascript (debug in production)

## Modular

* Disconnected pieces that when put together for something
* Best choice right now is to use require and shim what you need.
  * But shimming is a lot of work on a big application
  * A configuration is not something you should have to maintain
* Package manager elevate dependencies to a higher level
* Build only what you reference
  * Script loader becomes resource loader
* Never modify the state of objects inside the root app object

## ES6

Define modules in es6.  Just add a transpiler.  ES6 --> AMD --> dist

## Web Components

A collective of five W3C recs: templates, decorators, custom elements, shadow dom, imports...and MDV.

See Backbone.Component.  And ScopedCSS.  

