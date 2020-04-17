# Infrastructure

This is the home of the underlying infrastructure for the App 2025 **AnyCompany** SaaS application. This infrastructure creates one [Amazon EventBridge] custom event bus and an [AWS Lambda] function that allows [AWS Step Functions] workflows to place events onto the bus.

## Deployment instructions

1. First, build the app.
    ```bash
    sam build
    ```
1. Next, deploy the app using a guided deployment.
    ```bash
    sam deploy --guided
    ```
    * At the **Stack Name** prompt, enter `app2025-infrastructure`

## Placing events onto the bus

From this directory:

```bash
aws events put-events --entries file://putevents.json
```

This places five sample events onto the custom event bus you created.
