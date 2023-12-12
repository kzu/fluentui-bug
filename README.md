# FluentUI FluentCard + FluentDesignSystemProvider Bug

Removing the `FluentDesignSystemProvider` from `Routes.razor` or 
the `FluentCard` from `Home.razor` fixes the issue.

The exception when both are in place can be viewed in the developer 
tools: 

```
web-components-v2.5.16.min.js:21  Uncaught RangeError: Maximum call stack size exceeded
    at d (web-components-v2.5.16.min.js:21:88279)
    at b (web-components-v2.5.16.min.js:21:89056)
    at Kn (web-components-v2.5.16.min.js:21:89167)
    at Object.evaluate (web-components-v2.5.16.min.js:21:98645)
    at c.<anonymous> (web-components-v2.5.16.min.js:21:98786)
    at c.observe (web-components-v2.5.16.min.js:1:4877)
    at uo.handleChange (web-components-v2.5.16.min.js:16:93313)
    at c.notify (web-components-v2.5.16.min.js:1:3138)
    at c.call (web-components-v2.5.16.min.js:1:5462)
    at u.notify (web-components-v2.5.16.min.js:1:3138)
```
