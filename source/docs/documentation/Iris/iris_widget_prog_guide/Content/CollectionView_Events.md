---
layout: "documentation"
category: "iris_widget_prog_guide"
---
                               


.CollectionView Events
======================

The CollectionView widget has the following events associated with it:

* * *


<details close markdown="block"><summary>onDecelerationStarted Event</summary>

* * *

This event is triggered only on iOS. It is called when deceleration starts at the end of scrolling.

### Syntax
{% highlight voltMx %}
onDecelerationStarted()
{% endhighlight %}

### Read/Write

Read + Write

### Remarks

This event is supported only on iOS

Example

{% highlight voltMx %}
//Sample code to set onDecelerationStarted event callback for CollectionView widget.

frmCollection.myCollection.onDecelerationStarted=deceleratedCallback;

function deceleratedCallback(){
      
   //Write your code here.
}
{% endhighlight %}

### Platform Availability

*   iOS

* * *

</details>
<details close markdown="block"><summary>onItemDisplay Event</summary>

* * *

This event is triggered when you display any item in the CollectionView widget.

### Syntax
{% highlight voltMx %}
onItemDisplay(  
     widgetHandle,  
     sectionIndex,  
     itemIndex,  
     itemMdl)
{% endhighlight %}

### Parameters

widgetHandle

Specifies the current CollectionView widget.

sectionIndex

Specifies the index of the section of CollectionView item

itemIndex

Specifies the index of the clicked item.

itemMdl

Specifies the item Model corresponding to the section index and item index. This parameter is valid only for iOS and SPA platforms.

### Read/Write

Read + Write

### Remarks

The onItemDisplay event provides you access to the itemMdl. This itemMdl can be animated by using the itemMdl.animate API. For more information on widget animation, refer the [Widget Animation Using Flex Forms](Animation.html#widget-level-animation-using-flex-forms) section.

### Example

{% highlight voltMx %}
function onItemDisplay(widgetHandle, sectionIndex, itemIndex, itemMdl) {
    voltmx.print("widgetHandle is:" + widgetHandle);
    voltmx.print("sectionIndex is:" + sectionIndex);
    voltmx.print("itemIndex is:" + itemIndex);
    voltmx.print("itemMdl is:" + itemMdl);
}
{% endhighlight %}

### Platform Availability

Available on all platforms.

* * *

</details>
<details close markdown="block"><summary>onItemSelect Event</summary>

* * *

This event is triggered when the user selects any item in the CollectionView.

### Syntax
{% highlight voltMx %}
onItemSelect (  
     Widget,  
     sectionIndex,  
     ItemIndex)
{% endhighlight %}

### Parameters

CollectionViewWidget

Reference to the CollectionView widget that raised the event.

SectionIndex

Specifies the index of the section to which the item belongs to.

ItemIndex

Specifies the index of item that has been clicked.

### Read/Write

Read + Write

### Remarks

This event is not raised if the **selectable** property in the **metainfo** is set to false.

In the Android platform, when a gesture or touch events are placed inside the flex template for the CollectionView widget, because of the propagation of events to the below container, the flex template may not receive the onItemSelect event.

### Platform Availability

*   iOS
*   Android
*   Windows
*   SPA

* * *

</details>
<details close markdown="block"><summary>onPull Event</summary>

* * *

An event callback that is invoked by the platform when scrolling the CollectionView widget from it's edges.

### Syntax
{% highlight voltMx %}
onPull(JSFlexContainer)
{% endhighlight %}

### Parameters

JSFlexContainer

Handle to the widget reference.

### Read/Write

Read + Write

### Remarks

For flow layout:

*   The views created from these widgets are shown when you pull or push the scrollview container from its edges.

For horizontal layout:

*   The width of the view is set to the width of the CollectionView.
*   The height is based on the height configured for the CollectionView Widget. 50dp is the default value.
*   The view is docked at the extreme end of the CollectionView widget.

For vertical layout:

*   The height of the view is set to the height of the CollectionView.
*   The view is docked at the extreme end of the CollectionView widget.

### Example

{% highlight voltMx %}
//Sample code to set onPull event callback for CollectionView widget.

frmCollection.myCollection.onPull=onPulleventCallback;

function onPulleventCallback(widgetref){
      
   voltmx.print("widget reference:" + widgetref);
}
{% endhighlight %}

### Platform Availability

*   iOS
*   Android
*   Windows
*   SPA

* * *

</details>
<details close markdown="block"><summary>onPush Event</summary>

* * *

An event callback that is invoked by the platform when scrolling the CollectionView widget widget from it's edges.

### Syntax
{% highlight voltMx %}
onPush(widgetref)
{% endhighlight %}

### Parameters

widgetref

Handle to the widget reference.

### Read/Write

Read + Write

### Remarks

For flow layout:

*   The views created from these widgets are shown when you pull or push the FlexContainer from its edges.

For horizontal layout:

*   The width of the view is set to the width of the CollectionView.
*   The height is based on the height configured for the CollectionView Widget. 50dp is the default value.
*   The view is docked at the extreme end of the CollectionView widget.

For vertical layout:

*   The height of the view is set to the height of the CollectionView.
*   The view is docked at the extreme end of the CollectionView widget.

### Example

{% highlight voltMx %}
//Sample code to set onPush event callback for CollectionView widget.

frmCollection.myCollection.onPush=onPusheventCallback;

function onPusheventCallback(widgetref){
      
   voltmx.print("widget reference:" + widgetref);
}
{% endhighlight %}

### Platform Availability

*   iOS
*   Android
*   Windows
*   SPA

* * *

</details>
<details close markdown="block"><summary>onReachingBegining Event</summary>

* * *

**onReachingBegining** gets called when scrolling reaches the beginning of the CollectionView widget.

### Syntax
{% highlight voltMx %}
onReachingBegining(CollectionViewWidget,offset)
{% endhighlight %}

### Parameters

CollectionViewWidget

Handle to the widget reference.

offset

Object containing values for x and y.

### Read/Write

Read + Write

### Example

{% highlight voltMx %}
//Sample code to set onReachingBegining event callback for CollectionView widget.

frmCollection.myCollection.onReachingBegining=onReachingBeginingCallback;

function onReachingBeginingCallback(widgetref, offset){
      
   voltmx.print("widget reference:" + widgetref + "and the offset is:" + offset);
}
{% endhighlight %}

### Platform Availability

*   iOS
*   Android
*   Windows
*   SPA

* * *

</details>
<details close markdown="block"><summary>onReachingEnd Event</summary>

* * *

onReachingEnd gets called when scrolling reaches the end of the CollectionView widget.

### Syntax
{% highlight voltMx %}
onReachingEnd(CollectionViewWidget)
{% endhighlight %}

### Parameters

CollectionViewWidget

Handle to the widget reference.

offset

Object containing values for x and y.

### Read/Write

Read + Write

### Example

{% highlight voltMx %}
//Sample code to set onReachingEnd event callback for CollectionView widget.

frmCollection.myCollection.onReachingEnd=onReachingEndCallback;

function onReachingEndCallback(widgetref, offset){
      
   voltmx.print("widget reference:" + widgetref + "and the offset is:" + offset);
}
{% endhighlight %}

### Platform Availability

*   iOS
*   Android
*   Windows
*   SPA

* * *

</details>
<details close markdown="block"><summary>onScrollStart Event</summary>

* * *

Indicates that the scroll container inside the CollectionView widget started scrolling.

### Syntax
{% highlight voltMx %}
onScrollStart (source)
{% endhighlight %}

### Parameters

source

Specifies the widget on which scrolling started.

### Read/Write

Read + Write

### Remarks

The onScrollStart event is called asynchronously. The event is triggered only when scrolling is started. When touch does not result to a scroll, this event is not raised.

### Example

{% highlight voltMx %}
//Sample code to set onScrollStart event callback for CollectionView widget.

frmCollection.myCollection.onScrollStart =onScrollStartCallback;

function onScrollStartCallback(eventobject){
      
   voltmx.print("eventobject is:" + eventobject);
}
{% endhighlight %}

### Platform Availability

*   iOS
*   Android
*   Windows
*   SPA

* * *

</details>
<details close markdown="block"><summary>onScrollTouchReleased Event</summary>

* * *

Indicates that user scrolling touch on the display is released. This callback is called asynchronously.

### Syntax
{% highlight voltMx %}
onScrollTouchReleased (source)
{% endhighlight %}

### Parameters

source

Specify the segment on which scrolling touch is released.

### Read/Write

Read + Write

### Example

{% highlight voltMx %}
//Sample code to set onScrollTouchReleased event callback for CollectionView widget.

frmCollection.myCollection.onScrollTouchReleased=onScrollTouchReleasedCallback;

function onScrollTouchReleasedCallback(eventobject){
      
   voltmx.print("eventobject is:" + eventobject);
}
{% endhighlight %}

### Platform Availability

*   iOS
*   Android
*   Windows
*   SPA

* * *

</details>
<details close markdown="block"><summary>onScrolling Event</summary>

* * *

Indicates that segment scrolling is in progress. This callback is called asynchronously.

### Syntax
{% highlight voltMx %}
onScrolling (source)
{% endhighlight %}

### Parameters

source

Specify the segment on which scrolling is in progress.

### Read/Write

Read + Write

### Example

{% highlight voltMx %}
//Sample code to set onScrolling event callback for CollectionView widget.

frmCollection.myCollection.onScrolling=onScrollingCallback;

function onScrollingCallback(eventobject){
      
   voltmx.print("eventobject is:" + eventobject);
}
{% endhighlight %}

### Platform Availability

*   iOS
*   Android
*   Windows
*   SPA

* * *

</details>
<details close markdown="block"><summary>onScrollEnd Event</summary>

* * *

Indicates that segment scrolling has come to an end.

### Syntax
{% highlight voltMx %}
onScrollEnd (source)
{% endhighlight %}

### Parameters

source

Specify the segment on which scrolling is coming to an end.

### Read/Write

Read + Write

### Remarks

The onScrollEnd callback is called asynchronously. This event is called only when the scrolling reached end of the scroll.

When multiple scrolls performed on the Segment widget, the onScrollTouchReleased is triggered whenever touch is released, but the onScrollEnd event is triggered only when the entire scrolling is ended. So when the user keeps on flinging on the display, the onScrollTouccReleased callback is triggered multiple times and onScrollEnd is triggered only once.

### Example

{% highlight voltMx %}
//Sample code to set onScrollEnd event callback for CollectionView widget.

frmCollection.myCollection.onScrollEnd=onScrollEndCallback;

function onScrollEndCallback(eventobject){
      
   voltmx.print("eventobject is:" + eventobject);
}
{% endhighlight %}

### Platform Availability

*   iOS
*   Android
*   Windows
*   SPA

* * *

</details>
<details close markdown="block"><summary>onScrollWidgetPosition Event</summary>

* * *

This event callback is invoked by the platform when the widget location position gets changed on scrolling. The onScrollWidgetPosition event returns the positional coordinates of the widget's location with respect to the screen (screenX and screenY) and the parent container (frameX and frameY). This event is invoked asynchronously, and is not available for FlexForm widget.

### Syntax
{% highlight voltMx %}
onScrollWidgetPosition()
{% endhighlight %}

### Read/Write

Read + Write

### Example

{% highlight voltMx %}
var LabelWdg = new voltmx.ui.Label(basicConf, layoutConf, pspConf);
form.add(LabelWdg);
LabelWdg.onScrollWidgetPosition = onScrollWidgetPositionCallBack;

function onScrollWidgetPositionCallBack(wdg, screenX, screenY, frameX, frameY) { //wdg : Widget that is registered for onScrollWidgetPosition.
    /*screenX : Position of widget with respect to 
the screen's X - coordinates (after downsizing the navigation bar and status bar).*/
    /*screenY : Position of widget with respect to the screen's Y - 
coordinates (after downsizing the navigation bar and status bar).*/
    //frameX : Position of widget with respect to parent container's X- coordinates.
    //frameY : Position of widget with respect to parent container's Y- coordinates.
}
{% endhighlight %}

### Platform Availability

*   Not Accessible from IDE
*   Android, iOS, SPA, and Windows

* * *

