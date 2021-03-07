# TIL
Something interesting?


* In Github, use `t` key binding to open the file finder inside the repo to find files quickly. 

* An alternative to `Array#join` is `Array*''` => `array = ['hello', 'world'] => array*'' => helloworld`

* In Ruby, By default, your code is always running a thread. Even if you don't create any new threads, there's always at least one main thread
```Thread.current == Thread.main``` returns true

* at_exit() - Converts block to a Proc object (and therefore binds it at the point of call) and registers it for execution when the program exits. If multiple handlers are registered, they are executed in reverse order of registration.
Ex: ```at_exit { puts "cruel world" }```

* The default `method_missing` actually lives in the Kernel module, which is included by Object

* To tunnel to your local web application using ssh by http://localhost.run/ No external depedency required(similar to ngrok)

* Concerns vs Service Objects --
```
- Services are operations/functions turned into classes.
- Concerns are mixins.

Concerns are essentially modules that allow you to encapsulate aspects of models into separate files to DRY up your code. The advantage is that they inherit from the ActiveSupport:Concern module, so you can access the ActiveRecord operations like validations and associations for the model in which the concern is included.

Service objects are used primarily to wrap a method in an object. These are useful in splitting logic up into small reusable components. These are often used for decoupling systems, and making systems easier to understand, because fundamentally what they do take you from a few many-purpose classes to many classes with a single purpose.

I have my concerns about concerns and tend to err on the side of caution with them.
```
