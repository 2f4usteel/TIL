# TIL
Something interesting?


* In Github, use `t` key binding to open the file finder inside the repo to find files quickly. 

* An alternative to `Array#join` is `Array*''` => `array = ['hello', 'world'] => array*'' => helloworld`

* In Ruby, By default, your code is always running a thread. Even if you don't create any new threads, there's always at least one main thread
```Thread.current == Thread.main``` returns true