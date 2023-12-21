# Schedule Multiple ECS Fargate Task with specific configurations

This project supports the deployment of multiple ECS tasks via EventBridge Schedules.

## Use Case

The specific use case this was designed is to run automated scheduled tasks across multiple AWS Accounts or whole Organizations using Assume Role functionality.

The template provided here has been modified to be a more basic use case where a custom image that requires a unique configuration can be run in its own scheduled task.

## Deployment

This template deploys N number of ECS Fargate task definitions, SSM Parameters, and companion EventBridge Schedules using CloudFormation Loops to pair each Task with its own schedule.

Modify `Line 140` to add/remove the number of deployments desired using unique task names.

## Modifications

Specific Task permission will need to be added to the `rTaskDefTaskRole:` resource to make sure the task has the ability to do what it needs to do.

## Warnings and Notices

Use at your own risk and deploy responsibly.
This is a sanitized template that was originally used for a very specific use case.

This can easily be modified to support any task that may require a unique configuration that may be dynamic or change prior to each schedule run.
