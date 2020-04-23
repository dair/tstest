# How to run multiple files in node.js?

I have this structure here. What I am trying to is to run all this together.

```
tsc && node dist/first.js
```

But of course it fails:

```
console.log("Hello" + someVar.toString());
                      ^

ReferenceError: someVar is not defined
    at Object.<anonymous> (/Users/dair/Documents/src/test/tstest-git/dist/first.js:2:23)
    at Module._compile (internal/modules/cjs/loader.js:1147:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1167:10)
    at Module.load (internal/modules/cjs/loader.js:996:32)
    at Function.Module._load (internal/modules/cjs/loader.js:896:14)
    at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:71:12)
    at internal/main/run_main_module.js:17:47
```

**The question**: how to run this?



**Update**: got it. It is needed to write
```
import { someVar } from 'second'
```

for this to work.
Makes sense.
