# Class-17 Reading Notes

It's a topic that is very relevant to this week's course work, but also very practical in the 'real world'.

## [AWS S3](https://aws.amazon.com/s3/)

1. What is Amazon S3?
    * Amazon Simple Storage Service (Amazon S3) is an object storage service offering industry-leading scalability, data availability, security, and performance. 
      * Customers of all sizes and industries can store and protect any amount of data for virtually any use case, such as data lakes, cloud-native applications, and mobile apps. 
      * With cost-effective storage classes and easy-to-use management features, you can optimize costs, organize data, and configure fine-tuned access controls to meet specific business, organizational, and compliance requirements.
2. Name some use cases for Amazon S3.
    * Build a data lake.
    * Back up and restore critical data.
    * Archive data at the lowest cost.
    * Run cloud-native applications.
3. Name some benefits of using Amazon S3.
    * Low cost
    * Scalablity
    * Durability
    * High availability
    * Security
    * Easy to manage

## [AWS Lambda Basics](https://www.serverless.com/aws-lambda)

1. What is AWS Lambda?
    * AWS Lambda is a serverless computing service provided by Amazon Web Services (AWS).
    * Users of AWS Lambda create functions, self-contained applications written in one of the supported languages and runtimes, and upload them to AWS Lambda, which executes those functions in an efficient and flexible manner.
2. Name some use cases for AWS Lambdas.
    * Due to Lambda’s architecture, it can deliver great benefits over traditional cloud computing setups for applications where:
      * Individual tasks run for a short time.
      * Each task is generally self-contained.
      * There is a large difference between the lowest and highest levels in the workload of the application.
    * Scalable APIs.
      * When building APIs using AWS Lambda, one execution of a Lambda function can serve a single HTTP request.
      * Different parts of the API can be routed to different Lambda functions via Amazon API Gateway.
      * AWS Lambda automatically scales individual functions according to the demand for them, so different parts of your API can scale differently according to current usage levels.
      * This allows for cost-effective and flexible API setups.
    * Data processing.‍
      * Lambda functions are optimized for event-based data processing.
      * It is easy to integrate AWS Lambda with datasources like Amazon DynamoDB and trigger a Lambda function for specific kinds of data events.
      * For example, you could employ Lambda to do some work every time an item in DynamoDB is created or updated, thus making it a good fit for things like notifications, counters and analytics.
3. Describe “serverless” to a non-technical friend.
    * The concept of “serverless” computing refers to not needing to maintain your own servers to run these functions.
    * AWS Lambda is a fully managed service that takes care of all the infrastructure for you.
    * And so “serverless” doesn’t mean that there are no servers involved: it just means that the servers, the operating systems, the network layer and the rest of the infrastructure have already been taken care of, so that you can focus on writing application code.

## [CDN](https://cyberhoot.com/cybrary/content-delivery-network-cdn/)

1. What is a CDN?
    * Content Delivery Network: a geographically distributed group of servers that work together to provide fast delivery of Internet content. 
    * A CDN allows for the fast transfer of data needed for loading Internet content including HTML pages, javascript files, stylesheets, images, and videos.
2. How does a CDN work with relation to the website visitor?
    * CDNs work through servers nearest to the website visitor respond to the request.
    * The content delivery network copies the pages of a website to a network of servers that are spread out at geographically different locations, caching the contents of the page.
    * When a user requests a webpage that is part of a content delivery network, the CDN will redirect the request from the originating site’s server to a server in the CDN that is closest to the user and deliver the cached content.
    * CDNs will also communicate with the originating server to deliver any content that has not been previously cached.
    * In turn, the speed is improved by distributing content closer to the website visitors by using a nearby CDN server, causing visitors to experience faster page loading times.
    * In simpler terms, for example, instead of a user in London trying to access a server in LA, which can cause slower Internet speeds, the user would be redirected through a CDN that is geographically closest to them (London, Paris, Stockholm, etc).
    * As of today, the majority of web traffic goes through through CDNs, including traffic from major sites like Facebook, Netflix, and Amazon.
3. What are the benefits of employing a CDN?
    * Speed: increased speed for both website load times, and content delivery (most obviously, video).
    * Security: specifically reducing the likelihood of falling victim to and improve defenses against Distributed Denial of Service attacks (DDoS).

## Things I want to know more about

1. I would like to dig in deeper on some of the documentation re. Lambda.