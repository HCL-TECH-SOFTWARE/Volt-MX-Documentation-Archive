---
layout: "documentation"
category: "voltmx_foundry_user_guide"
---
                               

User Guide: [SDKs](../../Foundry_SDKs.html) > [Cordova (PhoneGap) SDK](../Installing_PhoneGap_SDK.html) > [Invoking an Object Service](Objects_API_Reference.html) > OfflineObjectService Class

OfflineObjectService Class
==========================

Provides methods that perform operations acting on the sync database, including basic CRUD, metadata, and binary-related functions. An instance of OfflineObjectService is returned by the [getObjectService Method](getObjectService_Method.html) when the second parameter specifies {"access":"offline"}.

Methods
-------

The following methods are used by the OfflineObjectService class and its instantiations.

### create Method

Creates an object offline in the sync database.

#### Syntax

{% highlight voltMx %} create(options, successCallback, failureCallback);
{% endhighlight %}

#### Parameters

  
| Parameter | Description |
| --- | --- |
| options | JSON object with the mandatory parameter "dataObject", which must be an instance of the [voltmx.sdk.dto.DataObject Class](voltmx.sdk.dto.DataObject_Class.html) |
| successCallback | Function invoked when the operation succeeds, with the primary key of the created object |
| failureCallback | Function invoked when the operation fails, with cause of failure |

#### Example

{% highlight voltMx %} function create() { 
    var objSvc = voltmx.sdk.getCurrentInstance().getObjectService("serviceName", {
        "access": "offline"
    }); 
    var dataObject = new voltmx.sdk.dto.DataObject("ObjectName"); 
    dataObject.addField("field1", "value1"); 
    var options = {
        "dataObject": dataObject
    }; 
    objSvc.create(options,     function(res) {
        alert("Record created");
    },     function(err) {
        alert("Error in record creation");
    }  );
}
{% endhighlight %}

> **_Note:_** When using object services for SAP, the general norm is to have character field values stored in upper case. However, if you need to pass in mixed/lower case values for an SAP field, ensure that this field is designated as mixed case in the SAP Add-in LDB workbench.

### update Method

Updates an object offline in the sync database (local store).

#### Syntax

{% highlight voltMx %} update(options, successCallback, failureCallback);
{% endhighlight %}

#### Parameters

  
| Parameter | Description |
| --- | --- |
| options | JSON object with the mandatory parameter "dataObject", which must be an instance of the [voltmx.sdk.dto.DataObject Class](voltmx.sdk.dto.DataObject_Class.html) |
| successCallback | Function invoked when the operation succeeds, with the number of records updated |
| failureCallback | Function invoked when the operation fails, with cause of failure |

#### Example

{% highlight voltMx %} function update() { 
    var objSvc = voltmx.sdk.getCurrentInstance().getObjectService("serviceName", {
        "access": "offline"
    }); 
    var dataObject = new voltmx.sdk.dto.DataObject("ObjectName"); 
    dataObject.addField("field1", "value1"); 
    dataObject.addField("primaryKeyField", "value"); 
    var options = {
        "dataObject": dataObject
    }; 
    objSvc.update(options,     function(res) {
        alert("Record updated");
    },     function(err) {
        alert("Error in record update");
    }  );
}
{% endhighlight %}

### delete Method

Deletes an object offline in the sync database.

#### Syntax

{% highlight voltMx %} deleteRecord(options, successCallback, failureCallback);
{% endhighlight %}

#### Parameters

  
| Parameter | Description |
| --- | --- |
| options | JSON object with the mandatory parameter "dataObject", which must be an instance of the [voltmx.sdk.dto.DataObject Class](voltmx.sdk.dto.DataObject_Class.html) |
| successCallback | Function invoked when the operation succeeds, with the number of records deleted |
| failureCallback | Function invoked when the operation fails, with cause of failure |

#### Example

{% highlight voltMx %} function deleteRecord() { 
    var objSvc = voltmx.sdk.getCurrentInstance().getObjectService("serviceName", {
        "access": "offline"
    }); 
    var dataObject = new voltmx.sdk.dto.DataObject("ObjectName"); 
    dataObject.addField("field1", "value1"); 
    dataObject.addField("primaryKeyField", "value"); 
    var options = {
        "dataObject": dataObject
    }; 
    objSvc.deleteRecord(options,     function(res) {
        alert("Record deleted");
    },     function(err) {
        alert("Error in record deletion");
    }  );
}
{% endhighlight %}

### getMetadataOfAllObjects Method

Gets the metadata associated with the objects defined in the service from the local store.

#### Syntax

{% highlight voltMx %} getMetadataOfAllObjects(options, successCallback, failureCallback);
{% endhighlight %}

#### Parameters

  
| Parameter | Description |
| --- | --- |
| options | JSON object with the optional parameter "getFromServer" |
| successCallback | Function invoked when the operation succeeds, with the number of records updated |
| failureCallback | Function invoked when the operation fails, with cause of failure |

#### Example

{% highlight voltMx %} function getMetadata() { 
    var objSvc = voltmx.sdk.getCurrentInstance().getObjectService("serviceName", {
        "access": "offline"
    });  
    objSvc.getMetadataOfAllObjects({},     function(res) {
        alert("Metadata::" + res);
    },     function(err) {
        alert("Error in metadata::" + err);
    }  );
}
{% endhighlight %}

### getMetadataOfObject Method

Gets the metadata associated with an object defined in the service from the local store.

#### Syntax

{% highlight voltMx %} getMetadataOfObject(objectName, options, successCallback, failureCallback);
{% endhighlight %}

#### Parameters

  
| Parameter | Description |
| --- | --- |
| objectName | The name of the desired object as defined in the service |
| options | JSON object with the optional parameter "getFromServer" |
| successCallback | Function invoked when the operation succeeds, with the number of records returned |
| failureCallback | Function invoked when the operation fails, with cause of failure |

#### Example

{% highlight voltMx %} function getMetadata() { 
    var objSvc = voltmx.sdk.getCurrentInstance().getObjectService("serviceName", {
        "access": "offline"
    });  
    objSvc.getMetadataOfObject("objectName", {},     function(res) {
        alert("Metadata::" + res);
    },     function(err) {
        alert("error in metadata::" + err);
    }  );
}
{% endhighlight %}

### executeSelectQuery Method

Executes a Select query on the sync database.

#### Syntax

{% highlight voltMx %} executeSelectQuery(queryString, successCallback, failureCallback);
{% endhighlight %}

#### Parameters

  
| Parameter | Description |
| --- | --- |
| queryString | SQL Select query string |
| successCallback | Function invoked when the operation succeeds, with the number of records operated on |
| failureCallback | Function invoked when the operation fails, with cause of failure |

#### Example

{% highlight voltMx %} function executeSelectQuery() { 
    var objSvc = voltmx.sdk.getCurrentInstance().getObjectService("serviceName", {
        "access": "offline"
    });  
    var queryString = "select * from table";  
    objSvc.executeSelectQuery(queryString,     function(res) {
        alert("Metadata::" + res);
    },     function(err) {
        alert("Error in metadata::" + err);
    }  );
}
{% endhighlight %}

### getBinaryContent Method

Gets binary content from the sync database.

#### Syntax

{% highlight voltMx %} getBinaryContent(options, successCallback, failureCallback);
{% endhighlight %}

#### Parameters

  
| Parameter | Description |
| --- | --- |
| options | JSON object with the mandatory parameter "dataObject", which is an instance of the [voltmx.sdk.dto.DataObject Class](voltmx.sdk.dto.DataObject_Class.html) |
| successCallback | Function invoked when the operation succeeds, with the number of records gotten |
| failureCallback | Function invoked when the operation fails, with cause of failure |

#### Example

{% highlight voltMx %} function getBinaryContent() { 
    var objSvc = voltmx.sdk.getCurrentInstance().getObjectService("serviceName", {
        "access": "offline"
    });  
    var dataObject = new voltmx.sdk.dto.DataObject("media");  
    //primary key details to get media object  
    dataObject.addField("name", "4005174-002");  
    var options = {};  
    options.dataObject = dataObject;  
    //binary column name to get the binary data  
    options.binaryAttrName = "data";  
    options.responsetype = "base64string/filepath";  
    //filepath is default if it is not set by developer  
    objSvc.getBinaryContent(options, successcallback, errorcallback);  

    function successcallback(response) {    
        //response will contain base64string or filepath    
        //  based on responsetype   
        //value provided by the developer.   
        var content = response.records[0].data;  
    }  

    function errorcallback(err) {
        Alert(err);
    }
}
{% endhighlight %}
