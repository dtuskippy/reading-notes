# Class-19 Reading Notes

It's a topic that my team is considering for Lab 14, and a topic certainly relevant to Lab 19.  

## [AWS SQS vs SNS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)

1. What is the difference betweeen SQS and SNS?
    * SNS is a distributed publish-subscribe service.
    * SQS is distributed queuing service.
2. Differences between SQS and SNS in greater detail:
    * Entity Type
       * SQS : Queue (similar to JMS, MSMQ).
       * SNS : Topic-Subscriber (Pub/Sub system).
    * Message consumption
      * SQS : Pull Mechanism — Consumers poll messages from SQS.
      * SNS : Push Mechanism — SNS pushes messages to consumers.
    * Persistence
      * SQS : Messages are persisted for some duration if no consumer available. The retention period value is from 1 minute to 14 days. The default is 4 days.
      * SNS : No persistence. Whichever consumer is present at the time of message arrival, gets the message and the message is deleted. If no consumers available then the message is lost.
      * In SQS the message delivery is guaranteed but in SNS it is not.
    * Consumer Type
      * SQS : All the consumers are supposed to be identical and hence process the messages in exact same way.
      * SNS : All the consumers are (supposed to be) processing the messages in different ways.
2. What are some use cases for both SNS and SQS?
    * SNS
      * You would like to be able to publish and consume batches of messages.
      * You would like to allow the same message to be processed in multiple ways.
      * Multiple subscribers are needed.
    * SQS
      * You need a simple queue with no particular additional requirements.
      * Decoupling two applications and allowing parallel asynchronous processing.
      * Only one subscriber is needed.
    * You can design a fanout pattern by using both SNS and SQS. 
        * In this pattern, a message published to an SNS topic is distributed to multiple SQS queues in parallel.
3. SNS in greater detail:
    * Amazon SNS is a fast, flexible, fully managed push notification service that lets you send individual messages or to bulk messages to large numbers of recipients. Amazon SNS makes it simple and cost effective to send push notifications to mobile device users, email recipients or even send messages to other distributed services.
    * SNS is a distributed publish-subscribe system. Messages are pushed to subscribers as and when they are sent by publishers to SNS.
    * SNS supports several end points such as email, sms, http end point and SQS. If you want unknown number and type of subscribers to rece  ive messages, you need SNS.
    * With Amazon SNS, you can send push notifications to Apple, Google, Fire OS, and Windows devices , as well as to Android devices in China with Baidu Cloud Push. You can use SNS to send SMS messages to mobile device users in the US or to email recipients worldwide.
4. SQS in greater detail:
    * Amazon SQS is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.
    * SQS is a distributed queuing system. Messages are not pushed to receivers. Receivers have to poll SQS to receive messages. Messages can be stored in SQS for short duration of time (max 14 days).
    * Messages can’t be received by multiple receivers at the same time. Any one receiver can receive a message, process and delete it. Other receivers do not receive the same message later. Polling inherently introduces some latency in message delivery in SQS unlike SNS where messages are immediately pushed to subscribers.
  

## [AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)

1. Describe how to use SQS and SNS in a “fanout” pattern.
    * A message is delivered to multiple subscribers, some of which are other SNS services, and some of which are SQS services -- example credit card transaction had 3 subscribers:
      * Lamba function which acts as SNS sending customer notifications; best effor delivery, so potential to lose message before receipt.
      * Transaction analytics queue, e.g. dashboard to poll information at later time; once poll occurs, message deleted; message gauranteed.
      * Transaction fraud detection queue -- once poll occurs, message deleted; message gauranteed.
2. Explain how “push notifications” work, using SNS.
    * The publisher sends out the required notifications that are to be delivered to subscribers.
    * The published messages are delivered to the SNS service, which has the following key components:
      * SNS Topic – that is used to filter out the messages that have to be sent to different subscribers. 
        * As an AWS developer, you first need to create an SNS topic that acts as the access point for subscribers.
        * Using the topic, subscribers can receive message notifications on their selected subject.
      * Message Filter – After being decoupled using topics, the SNS messages enter the message filter, which further filters the messages based on the subscriber’s selected policy.
        * Post the policy checking and permissions, the messages are finally sent to the respective subscribers.
    * The subscriber receives the message through subscribing queues or microservices. Subscribers provide useful information such as URL address, email address, or phone number in order to receive the message.

## [SQS and SNS Basics](https://www.youtube.com/watch?v=UesxWuZMZqI)

1. How might a large scale, distributed application make use of a Queue system like SQS?
   * Extended queue gives the ability to scale to massive amounts of users; some of the costs are sometimes you get a duplicated message, or sometimes poetically the message rules will arrive out of order.

## Bookmarks

1. [SNS Javascript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SNS.html)
2. [SQS Javascript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SQS.html)

## Things I want to know more about

1. My team is considering this topic for Lab 14, so planning to dig into the docs and dig further on youtube videos.