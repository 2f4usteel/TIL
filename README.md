# TIL
Something interesting?


* In Github, use `t` key binding to open the file finder inside the repo to find files quickly. 

* An alternative to `Array#join` is `Array*''` => `array = ['hello', 'world'] => array*'' => helloworld`

* In Ruby, By default, your code is always running a thread. Even if you don't create any new threads, there's always at least one main thread
```Thread.current == Thread.main``` returns true

* at_exit() - Converts block to a Proc object (and therefore binds it at the point of call) and registers it for execution when the program exits. If multiple handlers are registered, they are executed in reverse order of registration.
Ex: ```at_exit { puts "cruel world" }```

* The default `method_missing` actually lives in the Kernel module, which is included by Object