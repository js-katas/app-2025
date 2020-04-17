# App 2025

Want to see how everyone will build [serverless applications][serverless] on [AWS][aws] in 2025? Want to use those patterns today to gain a competitive advantage?

Come learn how, with App 2025! Every Thursday we'll build a bit of our application live on [Twitch][twitch], so you can see the patterns that will help you get ahead today.

## Past sessions:

### Amazon EventBridge as the backbone of your app

In the [first episode][first-episode] of App 2025, viewers learn a high-level pattern for building serverless applications. A sample use case is presented: an order fulfillment application for AnyCompany , a fictional Software as a Service (SaaS) company. [Amazon EventBridge][eventbridge] is introduced as the backbone of the app. [AWS Step Functions][step-functions] workflows, both standard and express, are introduced for business processes that consume events from EventBridge. Service integrations are introduced for data storage, and [Identity and Access Management (IAM)][iam] considerations are discussed. Monitoring and auditability of events on EventBridge are discussed. Finally, [AWS SAM CLI][sam-cli] is introduced, and a simple template is created with a single resource, a custom EventBridge event bus.

### Express Workflows for quick-running processes

In the [second episode][second-episode] of App 2025, viewers learn a second high-level pattern for building serverless applications. AWS Step Functions [Express Workflows][express-workflows] are introduced for building high-volume, short-duration workflows. Express and Standard Workflows are compared and a rubric is provided for when to select each. The workflow event loop pattern is introduced: an event on an EventBridge event bus satisfies a rule and invokes an Express Workflow as a target. Once the workflow completes, a “ProcessCompleted” event is placed back onto the bus for further processing.

## Upcoming Sessions (subject to change):

* 23 April - Waiting for human interaction with the [callback pattern][callback-pattern]
* 30 April - Notifying users with [Amazon SNS][sns]

## Deploying the app

1. First, [deploy the infrastructure][deploy-infrastructure].
1. Next, [deploy the customer microservice][deploy-customer].

Copyright 2020 Amazon.com, Inc. or its affiliates. All Rights Reserved.
SPDX-License-Identifier: Apache-2.0

[aws]: https://aws.amazon.com/
[callback-pattern]: https://docs.aws.amazon.com/step-functions/latest/dg/connect-to-resource.html#connect-wait-token
[eventbridge]: https://aws.amazon.com/eventbridge/
[express-workflows]: https://aws.amazon.com/about-aws/whats-new/2019/12/introducing-aws-step-functions-express-workflows/
[iam]: https://aws.amazon.com/iam/
[sam-cli]: https://github.com/awslabs/aws-sam-cli/
[serverless]: https://aws.amazon.com/serverless/
[sns]: https://aws.amazon.com/sns/
[step-functions]: https://aws.amazon.com/step-functions/
[twitch]: https://twitch.tv/robsutter/

[first-episode]: https://youtu.be/jYmZH7j_MXA?t=80
[second-episode]: https://youtu.be/pdc6oorQ3lE

[deploy-infrastructure]: infrastructure/
[deploy-customer]: customer/
