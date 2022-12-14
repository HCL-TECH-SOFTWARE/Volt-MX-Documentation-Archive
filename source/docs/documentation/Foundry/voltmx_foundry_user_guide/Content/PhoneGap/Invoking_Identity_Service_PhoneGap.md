---
layout: "documentation"
category: "voltmx_foundry_user_guide"
---
                             

User Guide: [SDKs](../Foundry_SDKs.html) > [Cordova (PhoneGap) SDK](Installing_PhoneGap_SDK.html) > Login with provider type as Basic

Invoking an Identity Service
============================

Identity service is used to authenticate user to use Volt MX Foundry integration service.

You can use the following methods for an Identity Service:

*   [Login with provider type as Basic](#login-with-provider-type-as-basic)
*   [Login with provider type as OAuth/SAML](#login-with-provider-type-as-oauth-saml)
*   [Get Profile](#get-profile)
*   [Get Backend Token](#get-backend-token)
*   [Logout](#logout)

Login with provider type as Basic
---------------------------------

{% highlight voltMx %} // Sample code to authenticate to Volt MX Foundry Client
//For Volt MX user repository, use "userstore" in place of "<IdentityName>"
var identity = voltmxSDKObject.getIdentityService("<IdentityName>");
identity.login({
        "username": username,
        "password": password
    },
    successHandler, errorHandler);
{% endhighlight %}

> **_Important:_** When you select Volt MX User Repository as the identity type, the system does not allow you to provide an identity name.  
  
To use Volt MX User Repository as authentication service, ensure that the value for `providerName` is set as userstore. If you set providername with any other value (for example, Volt MX User Repository, User Store or Cloud Repository), the system throws an error.

Login with provider type as OAuth/SAML
--------------------------------------

{% highlight voltMx %} // Sample code to authenticate to Volt MX Foundry Client
var identity = voltmxSDKObject.getIdentityService("<IdentityName>");
identity.login({}, successHandler, errorHandler);
{% endhighlight %}

Get Profile
-----------

{% highlight voltMx %} // Sample code to get profile information of the user
var fromserver = false;
identity.getProfile(fromserver, successHandler, errorHandler);
{% endhighlight %}

Get Backend Token
-----------------

{% highlight voltMx %} 
// Sample code to get backend token for provider
var fromserver = false;
identity.getBackendToken(fromserver, {}, successHandler, errorHandler);
{% endhighlight %}

Logout
------

{% highlight voltMx %} // Sample code to logout from auth service

identity.logout(successHandler, errorHandler);
{% endhighlight %}
