# Autoresponder Webform Subscription Triggers

Autoresponders triggered when a customer subscribes using a [subscription webform](/kb/regular-web-forms). 

## Configuration

Navigate to the _Autoresponders_ page and click 'Create new autoresponder' 
button and select 'Webform subscription' as your trigger. Please make sure you have at 
least one [subscription webform](/kb/regular-web-forms) created.

![](images/autoresponders/responder_3.png)

After this basic information is entered, you will be able to configure the autoresponders' details:

![](images/autoresponders/responder_4.png)

Let check what options you can control:

* **Webform submission** - A webform submission triggers this autoresponder. 
* **Reply to** - Email for your subscribers to reply to.
* **From name** - Name of sender (your or your organization). Subscribers will see emails as coming from this name.
* **Enabled** - Toggle that allows you to enable/disable autoresponder.
* **Delay rules** - Configure as many autoresponder messages as you need. 
    * _Then wait for_ - amount of time you want us to wait before sending the next message
    * _Start with_ - newsletter template you want to send
    * _With Subject_ - email subject

## Example

From the screenshot above, the following events will happen: 

* Contact submits a webform submission 
* The system waits for 2 hours
* The system sends out a newsletter "Follow Up Email" with subject "Thanks for joining us!"
* The system waits for 1 day 
* The system sends out a newsletter "Follow Up Email 2" with subject "Great opportunity."

