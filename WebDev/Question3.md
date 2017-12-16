# Question Three

Consider the following snippit of code:
```js
    var myObject = {
        foo: "bar",
        func: function() {
            var self = this;
            console.log("outer func:  this.foo = " + this.foo);
            console.log("outer func:  self.foo = " + self.foo);
            (function() {
                console.log("inner func:  this.foo = " + this.foo);
                console.log("inner func:  self.foo = " + self.foo);
            }());
        }
    };
    myObject.func();
```
Your task is to determine the output of this code and why, submit your solution as a word document.

Good Luck!


## Solving the question

The following are steps on how to submit a solution
 - Create a folder
 - Create files associated with the question you are solving in that folder
 - Once you have completed all the questions zip up the file and send it to me via messenger. 