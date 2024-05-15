## Challenge 3: Running three consumers

### Objective

- You will learn how to create a 1-to-1 mapping between queues and consumers.
- You will modify the consumer you created in the first challenge to fit the requirements of the notification system.

### Instructions

- The last thing we need to have a working notification system is to bind a consumer to each queue. Ideally, each consumer will receive messages from the queue it’s bound to and broadcast the message received to the users . For brevity’s sake we won’t be doing all that. A consumer will receive messages and just log it to the console.
- Because we have three queues we will be needing three consumers. Creating a script from scratch for each consumer will be redundant. Instead, modify your existing consumer script to accept command line arguments.
- Modify the consumer script to accept one of three command line arguments: `hr, marketing, and support`  — the consumer will then bind to the `hr_queue, marketing_queue, or support_queue` at runtime, depending on the argument passed.
