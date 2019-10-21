# simple-php-webhook

Simple webhook, simple documentation.
This is an example webhook for PHP. It's not pretty, but it does the job. 

We strongly suggest to keep webhooks simple and fast and handle processing logic async. This webhook contains an example message for testing. You can navigate to https://app.messengerpeople.dev/monitoring/ to see all your incoming and outgoing messages. The field "webhook_request" contains the payload that would be sent to your webhook.  

DO:

Store the incoming message in a messagequeue or database and process it asynchronously in a different worker.

DON'T:

Parse the message, do many DB Queries, or any blocking external requests. We have a very low timeout setting (2 seconds), so keep your webhook fast.

