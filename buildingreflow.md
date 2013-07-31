# Building Reflow

## Problem

There wasn't any good way to see what your website looked like responsively at desgin time.

## Solution

Adobe wanted to create a tool to express responsive intent.  Show exactly what a website would do as it scaled.

## Backbone

Reflow was built with Backbone.  Lots of iteration.  Built with Fluid (web wrapper) at first.  One week sprints.  Customer validations.  Research.  Evaluate at the end of the week.  That fast of a turnaround was not possible doing it without web technologies.  Using backbone also helped them understand the web dev space better.

## Prototyping

Write code in your prototype like you're writing it for production.  Test driven from day one.  

You prototype the things you don't think are possible.  Single leading reason this app was successful.

## Modularity: A Lesson in Refactoring

Require.js let the app scale in a way they couldn't otherwise.

## Multiple Inheritance

Used functional mixins.

`_.extend(BoxView.prototype, ViewMixin);`

## Views

Originally they had a lot of logic in the templates.  They broke down render methods to smaller views and actions in methods.  Then they wanted a way to deal with nested, hierarchial views.  Ended up having bloated views with bloated render methods even though they broke them down.  If they had to do it again, he'd use Marionette or Backbone layout manager.

## Templates

`_.template`: Never needed more than underscore.

All the logic for the templates happens in preparing the models very well (view models?)

## Collections

Wasn't support for mixed models. They had a canvas with a bunch of things rendered on it (and those things are different).  They came up with having a type on the model itself and having a view mappings function.

Filterable collection: they represent a different view on the data with filters.

## jQuery Plugins

They wrote a bunch of jQuery plugins for reflow.  They could write a plugin that would work on any dom and wrap it in a backbone view.  They can do the complicated things that the jQuery API makes easier and it can be used elsewhere.

## Testing

They TDD'd from day one.  You cannot make quality software without TDD.  You can't refactor without tests.  Sinon + Squire.  Sonar.  
