## Challenge 2: Creating queues, exchanges and bindings

### Objective

- You will learn about exchanges, bindings and routing keys in LavinMQ — building on the concepts you’ve learnt in the previous challenge.
- You will modify the producer you created in the previous challenge to fit the requirements of the notification system.

### Instructions

- Messages published to LavinMQ first land in an **exchange**. Exchanges are message routing agents — they forward the messages they receive to the correct queue.
- Exchanges use a combination of binding and routing keys to know the right queue to forward a message to.
- Recall in the overview we stated that the notification system will have three queues, one per Slack channel — **your task here** is to incorporate that into your producer.
- First, create a direct exchange `slack_notifications` and three queues: `hr_queue, marketing_queue, and support_queue`  ****in the producer. *Feel free to change the names to whatever you like.*
- Then bind each queue to the `slack_notifications` exchange using the corresponding binding keys: `hr, marketing, and support` respectively.
- Next, simulate a scenario where the producer publishes events from the `hr, marketing, and support` Slack channels with the **routing keys** `hr, marketing, and support` ****respectively.
- Using the bindings and routing keys above, the `slack_notifications` exchange will route messages from the `hr, marketing, and support` Slack channels to the `hr_queue, marketing_queue, and support_queue` queues respectively.
