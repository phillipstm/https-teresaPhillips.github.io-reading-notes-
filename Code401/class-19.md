#  AWS: Events

## AWS SQS vs SNS

<https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5>

SQS=Simple Queue Service
SNS=Simple Notification Service

What is the difference betweeen SQS and SNS?

SNS is a publish-subscribe service and the other is a queing service. If you want unknown number and type of subscribers to receive messages, you need SNS.

SQS messages are not pushed to receivers and can’t be received by multiple receivers at the same time. In SQS the message delivery is guaranteed but in SNS it is not.

What are some use cases for both SNS and SQS?

**Persistence**
SQS : Messages are persisted for some duration is no consumer available. The retention period value is from 1 minute to 14 days. The default is 4 days.
SNS : No persistence. Whichever consumer is present at the time of message arrival, get the message and the message is deleted. If no consumers available then the message is lost.

**Consumer Type**
SQS : All the consumers are supposed to be identical and hence process the messages in exact same way.
SNS : All the consumers are (supposed to be) processing the messages in different ways.

**Use Cases**
**Choose SNS if:**

You would like to be able to publish and consume batches of messages.
You would like to allow same message to be processed in multiple ways.
Multiple subscribers are needed.
**Choose SQS if:**

You need a simple queue with no particular additional requirements.
Decoupling two applications and allowing parallel asynchronous processing.
Only one subscriber is needed.
We can design fanout pattern by using both SNS and SQS. In this pattern, a message published to an SNS topic is distributed to multiple SQS queues in parallel.

Summary
SQS is mainly used to decouple applications. SNS distributes several copies of message to several subscribers.

## AWS SNS and SQS

<https://www.youtube.com/watch?v=mXk0MNjlO7A>

Describe how to use SQS and SNS in a “fanout” pattern.

SNS-It is the way a message is sent it can fanout to differnt types as SQS, Lamda, or Email.

SQS-Queue needs to be polled to discover new events. Processed by a single consumer.

Explain how “push notifications” work, using SNS.

It is able to push a payload to several services at once. Like a transaction, push notice to consumer, vendor, ananytics, Lamda etc..

## SQS and SNS Basics

<https://www.youtube.com/watch?v=UesxWuZMZqI>

How might a large scale, distributed application make use of a Queue system like SQS?

You handle functions and notifications in SQS which are easy to load balance using Lambda.

## Bookmark and Review

### SNS Javascript SDK

**latest version**
<https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/index.html>

<https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SNS.html>

### SQS Javascript SDK

**latest version**
<https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/index.html>

<https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SQS.html>

### Things I want to know more about


📚 MY RECOMMENDED READING LIST FOR SOFTWARE DEVELOPERS📚[Be A Better Dev-youTube]
Clean Code - <https://amzn.to/37T7xdP>
Clean Architecture - <https://amzn.to/3sCEGCe>
Head First Design Patterns - <https://amzn.to/37WXAMy>   
Domain Driver Design - <https://amzn.to/3aWSW2W>
Code Complete - <https://amzn.to/3ksQDrB>
The Pragmatic Programmer - <https://amzn.to/3uH4kaQ>  
Algorithms - <https://amzn.to/3syvyP5>
Working Effectively with Legacy Code - <https://amzn.to/3kvMza7>
Refactoring - <https://amzn.to/3r6FQ8U>
