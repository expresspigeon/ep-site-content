# Webhooks for Transactional Events

While you can pull a report for a [single message](transactional-reporting-for-single-message) 
or even [multiple messages](transactional-reporting-for-multiple-messages), it takes polling our API 
 for information. A more efficient way efficient way to get all this data is to use 
 [Webhooks](https://en.wikipedia.org/wiki/Webhook) to get notified in real time when this is happening. 
  
## Setup Authentication

Please, navigate to Transactional, and then to the Webhooks tab:  

![](images/webhooks.png)

## Plant Authentication file 

On this page, please download an authentication file by clicking the "Download file" button. 
Once you have the file, you need to plant this file on your site in order to verify the ownership of the website.
 
## Tell us where it is 

Usually these files are placed at the root of your site: `https://yoursite.com/ep-api-28f848b89552441788fef75xxxxxxxxx.txt`. 
After that, please enter the URL to your site on the config page: 

![](images/webhooks-1.png)

## Test configuration

After the configuraion is complete, you need to validate it in order to move forward. 
Please, click the "Test link" button and observe messages. 

If the configuration is correct, you will see a green positive message and the "Continue" button will be enabled. 
 
## Configure event types

Once you move to the next page, you will be able to configure separate URIs for every type of event, once you enable them. 

![](images/webhooks-2.png)

> Additionally, you can click the "Play" button for each event to see the format and simulate an actual request.

## Webhook types and payload

Delivered:

~~~~ {.js .numberLines}
{
   "id":"1234", 
   "timestamp": "2017-05-28T14:03:17.956+0300",
   "email":"john@doe.com",
   "type":"delivered" 
}
~~~~

Opened:

~~~~ {.js .numberLines}
{
   "id":"1234", 
   "timestamp": "2017-05-28T14:03:17.956+0300",
   "email":"john@doe.com",
   "type":"opened",
   "user-agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:64.0) Gecko/20100101 Firefox/64.0",
   "ip":"215.11.12.11",
   "latitude":51.3,
   "longitude":9.49
}
~~~~

Clicked:

~~~~ {.js .numberLines}
{
   "id":"1234", 
   "timestamp": "2017-05-28T14:03:17.956+0300",
   "email":"john@doe.com",
   "type":"clicked",
   "user-agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:64.0) Gecko/20100101 Firefox/64.0",
   "ip":"215.11.12.11",
   "latitude":51.3,
   "longitude":9.49
}
~~~~

Suppressed:

~~~~ {.js .numberLines}
{
   "id":"1234", 
   "timestamp": "2017-05-28T14:03:17.956+0300",
   "email":"john@doe.com",
   "type":"suppressed" 
}
~~~~

Soft Bounce:

~~~~ {.js .numberLines}
{
   "id":"1234", 
   "timestamp": "2017-05-28T14:03:17.956+0300",
   "email":"john@doe.com",
   "type":"bounced" 
}
~~~~

Hard bounce:

~~~~ {.js .numberLines}
{
   "id":"1234", 
   "timestamp": "2017-05-28T14:03:17.956+0300",
   "email":"john@doe.com",
   "type":"hard_bounce" 
}
~~~~

## Webhook errors

In case your API goes down and we are unable to execute the service calls, we log at most 500 errors to the [Error Log](/kb/webhooks-error-log).