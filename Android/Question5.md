# Question Five (Android)

Assume that the button UI element belongs to the main thread, why will the following code crash?

```java
    Button button = (Button) findViewById(.../* Pretend contains button ID*/)
    Thread thread = new Thread(new Runnable() {
        public void run() {
            button.setOnClickListener((View v) -> {
                // Stuff
            });
        }
    });
```


## Solving the question

The following are steps on how to submit a solution
 - Create a folder
 - Create files associated with the question you are solving in that folder
 - Once you have completed all the questions zip up the file and send it to me via messenger. 