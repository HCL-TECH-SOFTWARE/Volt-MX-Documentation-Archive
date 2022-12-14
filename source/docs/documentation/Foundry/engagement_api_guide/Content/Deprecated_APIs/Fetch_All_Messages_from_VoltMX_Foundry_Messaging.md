---
layout: "documentation"
category: "engagement_api_guide"
---
                          

Fetch All Messages from Volt MX Foundry Messaging
================================================

The API is used to get message content from the server based on the input parameters.

Request URL
-----------

{% highlight voltMx %}[http://<host or ip>:<port>/service/entrydata/fetchmessages](http://10.10.19.74:8080/service/entrydata/fetchmessages?userId=$ufid&amp;startElement=$start&amp;elementsPerPage=$perpage)
{% endhighlight %}

Request Method
--------------

HTTP POST

Input Parameters
----------------

This service takes input parameters in JSON formats.

1.  With KSID  
      
    {% highlight voltMx %}{ "ksid": "VoltMXSubscriberID",  
      "startElement": "0",   
      "elementsPerPage": "10" }
    {% endhighlight %}
    *   **ksid**: Volt MX Subscription ID returned when you subscribe to Volt MX Foundry Messaging system.
    *   startElement: Starting element is a non-negative integer such as 0,1,2,3.
    *   elementsPerPage: Number of messages to be displayed per page.
2.  With DEVICEID and APPID{% highlight voltMx %}{ "deviceId": "123456",  
       "appId" : "VoltMX Foundry Messaging_APPLICATION_ID",  
      "startElement": "0",   
      "elementsPerPage": "10" }
    {% endhighlight %}
    *   **deviceId**: Device ID of the Subscriber which was used when you subscribe to Volt MX Foundry Messaging system.
    *   **appId**: Application ID in Volt MX Foundry Messaging system.
    *   startElement: Starting element is a non-negative integer such as 0,1,2,3.
    *   elementsPerPage: Number of messages to be displayed per page.
3.  With UFID and APPID{% highlight voltMx %}{ "ufid": "xxx@gmail.com",  
       "appId": "VoltMX Foundry Messaging_APPLICATION_ID",  
      "startElement": "0",   
      "elementsPerPage": "10" }
    {% endhighlight %}
    
    *   **ufid**: UFID of the subscriber which was used when you subscribe to Volt MX Foundry Messaging system.
    *   **appId**: Application ID in Volt MX Foundry Messaging system.
    *   startElement: Starting element is a non-negative integer such as 0,1,2,3.
    *   elementsPerPage: Number of messages to be displayed per page.
    
    > **_Important:_** If the **Auth** t**oken** for **subscription** APItext box is enabled in the **Administration** \> **General** tab > **Security**, you need to append the authToken element in the JSON request for all the three formats.
    
    Sample JSON with authToken
    
    {% highlight voltMx %}{ "ksid": "VoltMXSubscriberID",  
      "startElement": "0",   
      "elementsPerPage": "10",  
      "authToken":  "xxxxxx"}
    {% endhighlight %}

Response
--------

Success response code is "_200_".

Response will be a JSON with all Push messages sent to the Subscriber. Sample response is:

{% highlight voltMx %}{"openedMessages":0,"submittedMessages":1,"totalMessages":1,"messages":[{"content":"This is a test push.","status":"Submitted","fetchid":"7530271640775557121"}]}
{% endhighlight %}

*   **openedMessages**: Number of Messages opened by Subscriber.
*   **submittedMessages**: Number of messages successfully delivered to Subscriber and not opened.
*   **totalMessages**: Total Number of messages successfully delivered to Subscriber.
