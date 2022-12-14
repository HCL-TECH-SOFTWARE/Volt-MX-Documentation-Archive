---
layout: "documentation"
category: "iris_widget_prog_guide"
---
                               

You are here: Creating an TextBox Using a Constructor: voltmx.ui.TextBox2

TextBox2 Widget
===============

The TextBox widget enables you to get a single-line input from users. This widget can accept input from the users in the form of numbers or text.

Here are some of scenarios where you can use a TextBox widget:

*   Getting the username and password on a login screen and the details on a sign-up screen
*   Entering purchase details while shopping online
*   Searching through a list of data to provide the relevant search results
*   Providing details while booking a flight or hotel

Some key features of the TextBox widget are as follows:

**Various Input Types:** Customize the soft keypad of any device. You can specify whether the soft keypad should be numeric or not, whether it should have cancel, search, done, or next and previous buttons, and much more.

**Text Masking:** Mask the entered text for security purposes. This feature is useful when you are designing password and payment details page.

**Searching through a list:** Provide a list of search items, and the TextBox widget can search through the list and generate search results. For instance, while providing the address of a user, you can create a list with all the states of a country. If the user types an alphabet, all the states that start with the alphabet A are displayed.

**Restricting Input:** Set certain characters that you do not want a user to use as input. This is useful when you want the user to decide a username for your application. If you want the user to not enter certain characters, for example, ‘$#@’. You can restrict the usage of these characters by using a TextBox widget.

> **_Note:_** In Windows platform, when a FlexForm has multiple TextArea/ TextBox widgets, and none of the widgets are in focus, the focus control of the form moves to the first focussable widget. This will also make the Form scroll up to the first widget.

Widgets are normally added to your application using Volt MX Iris, but can also be added from code. For general information on using widgets in Volt MX Iris, see [Designing an Application]({{ site.baseurl }}/docs/documentation/Iris/iris_user_guide/Content/Part_II_CreatingAnApplication.html) in the [Iris User Guide]({{ site.baseurl }}/docs/documentation/Iris/iris_user_guide/Content/Introduction.html).

For general information on the TextBox2 widget see the []({{ site.baseurl }}/docs/documentation/Iris/iris_user_guide/Content/Button.html)[TextBox2]({{ site.baseurl }}/docs/documentation/Iris/iris_user_guide/Content/TextBox2.html) topic in the Volt MX Iris User Guide.

This widget supports drag and drop of text for iOS 11 on iPad.

The TextBox widget capabilities can be broadly categorized into the following:

*   [Layout](#layout)
*   [Data Management](#data-management)
*   [Animations](#animations)
*   [User Input Handling](#user-input-handling)
*   [UI Appearance](#ui-appearance)
*   [Enabling RTL](#enabling-rtl)
*   [Miscellaneous](#miscellaneous)
*   [Configurations Common To All Widgets](#configurations-common-to-all-widgets)

#### Layout

  
| Properties | Description |
| --- | --- |
| [anchorPoint](TextBox_Properties.html#anchorPo) | Specifies the anchor point of the widget bounds rectangle using the widget's coordinate space. |
| [bottom](TextBox_Properties.html#bottom) | Determines the bottom edge of the widget and is measured from the bottom bounds of the parent container. |
| [centerX](TextBox_Properties.html#centerX) | Determines the center of a widget measured from the left bounds of the parent container. |
| [centerY](TextBox_Properties.html#centerY) | Determines the center of a widget measured from the top bounds of the parent container. |
| [contentAlignment](TextBox_Properties.html#contentAlignment) | Specifies the alignment of the text for a widget with respect to its boundaries. |
| [height](TextBox_Properties.html#height) | Determines the height of the widget and measured along the y-axis. |
| [left](TextBox_Properties.html#left) | Determines the lower left corner edge of the widget and is measured from the left bounds of the parent container. |
| [maxHeight](TextBox_Properties.html#maxHeigh) | Specifies the maximum height of the widget and is applicable only when the height property is not specified. |
| [maxWidth](TextBox_Properties.html#maxWidth) | Specifies the maximum width of the widget and is applicable only when the width property is not specified. |
| [minHeight](TextBox_Properties.html#minHeigh) | Specifies the minimum height of the widget and is applicable only when the height property is not specified. |
| [minWidth](TextBox_Properties.html#minWidth) | Specifies the minimum width of the widget and is applicable only when the width property is not specified. |
| [padding](TextBox_Properties.html#padding) | Defines the space between the content of the widget and the widget boundaries. |
| [paddingInPixel](TextBox_Properties.html#paddingInPixel) | Indicates if the padding is to be applied in pixels or in percentage. |
| [right](TextBox_Properties.html#right) | Determines the lower right corner of the widget and is measured from the right bounds of the parent container. |
| [top](TextBox_Properties.html#top) | Determines the top edge of the widget and measured from the top bounds of the parent container. |
| [width](TextBox_Properties.html#width) | Determines the width of the widget and is measured along the x-axis. |
| [zIndex](TextBox_Properties.html#zIndex) | Specifies the stack order of a widget. |

   

| Events | Description |
| --- | --- |
| [doLayout](TextBox_Events.html#doLayout) | This event is invoked for every widget when the widget position and dimensions are computed. |

 

#### Data Management

| Properties | Description |
| --- | --- |
| [autoCapitalize](TextBox_Properties.html#autoCapi) | Specifies the character capitalization behavior. |
| [autoComplete](TextBox_Properties.html#autoComp) | autoComplete property enables users to quickly find and select from a prepopulated list of values as they type, leveraging searching and filtering. |
| [autoCorrect](TextBox_Properties.html#autoCorr) | Determines whether auto-correction is enabled or disabled during typing. |
| [autoFilter](TextBox_Properties.html#autoFilt) | Specifies if the input characters you enter in the TextBox widget must be matched against the filterList and possible matches be displayed. |
| [autoSuggestions](TextBox_Properties.html#autoSuggestions) | Used to enable or disable suggestions such as spell checker, predictive text and corrections in the application. |
| [closeButtonText](TextBox_Properties.html#closeBut) | Specifies the text to replace the "Done" button that appears in the Keypad (opens when you select a textbox). |
| [isSensitiveText](TextBox_Properties.html#isSensitiveText) | Used to secure the text entered in a TextBox widget. |
| [filterList](TextBox_Properties.html#filterLi) | The values you enter in the TextBox are matched against this list and possible matches are displayed. |
| [keyboardActionLabel](TextBox_Properties.html#keyboardActionLabel) | Specifies the text to be displayed in action key of the keyboard. |
| [maxTextLength](TextBox_Properties.html#maxTextL) | Specifies the maximum number of characters that the text field can accept. |
| [placeholder](TextBox_Properties.html#placehol) | Specifies a short hint that describes the expected value of an input field (example, a sample value or a short description of the expected format). |
| [restrictCharactersSet](TextBox_Properties.html#restrictCharactersSet) | Restricts users from entering a set of input characters from the soft keyboard in the TextBox widget. |
| [secureTextEntry](TextBox_Properties.html#secureText) | Specifies whether the text entered by the user will be secured using a mask character, such as asterisk or dot. |
| [text](TextBox_Properties.html#text) | Specifies a general or descriptive text for the TextBox widget. |
| [textInputMode](TextBox_Properties.html#textInpu) | Specifies the type of input characters that a user can enter into the TextBox widget. |

 

| Methods | Description |
| --- | --- |
| [clone](TextBox_Methods.html#clone) | When this method is used on a container widget, then all the widgets inside the container are cloned. |

 

| Events | Description |
| --- | --- |
| [onBeginEditing](TextBox_Events.html#onbeginediting) | This is an event callback that is invoked by the platform when the user clicks within the TextBox and is about to start editing. |
| [onCancel](TextBox_Events.html#onCancel) | This event is a callback that is invoked by the platform then the user performs a click action on the Cancel button. |
| [onDone](TextBox_Events.html#onDone) | This event is a callback that is invoked by the platform then the user performs a click action on the Go or Enter button. |
| [onEndEditing](TextBox_Events.html#onendedi) | This is an event callback that is invoked by the platform. |
| [onTextChange](TextBox_Events.html#ontextchange) | This is an event callback triggered when text in the text box changes. |

#### Animations

| Methods | Description |
| --- | --- |
| [animate](TextBox_Methods.html#animate) | Applies an animation to the widget. |

 

| Properties | Description |
| --- | --- |
| [transform](TextBox_Properties.html#transfor) | Contains an animation transformation that can be used to animate the widget. |
| [widgetSwipeMove](TextBox_Properties.html#widgetSwipeMove) | Used to enable and configure the left or right swipe actions for a widget. |

#### 3D Touch

| Methods | Description |
| --- | --- |
| [registerForPeekandPop](TextBox_Methods.html#register) | Registers a widget to enable 3D Touch peek and pop gestures. |
| [setOnPeek](TextBox_Methods.html#setOnPek) | Sets and overrides the existing onPeekCallback for the widget. |
| [setOnPop](TextBox_Methods.html#setOnPop) | Sets and overrides the existing onPeekCallback for the widget. |
| [unregisterForPeekandPop](TextBox_Methods.html#unregist) | Unregisters a widget from 3D Touch peek and pop gestures. |

#### User Input Handling

| Methods | Description |
| --- | --- |
| [addGestureRecognizer](TextBox_Methods.html#addGestureRecognizer) | Allows you to set a gesture recognizer for a specified gesture for a specified widget. |
| [removeGestureRecognizer](TextBox_Methods.html#removeGestureRecognizer) | Allows you to remove the specified gesture recognizer for the specified widget. |
| [setGestureRecognizer](TextBox_Methods.html#setGestureRecognizer) | Allows you to set a gesture recognizer for a specified gesture for a specified widget. |

 

| Events | Description |
| --- | --- |
| [onBackKeyPress](TextBox_Events.html#onBackKeyPress) | This event callback is invoked when the back button of an Android mobile device is clicked. |
| [onKeyBoardDidHide](TextBox_Events.html#onKeyboardDidHide) | This event callback is invoked when the soft keyboard of an Android device has been closed. |
| [onKeyboardDidShow](TextBox_Events.html#onKeyboardDidShow) | This event callback is invoked after the soft keyboard of an Android device appears. |
| [onKeyboardWillHide](TextBox_Events.html#onKeyboardWillHide) | This event callback is invoked when the soft keyboard of an Android device is about to close. |
| [onKeyboardWillShow](TextBox_Events.html#onKeyboardWillShow) | This event callback is invoked when the soft keyboard of an Android device is about to appear. |
| [onKeyDown](TextBox_Events.html#onKeyDow) | This is an event callback that is invoked by the platform when the user presses a key (on the keyboard). |
| [onKeyUp](TextBox_Events.html#onKeyUp) | This is an event callback that is invoked by the platform when the user releases a key (on the keyboard). |
| [onTouchEnd](TextBox_Events.html#onTouchEnd) | An event callback is invoked by the platform when the user touch is released from the touch surface. |
| [onTouchMove](TextBox_Events.html#onTouchMove) | An event callback is invoked by the platform when the touch moves on the touch surface continuously until movement ends. |
| [onTouchStart](TextBox_Events.html#onTouchStart) | An event callback is invoked by the platform when the user touches the touch surface. |
| [onScrollWidgetPosition](TextBox_Events.html#onScrollWidgetPosition) | This event callback is invoked by the platform when the widget location position gets changed on scrolling. |

| Properties | Description |
| --- | --- |
| [isSelectable](TextBox_Properties.html#isSelectable) | Enables you to select the content inside the TextBox |
| [smartDashes](TextBox_Properties.html#smartDashes) | Allows you to insert hyphens without space in the text. |
| [smartInsertDelete](TextBox_Properties.html#smartInsertDelete) | Enables you to add a space when you copy and paste a text. |
| [smartQuotes](TextBox_Properties.html#smartQuotes) | Enables you to add curly quotes in the text. |
| [textCopyable](TextBox_Properties.html#textCopyable1) | Enable or disable the cut, copy and, paste of the text. |

#### UI Appearance

| Properties | Description |
| --- | --- |
| [backgroundColor](TextBox_Properties.html#backgrou) | Specifies the background color of the widget in hex format. |
| [backgroundColorMultiStepGradient](TextBox_Properties.html#backgroundColorMultiStepGradient) | Specifies the multi-step gradient color for the background of the widget. |
| [backgroundColorTwoStepGradient](TextBox_Properties.html#backgroundColorTwoStepGradient) | Specifies the two-step gradient color for the background of the widget. |
| [backgroundImage](TextBox_Properties.html#backgroundImage) | Sets the image for the background of the widget. |
| [borderColor](TextBox_Properties.html#borderColor) | Specifies the border color of the widget. |
| [borderColorGradient](TextBox_Properties.html#borderColorGradient) | Specifies the multi-step gradient color for the border of the widget. |
| [borderStyle](TextBox_Properties.html#borderStyle) | Specifies the border style for the widget. |
| [borderWidth](TextBox_Properties.html#borderWidth) | Specifies the width of the border for the widget in pixels. |
| [cornerRadius](TextBox_Properties.html#cornerRadius) | Specifies the radius of the border for the widget. |
| [disabledStateSkinProperties](TextBox_Properties.html#disabledStateSkinProperties) | Specifies the skin properties that define the look and feel of the widget, when the widget is disabled or blocked. |
| [focusStateSkinProperties](TextBox_Properties.html#focusStateSkinProperties) | Specifies the skin properties that define the look and feel of the widget, when the widget is in focus. |
| [fontColor](TextBox_Properties.html#fontColor) | Specifies the font color of the widget. |
| [fontFamily](TextBox_Properties.html#fontFamily) | Specifies the font family for the font of the widget. |
| [fontSize](TextBox_Properties.html#fontSize) | Specifies the font size for the widget in percentage (%) units. |
| [fontStyle](TextBox_Properties.html#fontStyle) | Specifies the font style for the widget. |
| [fontWeight](TextBox_Properties.html#fontWeight) | Specifies the weight for the font of the widget. |
| [hoverStateSkinProperties](TextBox_Properties.html#hoverStateSkinProperties) | Specifies the skin properties that define the look and feel of the widget, when the cursor hovers on the widget. |
| [pressedStateSkinProperties](TextBox_Properties.html#pressedStateSkinProperties) | Specifies the skin properties that define the look and feel of the widget, when the widget is pressed or clicked. |
| [shadowColor](TextBox_Properties.html#shadowColor) | Specifies the color for the shadow of the widget. |
| [shadowOffset](TextBox_Properties.html#shadowOffset) | This property specifies the current coordinates of the shadow region in the widget. |
| [shadowRadius](TextBox_Properties.html#shadowRadius) | Specifies the radius for the blur value of the shadow. |
| [textShadowColor](TextBox_Properties.html#textShadowColor) | Specifies the color for the text shadow of the widget. |
| [textShadowOffset](TextBox_Properties.html#textShadowOffset) | This property specifies the current coordinates of the text shadow region in the widget. |
| [textShadowRadius](TextBox_Properties.html#textShadowRadius) | Specifies the radius for the blur value of the text shadow. |
| [keyboardAppearance](TextBox_Properties.html#keyboardAppearance) | Allows you to set the on screen keyboard to a dark or light color scheme. |
| [keyBoardStyle](TextBox_Properties.html#keyBoard) | When you interact with a TextBox widget, a keyboard is displayed. |
| [leftViewImage](TextBox_Properties.html#leftView) | Specifies an optional image to be displayed on the left-hand side of a TextBox widget. |
| [nativeListFieldFocusSkin](TextBox_Properties.html#nativeLi) | Specifies the skin that is applied to a focused item in the native popup. |
| [nativeListFieldSkin](TextBox_Properties.html#nativeLi2) | Specifies the skin that is applied to each item in the native popup (the list of items are displayed and a pop up appears just below the text field) that appears when you enter a value in the TextBox. |
| [opacity](TextBox_Properties.html#opacity) | Specifies the opacity of the widget. |
| [shadowType](TextBox_Properties.html#shadowType) | Sets a type of the shadow effect to apply to the TextBox Widget. |
| [shadowDepth](TextBox_Properties.html#shadowDepth) | Defines the depth of the shadow effect applied to the TextBox Widget. |
| [showClearButton](TextBox_Properties.html#showClea) | Specifies if a "Clear" button must be provided. |
| [showCloseButton](TextBox_Properties.html#showClos) | Specifies if the "Done" button that appears in the keypad (opens when you select text box) must be visible or not. |
| [skin](TextBox_Properties.html#skin) | Specifies the look and feel of the widget when not in focus. |
| [viewType](TextBox_Properties.html#viewType) | Specifies the appearance of the Textbox as Search view or a textbox to accept text input. |

#### Enabling RTL

| Properties | Description |
| --- | --- |
| [retainContentAlignment](TextBox_Properties.html#retainContentAlignment) | Helps to retain the content alignment of the widget while applying RTL. |
| [retainFlexPositionProperties](TextBox_Properties.html#retainFlexPositionProperties) | Helps to retain the left, right and padding properties while applying RTL. |
| [retainFlowHorizontalAlignment](TextBox_Properties.html#retainFlowHorizontalAlignment) | Enables you to change the horizontal flow of the widget from left to right. |

#### Miscellaneous

| Methods | Description |
| --- | --- |
| [getBadge](TextBox_Methods.html#getBadge) | Enables you to read the badge value (if any) attached to the specified widget. |
| [setBadge](TextBox_Methods.html#setBadge) | Enables you to set the badge value to the given widget at the upper, right corner of the widget. |

| Properties | Description |
| --- | --- |
| [cursorType](TextBox_Properties.html#cursorType) | Specifies the type of the mouse pointer used. |
| [inputAccessoryViewType](TextBox_Properties.html#inputAccessoryViewType) | The extra buttons (or controls) allow specific operations needed by your application, such as moving to the next or previous text field, making the keyboard disappear and so on. The area above the keyboard is known as Input Accessory View |
| [enableHapticFeedback](TextBox_Properties.html#enableHapticFeedback) | Allows you to enable or disable haptic feedback on the TextBox widget. |
| [toolTip](TextBox_Properties.html#toolTip) | Specifies the hint text when the cursor hovers over a widget, without clicking it. |

#### Configurations Common To All Widgets

| Methods | Description |
| --- | --- |
| [blur](TextBox_Properties.html#blur) | Enables you to make the widget look unfocused. |
| [convertPointFromWidget](TextBox_Methods.html#convertPointFromWidget) | Allows you to convert the coordinate system from a widget to a point (receiver's coordinate system). |
| [convertPointToWidget](TextBox_Methods.html#convertPointToWidget) | Allows you to convert the coordinate system from a point (receiver's coordinate system) to a widget. |
| [enable](TextBox_Properties.html#enable) | Allows you to make a widget visible but not actionable. |
| [removeFromParent](TextBox_Methods.html#removeFromParent) | Allows you to remove a child widget from a parent widget. |
| [setEnabled](TextBox_Methods.html#setEnabled) | Specifies the widget that must be enabled or disabled. |
| [setFocus](TextBox_Methods.html#setFocus) | Specifies the widget on which there must be focus. |
| [setVisibility](TextBox_Methods.html#setVisibility) | Use this method to set the visibility of the widget. |

| Properties | Description |
| --- | --- |
| [accessibilityConfig](TextBox_Properties.html#accessibilityConfig) | Enables you to control accessibility behavior and alternative text for the widget. |
| [enable](TextArea_Properties.html#enable) | Allows you to make a widget visible but not actionable. |
| [enableCache](TextBox_Properties.html#enableCa) | Enables you to improve the performance of Positional Dimension Animations. |
| [id](TextBox_Properties.html#id) | id is a unique identifier of TextBox consisting of alpha numeric characters. |
| [info](TextBox_Properties.html#info) | A custom JSObject with the key value pairs that a developer can use to store the context with the widget. |
| [isVisible](TextBox_Properties.html#isVisibl) | This property controls the visibility of a widget on the form. |
| [Parent](TextBox_Properties.html#parent) | Helps you access the parent of the widget. |

| Events | Description |
| --- | --- |
| [postOnclickJS](TextBox_Events.html#postonclickjs) | This event allows the developer to execute custom javascript function after the onClick callback of the widget is invoked. |
| [preOnclickJS](TextBox_Events.html#preonclickjs) | This event allows the developer to execute custom javascript function before the onClick callback of the widget is invoked. |

TextBox2 Widget Basics
----------------------

You can use the TextBox widget to provide a field where a user can enter input text.  
For example, in the "Login" page of an Application, you can place two TextBox widgets for _Login_ _Password_ fields and instruct the users to enter their login credentials in those fields.

#### Creating an TextBox Using a Constructor: voltmx.ui.TextBox2

{% highlight voltMx %}
var mytextbox = new voltmx.ui.TextBox2 (basicConf, layoutConf, pspConf);
{% endhighlight %}

*   **basicConf** is an object with basic properties.
*   **layoutConf** is an object with layout properties.
*   **pspConf** is an object with platform specific properties.

> **_Note:_** The configuration properties should be passed only in the respective configuration objects otherwise they are ignored.

Example

{% highlight voltMx %}//Defining the properties for a Textbox with isVisible: true.
var txtBasic = {
    id: "textBox1",
    placeholder: "enter text",
    maxTextLength: 20,
    isVisible: true,
    autoCapitalize: constants.TEXTBOX_AUTO_CAPITALIZE_SENTENCES
};

var txtLayout = {
    padding: [5, 5, 5, 5],
    margin: [5, 5, 5, 5],
    containerWeight: 100,
    hExpand: true,
    widgetAlignment: constants.WIDGET_ALIGN_TOP_LEFT
};

var txtPSP = {
    pasteboardType: constants.TEXTBOX_PASTE_BOARD_TYPE_SYSTEM_LEVEL,
    keyboardActionLabel: constants.TEXTBOX_KEYBOARD_LABEL_GOOGLE
};
//Creating the Textbox.
var textBox1 = new voltmx.ui.TextBox2(txtBasic, txtLayout, txtPSP);

//Reading the autoCapitalize of the Textbox.	
alert("Textbox autoCapitalize ::" + textBox1.autoCapitalize);
{% endhighlight %}

For backward compatibility with support for all deprecated properties and behaviors, use the constructor **voltmx.ui.TextBox**.

{% highlight voltMx %}
var myTextBox = new voltmx.ui.TextBox(basicConf, layoutConf, pspConf)
{% endhighlight %}

### Changing the Text Size through the Larger Text option in iOS

You can now change the text size of TextBox widget through the Larger Text option from Settings -> General -> Accessibility -> Larger Text in iOS.

To support this feature, you must implement the 'dynamicTypeList' dictionary in the voltmx.application.setApplicationBehaviors function as follows:

{% highlight voltMx %}voltmx.application.setApplicationBehaviors({
    dynamicTypeList: {
        enableChangeTextSizeFromAccessibility: true,
        fontTextStyle: constants.FONT_TEXT_STYLE_BODY
    }
});
{% endhighlight %}

Input Parameters

*   enableChangeTextSizeFromAccessibility (BOOL): If set to true, you can change the text size through the Larger Text option from Settings -> General -> Accessibility -> Larger Text in iOS. Otherwise, the text size will not be changed.
    
*   fontTextStyle: This is the font style applied on the TextBox widget. If you pass only the enableChangeTextSizeFromAccessibility key-value pair in the dictionary and don’t send the fontTextStyle key-value pair, the default value for fontTextStyle will be constants.FONT\_TEXT\_STYLE\_BODY. The values for fontTextStyle are as follows:
    *   constants.FONT\_TEXT\_STYLE\_BODY
        
    *   constants.FONT\_TEXT\_STYLE\_HEADLINE
        
    *   constants.FONT\_TEXT\_STYLE\_SUBHEADLINE
        
    *   constants.FONT\_TEXT\_STYLE\_FOOTNOTE
        
    *   constants.FONT\_TEXT\_STYLE\_CAPTION1
        
    *   constants.FONT\_TEXT\_STYLE\_CAPTION2
        
    *   constants.FONT\_TEXT\_STYLE\_TITLE1 (available in iOS 9.0 and later)
        
    *   constants.FONT\_TEXT\_STYLE\_TITLE2 (available in iOS 9.0 and later)
        
    *   constants.FONT\_TEXT\_STYLE\_TITLE3 (available in iOS 9.0 and later)
        
    *   constants.FONT\_TEXT\_STYLE\_CALLOUT (available in iOS 9.0 and later)
        
    *   constants.FONT\_TEXT\_STYLE\_LARGETITLE (available in iOS 11.0 and later)

Platform Availability

*   iOS

Limitations

*   If you enable this feature, the font size and font family from the respective skin is not respected.
    
*   This feature is available only in iOS.
    

### Customizing Appearance

You can customize the appearance of the TextBox widget using the following properties:

*   widgetAlignment: Specifies the alignment of the widget.
*   margin: Defines the space around the widget.
*   padding: Defines the space between the content of the widget and the widget boundaries.
*   skin: Specifies the skin.
*   focusSkin: Specifies the focus skin.

