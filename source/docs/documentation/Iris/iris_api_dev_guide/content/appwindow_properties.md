---
layout: "documentation"
category: "iris_api_dev_guide"
---
                            

AppWindow Properties
====================

The AppWindow object contains the following properties.


<details close markdown="block"><summary>buttonsFocusSkin Property</summary>

* * *

This property applies a skin in the focused state to all the buttons in the title bar (back, maximize, and minimize buttons).

### Syntax

{% highlight VoltMx %}
appwindow.buttonsFocusSkin
{% endhighlight %}

### Type

String

### Read/Write

Read + Write

### Remarks

The default value for this property is null (system theme).

Passing a null or empty string resets the property to the system theme.

**BackgroundColor** and **ForegroundColor** are picked from valid skins. The rest of the skin properties are ignored.

### Availability

Windows 10

* * *

</details>
<details close markdown="block"><summary>buttonsHoverSkin</summary>

* * *

This property applies a skin when the mouse is hovering to all the buttons of the title bar (back, maximize, and minimize buttons).

### Syntax

{% highlight VoltMx %}
appwindow.buttonsHoverSkin
{% endhighlight %}

### Type

String

### Read/Write

Read + Write

### Remarks

The default value for this property is null (system theme).

Passing a null or empty string resets the property to the system theme.

**BackgroundColor**and **ForegroundColor** are picked from valid skins. The rest of the skin properties are ignored.

### Availability

Windows 10

**Example**

{% highlight VoltMx %}
var appwindow = voltmx.appication.getAppWindow();
appwindow.buttonsHoverSkin = "skin1";	
{% endhighlight %}

* * *

</details>
<details close markdown="block"><summary>buttonsInactiveSkin</summary>

* * *

This property applies a skin in the inactive state to all the buttons in the title bar (back, maximize, and minimize buttons).

### Syntax

{% highlight VoltMx %}
appwindow.buttonsInactiveSkin
{% endhighlight %}

### Type

String

### Read/Write

Read + Write

### Remarks

The default value for this property is null (system theme).

Passing a null or empty string resets the property to the system theme.

**BackgroundColor** and **ForegroundColor**are picked from valid skins. The rest of the skin properties are ignored.

### Availability

Windows 10

**Example**

{% highlight VoltMx %}
var appwindow = voltmx.application.getAppWindow();
appwindow.buttonsInactiveSkin = "skin1";		
{% endhighlight %}

* * *

</details>
<details close markdown="block"><summary>buttonsSkin</summary>

* * *

This property applies a skin in a normal state to all the buttons in the title bar (back, maximize, and minimize buttons).

### Syntax

{% highlight VoltMx %}
appwindow.buttonsSkin
{% endhighlight %}

### Type

String

### Read/Write

Read + Write

### Remarks

The default value for this property is null (system theme).

Passing a null or empty string resets the property to the system theme. **BackgroundColor** and **ForegroundColor** are picked from valid skins. The rest of the skin properties are ignored.

### Availability

Windows 10

**Example**

{% highlight VoltMx %}
var appwindow = voltmx.application.getAppWindow();
appwindow.buttonsSkin = "skin1";
{% endhighlight %}

* * *

</details>
<details close markdown="block"><summary>showBackButton</summary>

* * *

This property specifies whether the back button is shown in the title bar.

### Syntax

{% highlight VoltMx %}
appwindow.showBackButton
{% endhighlight %}

### Type

Boolean

### Read/Write

Read + Write

### Remarks

If this property is **true**, the form is checked. If the user is in the first form, the back button will be hidden. Otherwise, the button will be visible.

If the property is **false**, the back button is hidden.

The default value is **false**.

### Availability

Windows 10

**Example**

{% highlight VoltMx %}
var appwindow = voltmx.application.getAppWindow();
appwindow.showBackButton = true;	
{% endhighlight %}

* * *

</details>
<details close markdown="block"><summary>skin</summary>

* * *

This property applies a skin to the entire title bar.

### Syntax

{% highlight VoltMx %}
appwindow.skin
{% endhighlight %}

### Type

String

### Read/Write

Read + Write

### Remarks

The default value for this property is null (system theme).

Passing a null or empty string resets the property to the system theme.

**BackgroundColor** and **ForegroundColor** are picked from valid skins. The rest of the skin properties are ignored.

Availability

Windows 10

**Example**

{% highlight VoltMx %}
var appwindow = voltmx.application.getAppWindow();
appwindow.skin = "skin1";
{% endhighlight %}

* * *

</details>
<details close markdown="block"><summary>title</summary>

* * *

This property allows you to customize the title text shown on the title bar.

### Syntax

{% highlight VoltMx %}
appwindow.title
{% endhighlight %}

### Type

String

### Read/Write

Read + Write

### Remarks

The default value for this property is an empty string.

Any string is allowed but it should not be too long or the title will be truncated.

Pass a null or empty string to reset the title. Set the new title by providing a valid string.

The application name will always be displayed on the title bar with the given title added to it.

### Availability

Windows 10

**Example**

{% highlight VoltMx %}
appwindow.title = "some text";
appwindow.title = "";
{% endhighlight %}

* * *

![](resources/prettify/onload.png)
</details>