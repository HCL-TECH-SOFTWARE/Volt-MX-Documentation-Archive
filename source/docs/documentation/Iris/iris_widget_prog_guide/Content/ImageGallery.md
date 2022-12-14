---
layout: "documentation"
category: "iris_widget_prog_guide"
---
                               

ImageGallery Widget
-------------------

ImageGallery represents a set of images adjacent to each other. If the images exceed the row size, they are pushed to the next line.

You can add the ImageGallery Widget only to the VBox form. This widget will be available in the Widgets palette when the VBox form is selected in the app canvas.

This section provides the following documentation on this Widget.

##### [Overviews](#imagegallery-overviews)

##### [Events](ImageGallery_Events.html)

##### [Methods](ImageGallery_Methods.html)

##### [Properties](ImageGallery_Properties.html)

The ImageGallery widget capabilities can be broadly categorized into the following:

*   [Layout](#layout)
*   [Animations](#animations)
*   [Data Management](#data-management)
*   [User Input Handling](#user-input-handling)
*   [3D Touch](#3d-touch)
*   [UI Appearance](#ui-appearance)
*   [Miscellaneous](#miscellaneous)
*   [Configurations Common To All Widgets](#configurations-common-to-all-widgets)

#### Layout

  
| Properties | Description |
| --- | --- |
| [anchorPoint](ImageGallery_Properties.html#anchorPo) | Specifies the anchor point of the widget bounds rectangle using the widget's coordinate space. |

  

#### Animations

| Methods | Description |
| --- | --- |
| [animate](ImageGallery_Methods.html#animate) | Applies an animation to the widget. |

 

| Properties | Description |
| --- | --- |
| [transform](ImageGallery_Properties.html#transfor) | Contains an animation transformation that can be used to animate the widget. |

 

#### Data Management

| Methods | Description |
| --- | --- |
| [addAll](ImageGallery_Methods.html#addAll) | Allows you to add new images to the ImageGallery. |
| [addDataAt](ImageGallery_Methods.html#addDataA) | Allows you to add/insert a new image at a given index. |
| [removeAll](ImageGallery_Methods.html#removeAll) | Removes all the images in the HorizontalImageStrip. |
| [removeAt](ImageGallery_Methods.html#removeAt) | Removes the image at the given index in the ImageGallery. |
| [setData](ImageGallery_Methods.html#setData) | Allows you to set new images to the ImageGallery. |
| [setDataAt](ImageGallery_Methods.html#setDataAt) | Allows you to set a new image at a given index. |

 

| Properties | Description |
| --- | --- |
| [data](ImageGallery_Properties.html#data) | Represents the JSObject to represent the images to be rendered in ImageGallery. |

 

#### 3D Touch

| Methods | Description |
| --- | --- |
| [registerForPeekandPop](ImageGallery_Methods.html#register) | Registers a widget to enable 3D Touch peek and pop gestures. |
| [setOnPeek](ImageGallery_Methods.html#setOnPek) | Sets and overrides the existing onPeekCallback for the widget. |
| [setOnPop](ImageGallery_Methods.html#setOnPop) | Overrides the existing onPopCallback for the widget. |
| [unregisterForPeekandPop](ImageGallery_Methods.html#unregist) | Unregisters a widget from 3D Touch peek and pop gestures. |

 

#### User Input Handling

 

| Methods | Description |
| --- | --- |
| [addGestureRecognizer](ImageGallery_Methods.html#addGestureRecognizer) | Allows you to set a gesture recognizer for a specified gesture for a specified widget. |
| [removeGestureRecognizer](ImageGallery_Methods.html#removeGestureRecognizer) | Allows you to remove the specified gesture recognizer for the specified widget. |
| [setGestureRecognizer](ImageGallery_Methods.html#setGestureRecognizer) | Allows you to set a gesture recognizer for a specified gesture for a specified widget. |

 

#### UI Appearance

| Properties | Description |
| --- | --- |
| [focusSkin](ImageGallery_Properties.html#focusSkin) | Specifies the look and feel of the widget when in focus. |
| [hoverSkin](ImageGallery_Properties.html#hoverSki) | Specifies the look and feel of a widget when the cursor hovers on the widget. |
| [navigationBarPosition](ImageGallery_Properties.html#navigationBarPosition) | Specifies the position of the navigation bar for the ImageGallery. |
| [selectedIndex](ImageGallery_Properties.html#selectedIndex) | Indicates the currently selected image in the ImageGallery. |
| [selectedItem](ImageGallery_Properties.html#selectedItem) | Returns the selected data object (input array) corresponding to the selected image of the ImageGallery. |
| [skin](ImageGallery_Properties.html#skin) | Specifies the look and feel of the ImageGallery when not in focus. |
| [spaceBetweenImages](ImageGallery_Properties.html#spaceBetweenImages) | Specifies the space between the images in the ImageGallery. |
| [viewType](ImageGallery_Properties.html#viewType) | Specifies the appearance of the Image Gallery as Default view or Page view. |
| [viewConfig](ImageGallery_Properties.html#viewConf) | Specifies the view configuration parameters when the viewType is set as IMAGE\_GALLERY\_VIEW\_TYPE\_PAGEVIEW for Desktop Web platform. |

#### Miscellaneous

| Properties | Description |
| --- | --- |
| [imageWhenFailed](ImageGallery_Properties.html#imageWhenFailed) | Specifies the image to be displayed when the remote resource is not available. |
| [imageWhileDownloading](ImageGallery_Properties.html#imageWhileDownloading) | Specifies the image to be displayed when the remote source is still being downloaded. |
| [itemsPerRow](ImageGallery_Properties.html#itemsPerRow) | Specifies the number of images to be displayed per row in an ImageGallery at a time. |
| [noofRowsPerPage](ImageGallery_Properties.html#noofRows) | Specifies the number of rows to be displayed in each page. |

 

| Methods | Description |
| --- | --- |
| [getBadge](ImageGallery_Methods.html#getBadge) | Enables you to read the badge value (if any) attached to the specified widget. |
| [setBadge](ImageGallery_Methods.html#setBadge) | Enables you to set the badge value to the given widget at the upper, right corner of the widget. |

 

| Events | Description |
| --- | --- |
| [onSelection](ImageGallery_Events.html#onSelection) | An event callback that is invoked by the platform when an Image is selected in ImageGallery. |

#### Configurations Common To All Widgets

| Methods | Description |
| --- | --- |
| [convertPointFromWidget](ImageGallery_Methods.html#convertPointFromWidget) | Allows you to convert the coordinate system from a widget to a point (receiver's coordinate system). |
| [convertPointToWidget](ImageGallery_Methods.html#convertPointToWidget) | Allows you to convert the coordinate system from a point (receiver's coordinate system) to a widget. |
| [removeFromParent](ImageGallery_Methods.html#removeFromParent) | Allows you to remove a child widget from a parent widget. |
| [setEnabled](ImageGallery_Methods.html#setEnabled) | Specifies the widget that must be enabled or disabled. |
| [setFocus](ImageGallery_Methods.html#setFocus) | Specifies the widget on which there must be focus. |
| [setVisibility](ImageGallery_Methods.html#setVisibility) | Sets the visibility of the widget. |

 

| Properties | Description |
| --- | --- |
| [accessibilityConfig](ImageGallery_Properties.html#accessibilityConfig) | Enables you to control accessibility behavior and alternative text for the widget. |
| [enableCache](ImageGallery_Properties.html#enableCa) | Enables you to improve the performance of Positional Dimension Animations. |
| [id](ImageGallery_Properties.html#id) | id is a unique identifier of ImageGallery consisting of alpha numeric characters. |
| [info](ImageGallery_Properties.html#info) | A custom JSObject with the key value pairs that a developer can use to store the context with the widget. |
| [isVisible](ImageGallery_Properties.html#isVisible) | controls the visibility of a widget on the form. |

 

| Events | Description |
| --- | --- |
| [postOnclickJS](ImageGallery_Events.html#postOncl) | Allows the developer to execute custom javascript function after the onClick callback of the ImageGallery is invoked. |
| [preOnclickJS](ImageGallery_Events.html#preOncli) | Allows the developer to execute custom javascript function when the ImageGallery is invoked. |

### ImageGallery Overviews

> **_Note:_** ImageGallery widget is not supported in BlackBerry 10 platform.

#### Creating an Image Gallery using a constructor: voltmx.ui.ImageGallery

{% highlight voltMx %}
var imagegallery1 = new voltmx.ui.ImageGallery2 (basicConf, layoutConf, pspConf)
{% endhighlight %}

*   **basicConf** is an object with basic properties.
*   **layoutConf** is an object with layout properties.
*   **pspConf** is an object with platform specific properties.

> **_Note:_** The configuration properties should be passed only in the respective configuration objects otherwise they are ignored

Example

{% highlight voltMx %}//Defining properties for ImageGallery.
var imgGalBasic = 
    { 
      id: "imgGallery",
      isVisible: true,
      skin: "gradroundfocusbtn",
      focusSkin: "gradroundfocusbtn",
      selectedIndex:3,
      spaceBetweenImages: 50
    };
var imgGalLayout = {containerWeight:50};
var imgGalPSP = {itemsPerRow:3, navigationBarPosition:"Bottom"};
//Creating the ImageGallery.
var imgGallery = new voltmx.ui.ImageGallery(imgGalBasic,imgGalLayout,imgGalPSP );
//Reading the containerWeight of ImageGallery.
alert("ImageGallery containerWeight is ::"+imgGallery.containerWeight); 
{% endhighlight %}

For backward compatibility with support for all deprecated properties and behaviors, use the constructor **voltmx.ui.ImageGallery**.

{% highlight voltMx %}
var imageGal1= new voltmx.ui.ImageGallery (basicConf, layoutConf, pspConf)
{% endhighlight %}

#### Customizing Appearance

You can customize the appearance of the Image Gallery using the following properties:

*   imageScaleMode: Specifies the scale mode for all the images in the ImageGallery.
*   referenceHeight: Specifies the reference height of the ImageGallery in pixels.
*   referenceWidth: Specifies the reference width of the ImageGallery in pixels.
*   margin: Defines the space around a widget.
*   [skin](ImageGallery_Properties.html#skin): Specify the skin to be applied to the images in the Image Gallery.
*   [focusSkin](ImageGallery_Properties.html#focusSkin): Specify the skin to be applied to the individual image in the ImageGallery when in focus.

#### Important Considerations:

*   The Image Gallery occupies 100% of the screen width.
*   On devices which have a navigation key, you can use the up or down keys to navigate through the images.
*   Form cycling is supported (i.e, if you reach the end of the gallery and if it is the last widget, you are taken to the first control of the form).
*   For Symbian, Image gallery always uses an image size of 64x64 pixels.
*   For Windows Desktop, Image Gallery widget behaves like a screen-level widget,hence [HorizontalImageStrip](Horizontal_Image_Strip.html) is preferred while using images.

