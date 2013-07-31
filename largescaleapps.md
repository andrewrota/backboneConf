Specialized objects
  Application
    App Modules
      Router
      Controllers
        Specialized Views
    Components
      take specialized behavior outside of views into reusable component
      forms, etc.
    Mixins
    Entities
    Config
  Modules
    (namespace, grouping of specific behaviors)
  Messaging Bus
    Request, command, pub/sub

Modules
  Each module has one entity and has its own controllers and routing events
  Also has its own requests and commands.  Nothing talks to the entities directly.
Controller
  Sole responsibilities to the views in its scope.
  Most of the code you write is in the controller, it is very procedural
  Understands view dependencies.  It listens and responds to view events.
  Controller is the true mediator.  Inserts views into regions, etc.
  Controller also understands shared modules in the application.
  Can decorate views, and views don't need to know they've been decorated
View
  Just has to manage the template (DOM)
  Views are complete transient.  Standarize its methods.
  Mixins here are traits (like focusable, selectable)
    Store view related behavior in its life cycle
  Don't instantiate a model directly in a view.  That should happen in a controller
  Specialized views: Item view, collection view, layout.
  Just listening to events from the DOM and the controller is responsible for doing somethign 
  Getting the right properties into the model.  If you want to have custom computed properties, etc.
Messaging Bus
  Controller needs to reach out to entities.
  Indirectly call something.
  MessageBus is used sort of like a repository controller.
  Interface between controller and entities.  Commands are set on Application object.
Folder Organization
  backbone
    app.js
    apps
      playlist
        playlist_app.js
          {router, instantiate controllers, etc.}
        list
          {templates, views, etc.}
        show
        edit
        new
      playlist_songs
      currently_playing
      album
    config
    entities
    components
    mixins
    base
