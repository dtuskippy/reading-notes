# Class-18 Reading Notes

It's a topic that is very relevant to this week's course work, but also very practical in the 'real world'.

## [AWS API Gateway Overview](https://www.serverless.com/guides/amazon-api-gateway)

1. What is Amazon API Gateway?
    * Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic.
    * It also handles authentication, access control, monitoring, and tracing of API requests.
    * Many Serverless applications use Amazon API Gateway, which conveniently replaces the API servers with a managed serverless solution.
2. Why is Amazon API Gateway an important part of the Serverless ecosystem?
    * Within the Serverless ecosystem, API Gateway is the piece that ties together Serverless functions and API definitions.
    * Being able to trigger the execution of a Serverless function directly in response to an HTTP request is the key reason why API Gateway is so valuable in Serverless setups: it enables a truly serverless architecture for web applications.
    * When using API Gateway together with other AWS services, it’s possible to build a fully functional customer-facing web application without maintaining a single server yourself.
    * This brings the advantages of the serverless model—scalability, low maintenance, and low cost due to low overhead—to mainstream web applications.
3. How does API Gateway integrate with other AWS services?
    * Many AWS services support integration with Amazon API Gateway, including:
      * AWS Lambda: run Lambda functions to generate HTTP API responses.
      * AWS SNS: publish SNS notifications when an HTTP API endpoint is accessed.
      * Amazon Cognito: provide authentication and authorization for your HTTP APIs.
    * API Gateway supports direct integrations that can be configured in the API Gateway user interface (or via the API Gateway’s own API) for the following actions:
      * Invoking an AWS Lambda function.
      * Invoking another HTTP endpoint, with or without VPC Link.
      * Making an HTTP call against the API of any AWS service that provides an HTTP API.
      * Returning a mock response generated within API Gateway without calling out to other services.

## [AWS API Gateway](https://aws.amazon.com/api-gateway/)

1. What are the some benefits of using Amazon API Gateway?
    * Efficient API development.
    * Easy monitoring.
    * Performance at any scale.
    * Flexible security controls.
    * Cost savings at scale.
    * RESTful API options.
2. What two API types might you choose from?
    * RESTful APIs
      * Build RESTful APIs optimized for serverless workloads and HTTP backends using HTTP APIs. HTTP APIs are the best choice for building APIs that only require API proxy functionality.
      * If your APIs require API proxy functionality and API management features in a single solution, API Gateway also offers REST APIs.
    * WEBSOCKET APIs
      * Build real-time two-way communication applications, such as chat apps and streaming dashboards, with WebSocket APIs.
      * API Gateway maintains a persistent connection to handle message transfer between your backend service and your clients.

## [AWS DynamoDB Guide](https://www.dynamodbguide.com/what-is-dynamo-db/)

1. What is DynamoDB?
    * Basically AWS's Mongo
    * DynamoDB is a hosted NoSQL database offered by Amazon Web Services (AWS). It offers:
      * reliable performance even as it scales;
      * a managed experience, so you won't be SSH-ing into servers to upgrade the crypto libraries;
      * a small, simple API allowing for simple key-value access as well as more advanced query patterns.
2. Under what circumstances would you recommend DynamoDB over MongoDB?
    * Depends on use case of course, but if you're largely an AWS shop, it may make sense to go with DynamoDB due to tigther integration with other AWS services, and you'll get economies of scale on the management side.

## [AWS DynamoDB](https://aws.amazon.com/dynamodb/)

1. Explain to a non-technical friend how DynamoDB works.
    * DynamoDB is in a category databases called NoSQL, which means that it stores data documents instead of the columns and rows used by relational databases, and is purely available in the cloud on AWS.

## [Dynamoose](https://dynamoosejs.com/getting_started/Introduction)

1. What is Dynamoose?
    * Dyanamoose is the Mongoose for DynamoDB.
2. What are some key features of Dynamoose?
    * Type safety.
    * High level API.
    * Easy to use syntax.
    * DynamoDB Single Table Design Support.
    * Ability to transform data before saving or retrieving items.
    * Strict data modeling (validation, required attributes, and more).
    * Support for DynamoDB Transactions.
    * Powerful Conditional/Filtering Support.
    * Callback & Promise support.
    * AWS Multi-region support.

## Things I want to know more about

1. I would like to dig in deeper on some of the documentation for Dynamoose.