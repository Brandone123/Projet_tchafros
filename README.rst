Google Cloud Pub/Sub Python Samples
https://gstatic.com/cloudssh/images/open-btn.png

This directory contains samples for Google Cloud Pub/Sub. Google Cloud Pub/Sub is a fully-managed real-time messaging service that allows you to send and receive messages between independent applications.
Setup
Authentication

This sample requires you to have authentication setup. Refer to the Authentication Getting Started Guide for instructions on setting up credentials for applications.
Install Dependencies

    Clone python-docs-samples and change directory to the sample directory you want to use.

        $ git clone https://github.com/GoogleCloudPlatform/python-docs-samples.git

    Install pip and virtualenv if you do not already have them. You may want to refer to the Python Development Environment Setup Guide for Google Cloud Platform for instructions.

    Create a virtualenv. Samples are compatible with Python 2.7 and 3.4+.

        $ virtualenv env
        $ source env/bin/activate

    Install the dependencies needed to run the samples.

        $ pip install -r requirements.txt

Samples
Publisher
https://gstatic.com/cloudssh/images/open-btn.png

To run this sample:

$ python publisher.py --help

usage: publisher.py [-h]
                    project_id
                    {list,create,delete,publish,publish-with-custom-attributes,publish-with-error-handler,publish-with-batch-settings,publish-with-retry-settings}
                    ...

This application demonstrates how to perform basic operations on topics
with the Cloud Pub/Sub API.

For more information, see the README.md under /pubsub and the documentation
at https://cloud.google.com/pubsub/docs.

positional arguments:
  project_id            Your Google Cloud project ID
  {list,create,delete,publish,publish-with-custom-attributes,publish-with-error-handler,publish-with-batch-settings,publish-with-retry-settings}
    list                Lists all Pub/Sub topics in the given project.
    create              Create a new Pub/Sub topic.
    delete              Deletes an existing Pub/Sub topic.
    publish             Publishes multiple messages to a Pub/Sub topic.
    publish-with-custom-attributes
                        Publishes multiple messages with custom attributes to
                        a Pub/Sub topic.
    publish-with-error-handler
                        Publishes multiple messages to a Pub/Sub topic with an
                        error handler.
    publish-with-batch-settings
                        Publishes multiple messages to a Pub/Sub topic with
                        batch settings.
    publish-with-retry-settings
                        Publishes messages with custom retry settings.

optional arguments:
  -h, --help            show this help message and exit

Subscribers
https://gstatic.com/cloudssh/images/open-btn.png

To run this sample:

$ python subscriber.py --help

usage: subscriber.py [-h]
                     project_id
                     {list-in-topic,list-in-project,create,create-with-dead-letter-policy,create-push,delete,update-push,update-dead-letter-policy,remove-dead-letter-policy,receive,receive-custom-attributes,receive-flow-control,receive-synchronously,receive-synchronously-with-lease,listen-for-errors,receive-messages-with-delivery-attempts}
                     ...

This application demonstrates how to perform basic operations on
subscriptions with the Cloud Pub/Sub API.

For more information, see the README.md under /pubsub and the documentation
at https://cloud.google.com/pubsub/docs.

positional arguments:
  project_id            Your Google Cloud project ID
  {list-in-topic,list-in-project,create,create-with-dead-letter-policy,create-push,delete,update-push,update-dead-letter-policy,remove-dead-letter-policy,receive,receive-custom-attributes,receive-flow-control,receive-synchronously,receive-synchronously-with-lease,listen-for-errors,receive-messages-with-delivery-attempts}
    list-in-topic       Lists all subscriptions for a given topic.
    list-in-project     Lists all subscriptions in the current project.
    create              Create a new pull subscription on the given topic.
    create-with-dead-letter-policy
                        Create a subscription with dead letter policy.
    create-push         Create a new push subscription on the given topic.
    delete              Deletes an existing Pub/Sub topic.
    update-push         Updates an existing Pub/Sub subscription's push
                        endpoint URL. Note that certain properties of a
                        subscription, such as its topic, are not modifiable.
    update-dead-letter-policy
                        Update a subscription's dead letter policy.
    remove-dead-letter-policy
                        Remove dead letter policy from a subscription.
    receive             Receives messages from a pull subscription.
    receive-custom-attributes
                        Receives messages from a pull subscription.
    receive-flow-control
                        Receives messages from a pull subscription with flow
                        control.
    receive-synchronously
                        Pulling messages synchronously.
    receive-synchronously-with-lease
                        Pulling messages synchronously with lease management
    listen-for-errors   Receives messages and catches errors from a pull
                        subscription.
    receive-messages-with-delivery-attempts

optional arguments:
  -h, --help            show this help message and exit

Identity and Access Management
https://gstatic.com/cloudssh/images/open-btn.png

To run this sample:

$ python iam.py

usage: iam.py [-h]
              project
              {get-topic-policy,get-subscription-policy,set-topic-policy,set-subscription-policy,check-topic-permissions,check-subscription-permissions}
              ...

This application demonstrates how to perform basic operations on IAM
policies with the Cloud Pub/Sub API.

For more information, see the README.md under /pubsub and the documentation
at https://cloud.google.com/pubsub/docs.

positional arguments:
  project               Your Google Cloud project ID
  {get-topic-policy,get-subscription-policy,set-topic-policy,set-subscription-policy,check-topic-permissions,check-subscription-permissions}
    get-topic-policy    Prints the IAM policy for the given topic.
    get-subscription-policy
                        Prints the IAM policy for the given subscription.
    set-topic-policy    Sets the IAM policy for a topic.
    set-subscription-policy
                        Sets the IAM policy for a topic.
    check-topic-permissions
                        Checks to which permissions are available on the given
                        topic.
    check-subscription-permissions
                        Checks to which permissions are available on the given
                        subscription.

optional arguments:
  -h, --help            show this help message and exit

The client library

This sample uses the Google Cloud Client Library for Python. You can read the documentation for more details on API usage and use GitHub to browse the source and report issues.