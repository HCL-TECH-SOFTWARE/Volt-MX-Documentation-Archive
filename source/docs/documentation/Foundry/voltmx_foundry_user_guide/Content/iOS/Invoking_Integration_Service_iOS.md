---
layout: "documentation"
category: "voltmx_foundry_user_guide"
---
                             

User Guide: [SDKs](../Foundry_SDKs.html) > [iOS SDK](Installing.html) > Invoking an Integration Service

Invoking an Integration Service
===============================

{% highlight voltMx %} // Sample code to fetch the integration service details
HCLIntegrationService * integration = [
    [HCLIntegrationService alloc]
    initWithServiceName: @"<service-name>"
];

NSDictionary * headers = @ {@
    "<header-name1>": @"<header-value1>",
    @"<header-name2>": @"<header-value2>"
};

NSDictionary * parameters = @ {@
    "<param-name1>": @"<param-value1>",
    @"<param-name2>": @"<param-value2>"
};

[integration invokeOperationInBackgroundWithOperationName: @"<operation-name>"
    headers: headers
    parameters: parameters
    completion: ^ (NSDictionary * objects, NSError * error) {
        if (error == nil) {
            // use data in 'objects' returned by the operation
            // ...
        } else {
            // handle the failure case here
            // use the details in 'error'
        }
    }
];
{% endhighlight %}
