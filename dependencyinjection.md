## The pattern
Check for expected dependencies in classes

## Problems in Backbone Apps 

* Constructors are useful when they're instances
* Hard to organize
  * Use globals?  Bad.  Relying on globals is brittle.  They go against the grain of modularity (Dave Herman)

## Modules

Modules can help organize constructors.  Directory structure can help.  

Manuel dependency injection helps to organize your instances.

Keeping module system and instnace managmenet seperate helps organization.

## Organizing constructors and instances

Constructors form blueprint, instances compose the app while it's running.

(dependo: tool for visualizing js project via modules)

Expose single global to console to help with prototyping and debugging to see your instance dependency graph, which is harder to visualize.

## Refactoring

Remember: you can't refactor without tests!!

### Patterns

#### Application View

App instnance and collection are passed into views.  There are mixins to take care of this and check for dependencies.

Tests enforce the contract of dependencies.  You may see errors but they don't mean anything unless you write tests against them.


#### Single point of entry to access isntances

Avoid the need to use breakpoint debugging everywhere.

#### Long lived section views

#### SOLID Design Principles

OOP 101, but not necessarily JS 101.

* Single Responsibility Principle
* Open for extension, closed for mdoification
* Liskov Substitution
* Interface Segregation
* Dependency Inversion






