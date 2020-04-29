# App 2025

Want to see how everyone will build [serverless applications][serverless] on [AWS][aws] in 2025? Want to use those patterns today to gain a competitive advantage?

Come learn how, with App 2025! Every Thursday we'll build a bit of our application live on [Twitch][twitch], so you can see the patterns that will help you get ahead today.

## Past sessions:

### Amazon EventBridge as the backbone of your app

In the [first episode][first-episode] of App 2025, viewers learn a high-level pattern for building serverless applications. A sample use case is presented: an order fulfillment application for AnyCompany , a fictional Software as a Service (SaaS) company. [Amazon EventBridge][eventbridge] is introduced as the backbone of the app. [AWS Step Functions][step-functions] workflows, both standard and express, are introduced for business processes that consume events from EventBridge. Service integrations are introduced for data storage, and [Identity and Access Management (IAM)][iam] considerations are discussed. Monitoring and auditability of events on EventBridge are discussed. Finally, [AWS SAM CLI][sam-cli] is introduced, and a simple template is created with a single resource, a custom EventBridge event bus.

### Express Workflows for quick-running processes

In the [second episode][second-episode] of App 2025, viewers learn a second high-level pattern for building serverless applications. AWS Step Functions [Express Workflows][express-workflows] are introduced for building high-volume, short-duration workflows. Express and Standard Workflows are compared and a rubric is provided for when to select each. The workflow event loop pattern is introduced: an event on an EventBridge event bus satisfies a rule and invokes an Express Workflow as a target. Once the workflow completes, a “ProcessCompleted” event is placed back onto the bus for further processing.

### Waiting for interactions with callbacks

In the [third episode][third-episode] of App 2025, viewers learn how to pause execution of AWS Step Functions workflows using [callbacks][callbacks]. AWS Step Functions [Standard Workflows][standard-workflows] are introduced for building lower-volume, longer-running workflows. The _.waitTaskToken_ callback pattern is introduced for tasks that involve human interaction, are longer-running, or are cost-sensitive. Supported services are introduced, and _SendTaskSuccess_, _SendTaskFailure_, and _SendTaskHeartbeat_ are discussed.

## Upcoming Sessions (subject to change):

* 30 April - Simplifying your architecture with [Amazon SNS][sns] and [Amazon SQS][sqs]
* 07 May - Securing your workloads with [Amazon SNS][sns] and [Amazon SQS][sqs]
* 14 May - Enhancing the durability of your workloads with [Amazon SNS][sns] and [Amazon SQS][sqs] dead-letter queues (DLQs)
* 21 May - Service integrations for storing data
* 28 May - Serverless reporting with [Amazon Athena][athena]

## Deploying the app

1. First, [deploy the infrastructure][deploy-infrastructure].
1. Next, [deploy the customer microservice][deploy-customer].
1. Finally, [deploy the simulator app][deploy-simulator].

## Episode transcripts

Machine-generated transcripts for each episode are available in the [transcripts](transcripts) directory.

Copyright 2020 Amazon.com, Inc. or its affiliates. All Rights Reserved.
SPDX-License-Identifier: Apache-2.0

[athena]: https://aws.amazon.com/athena/
[aws]: https://aws.amazon.com/
[callbacks]: https://docs.aws.amazon.com/step-functions/latest/dg/connect-to-resource.html#connect-wait-token
[eventbridge]: https://aws.amazon.com/eventbridge/
[express-workflows]: https://aws.amazon.com/about-aws/whats-new/2019/12/introducing-aws-step-functions-express-workflows/
[iam]: https://aws.amazon.com/iam/
[sam-cli]: https://github.com/awslabs/aws-sam-cli/
[serverless]: https://aws.amazon.com/serverless/
[sns]: https://aws.amazon.com/sns/
[sqs]: https://aws.amazon.com/sqs/
[standard-workflows]: https://docs.aws.amazon.com/step-functions/latest/dg/concepts-standard-vs-express.html
[step-functions]: https://aws.amazon.com/step-functions/
[twitch]: https://twitch.tv/robsutter/

[first-episode]: https://youtu.be/jYmZH7j_MXA?t=80
[second-episode]: https://youtu.be/pdc6oorQ3lE
[third-episode]: https://youtu.be/raFNW7KdehE

[deploy-infrastructure]: infrastructure/
[deploy-customer]: customer/
[deploy-simulator]: simulator/
