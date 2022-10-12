# AWS: API, Dynamo and Lambda

## AWS API Gateway Overview

<https://www.serverless.com/amazon-api-gateway>

What is Amazon API Gateway?

Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.

Why is Amazon API Gateway an important part of the Serverless ecosystem?

It provides a set of tools that help you manage your API definitions and the mappings between endpoints and their respective backend services. It can also generate API references from your definitions and make them available to your users as API documentation.

How does API Gateway integrate with other AWS services?

API Gateway integrates with many other AWS services like AWS Lambda, AWS SNS, AWS IAM, and Cognito Identity Pools. These integrations allow for fully managed authentication and authorization layers, as well as detailed metrics and tracing for API requests.

## AWS API Gateway

<https://aws.amazon.com/api-gateway/>

What are the some benefits of using Amazon API Gateway?

Easy for developers to create, publish, maintain, monitor, and secure APIs at any scale. APIs act as the "front door" for applications to access data, business logic, or functionality from your backend services

What two API types might you choose from?

RESTful APIs and WebSocket APIs

## AWS DynamoDB Guide

<https://www.dynamodbguide.com/what-is-dynamo-db/>

What is DynamoDB?

A hosted NoSQL database offered by Amazon Web Services (AWS).

Under what circumstances would you recommend DynamoDB over MongoDB?

If connection, security, scalability. Dynamo is less flexabile but it won't let you write a bad query that won't scale.

## AWS DynamoDB

<https://aws.amazon.com/dynamodb/>

Explain to a non-technical friend how DynamoDB works.

Amazon DynamoDB is a high preformance cloud based database application that manages all preformance work for you.

## Dynamoose

What is Dynamoose?

Dynamoose is a modeling tool for Amazon's DynamoDB.

What are some key features of Dynamoose?

Type safety
High level API
Easy to use syntax
DynamoDB Single Table Design Support
Ability to transform data before saving or retrieving items
Strict data modeling (validation, required attributes, and more)
Support for DynamoDB Transactions
Powerful Conditional/Filtering Support
Callback & Promise support
AWS Multi-region support

## Things I want to know more about

image.png

Download the tools needed to to run JavaScript on AWS
<https://aws.amazon.com/developer/language/javascript/?nc1=f_dr>

Amazon CodeWhisperer
<https://aws.amazon.com/codewhisperer/>