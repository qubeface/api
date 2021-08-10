# QubeFace API


QubeFace
---------
---------

### PROPERTIES ###

| Property                | Type           | Description                                                                                       |
| ----------------------- | -------------- | ------------------------------------------------------------------------------------------------- |
| `id` | `string` | The unique QubeFace ID. This ID must be the same as the `id` of the HTML div container. This property is mendatory. |
| `effect` | `string` | Defines the kind of the transition effect. The possible values if this property corresponds to the values of the CSS property `transition-timing-function`. Default value is `ease-in-out`. |
| `backgroundColor` | `string` | The color of the cube as CSS background-color of the cube faces. Default value is `rgba(255,255,255,.85)`. |
| `spinDurationSeconds` | `number` | The spin animation duration in seconds. Default value is 0.7 seconds. |
| `actLock` | `boolean` | The action lock flag. Set the value 'true' to prevent the animation transformation. The flag is also "true" if the cube animation is running. Default value is `false`. |
| `sizePx` | `number` | The size of the cube in pixels. Default value is 400. |
| `startFace` | `string` | Defines the start face of the cube faces. The values are "front", "back", "left", "right", "top" and "bottom". Default value is "front". |
| `enableEventsWhileSpinning` | `boolean` | Enable events while spinning with this boolean flag. Default value is disabled, to prevent unwanted clicks or touch events. |
| `disableUnpresentFaces` | `boolean` | Set this flag to 'true' to disable all the form elements of the unfocused cube faces whenever the cube spins. This disabling can also handle already disabled form elements (like input or textarea). Default value is 'false'. |
| `stopSwipe` | `boolean` | Stops or reactivates swipe. This flag works only if swipe was enabled before. Default value is 'false'. |
| `stopSwipeX` | `boolean` | Stops or reactivates vertical swipe. This flag works only if swipe was enabled before. Default value is 'false'. |
| `stopSwipeY` | `boolean` | Stops or reactivates horizontal swipe. This flag works only if swipe was enabled before. Default value is 'false'. |
| `stopSwipeRight` | `boolean` | Stops or reactivates swipe right. This flag works only if swipe was enabled before. Default value is 'false'. |
| `stopSwipeLeft` | `boolean` | Stops or reactivates swipe left. This flag works only if swipe was enabled before. Default value is 'false'. |
| `stopSwipeUp` | `boolean` | Stops or reactivates swipe up. This flag works only if swipe was enabled before. Default value is 'false'. |
| `stopSwipeDown` | `boolean` | Stops or reactivates swipe down. This flag works only if swipe was enabled before. Default value is 'false'. |
| `borderWidth` | `number` | Cube border width in pixels as numeric value. When using a border, the cube size is retained (because the border is an inset). Default value is 0 (zero for no border). |
| `borderColor` | `string` | Cube border color as CSS border-color. Default color is white. |
| `borderStyle` | `string` | Cube border style as CSS border-style. Default value is `solid`. |
| `boxShadow` | `string` | The CSS box-shadow effect of the cube faces. Default value is `inset 0 0 20px rgba(0,0,0,.2)`. Set this value to null to define a cube without box-shadow effect. |
| `textAlign` | `string` | The CSS text-align to handle the text positions of all cube faces. Default value is 'center'. |
| `perspectivePx` | `number` | The perspective depth in pixels of the cube. Default value is 800. |
| `perspectiveOrigin` | `string` | The CSS perspective-origin of the cube. To change this property edit the horizontal perspective with a percentage value and the vertical perspective with a pixel value as '50% 100px'. The default value depends on the QubeFace `sizePx` property and was determined by the cube initialization. |
| `front` | `string` as HTML string | The initial face content of the front face. Set a text as string or HTML content. Take care that the content size is not bigger than the cube size of the properties `sizePx` and his `borderWidth`. For dynamically set/reset of content use the `setFront(value)` method. |
| `right` | `string` as HTML string | The initial cube face content of the right face. Set a text as string or HTML content. Take care that the content size is not bigger than the cube size of the properties `sizePx` and his `borderWidth`. For dynamically set/reset of content use the `setRight(value)` method. |
| `back` | `string` as HTML string | The initial cube face content of the back face. Set a text as string or HTML content. Take care that the content size is not bigger than the cube size of the properties `sizePx` and his `borderWidth`. For dynamically set/reset of content use the `setBack(value)` method. |
| `left` | `string` as HTML string | The initial cube face content of the left face. Set a text as string or HTML content. Take care that the content size is not bigger than the cube size of the properties `sizePx` and his `borderWidth`. For dynamically set/reset of content use the `setLeft(value)` method. |
| `top` | `string` as HTML string | The initial cube face content of the top face. Set a text as string or HTML content. Take care that the content size is not bigger than the cube size of the properties `sizePx` and his `borderWidth`. For dynamically set/reset of content use the `setTop(value)` method. |
| `bottom` | `string` as HTML string | The initial cube face content of the bottom face. Set a text as string or HTML content. Take care that the content size is not bigger than the cube size of the properties `sizePx` and his `borderWidth`. For dynamically set/reset of content use the `setBottom(value)` method. |
| `frontBgColor` | `string` | The initial cube face color as CSS background-color of the front face. |
| `rightBgColor` | `string` | The initial cube face color as CSS background-color of the right face. |
| `backBgColor` | `string` | The initial cube face color as CSS background-color of the back face. |
| `leftBgColor` | `string` | The initial cube face color as CSS background-color of the left face. |
| `topBgColor` | `string` | The initial cube face color as CSS background-color of the top face. |
| `bottomBgColor` | `string` | The initial cube face color as CSS background-color of the bottom face. |


### FUNCTIONS ###

| Function                | Type of parameter(s)    | Description                                                                                       |
| ----------------------- | ----------------------- | ------------------------------------------------------------------------------------------------- |
| `init()` |   | Initialize the QubeFace and start rendering with given definitions.  |
| `onSwipe(actionContent, swipeDirection)` | `JS-string/function, string` | This method sets a swipe action. for a swipe direction like up/down/left/right/vertical/horizontal/general. The parameter `actionContent` sets the action content as string with JavaScript content or as function type. The parameter `swipeDirection` makes a specific swipe action definition depending on swipe direction(s). This swipe direction options are: up/down/left/right/vertical/horizontal/general. The default value is 'general'. |
| `afterSwipe(actionContent, swipeDirection)` | `JS-string/function, string` | This method sets a swipe action after the swipe animation finished. It is for swipe directions like up/down/left/right/vertical/horizontal/general. The parameter `actionContent` sets the action content as string with JavaScript content or as function type. The parameter `swipeDirection` makes a specific swipe action definition depending on swipe direction(s). This swipe direction options are: up/down/left/right/vertical/horizontal/general. The default value is 'general'. |
| `setFront(value)` | `string/HTML` | Set the front cube face dynamically with text or HTML. |
| `setRight(value)` | `string/HTML` | Set the right cube face dynamically with text or HTML. |
| `setBack(value)` | `string/HTML` | Set the back cube face dynamically with text or HTML. |
| `setLeft(value)` | `string/HTML` | Set the left cube face dynamically with text or HTML. |
| `setTop(value)` | `string/HTML` | Set the top cube face dynamically with text or HTML. |
| `setBottom(value)` | `string/HTML` | Set the bottom cube face dynamically with text or HTML. |
| `moveToFace(faceName)` | `string` | Animated move to another initial defined cube side of the 3D cube (cube face) by faceName: front/back/left/right/top/bottom. |
| `addHeadCss(css)` | `string` | Add CSS as string to the HTML head. |
| `spinToFront()` |   | Animated spin to the front cube face. |
| `spinToRight()` |   | Animated spin to the right cube face. |
| `spinToBack()` |   | Animated spin to the back cube face. |
| `spinToLeft()` |   | Animated spin to the left cube face. |
| `spinToTop()` |   | Animated spin to the top cube face. |
| `spinToBottom()` |   | Animated spin to the bottom cube face. |
| `showFaceInstantly(faceName)` | `string` | Display an initial defined cube side of the 3D cube (cube face) instantly by faceName: front/back/left/right/top/bottom. |
| `remove()` |   | Remove the cube. This removes all HTML containers of this QubeFace (like cube and his wrapper) and the DOM content. So all cube faces are also removed. |
| `fadeOut()` |   | Start fade-out effect. |
| `fadeIn()` |   | Start fade-in effect. |
| `explode(animTimeMsec, animEffect, particleDistancePx, isWithFadeOut)` | `number, string, number, boolean` | Starts an explosion effect and remove the cube. This destructs all six cube faces. The parameter `animTimeMsec` defines the animation time in milliseconds. Default value is 500 milliseconds. The parameter `animEffect` must corresponds to the values of the CSS property `animation-timing-function`. Default value is `ease-out`. The parameter `particleDistancePx` defines how far the six particles fly. Default value is `ease-out`. Default value depends on the cube size `sizePx`. The parameter `isWithFadeOut` defines if the animation should also use a fade-out effect. This option is enabled on default. |
| `autoSpinX(rotationSeconds, isSpinningRight, isRotatedBack)` | `number, boolean, boolean` | Start infinite spinning the cube vertical (starts on front-face). The parameter `rotationSeconds` defines the speed of a whole rotation. Default value is 6 seconds. The parameter `isSpinningRight` defines the spinning direction to right if it's 'true' or to left if it's 'false'. This option is enabled on default. The parameter `isRotatedBack` defines if the cube back face should be 180deg rotated. This upside-down rotation is for a better face presentation when we spin vertically. This option is enabled on default. |
| `autoSpinY(rotationSeconds, isSpinningDown)` | `number, boolean` | Start infinite spinning the cube horizontal (starts on front-face). The parameter `rotationSeconds` defines the speed of a whole rotation. Default value is 6 seconds. The parameter `isSpinningDown` defines the spinning direction to spin down if it's 'true' or to spin up if it's 'false'. This option is enabled on default. |
| `initInfiniteAnimation(animSeconds, animKeyFrameName)` | `number, string` | Initialize infinity animation style (this overrides other animations). Use `initInfiniteAnimation(0, 'stop')` to stop the infinite animation and to jump to last rotate style definition. The parameter `animSeconds` defines the seconds of the animation. The parameter `animKeyFrameName` defines the name of the animation key frame. |
| `getCurrentFace()` |   | Returns the QubeFace instance. |
| `getId()` |   | Returns the ID of this QubeFace. This corresponds to the QubeFace property `id`. |
| `enableSwipe(isSwipeVertical, isSwipeHorizontal, isGrabMouseCursor)` | `boolean, boolean, boolean` | Enable swipe for touch and mouse-swipe. Define the vertical/horizontal option initial if that usage is relevant. The parameter `isSwipeVertical` defines if the user can swipe vertically. This option is enabled on default. The parameter `isSwipeHorizontal` defines if the user can swipe horizontally. This option is enabled on default. The parameter `isGrabMouseCursor` activates if the grab mouse cursor is used. This option is disabled on default. |
| `recalibratePerspectiveOrigin(newHalfSize)` | `string` | The parameter `newHalfSize` defines the new half size of the new cube perspective. Parameter example: "100px". This parameter is mendatory. This calibrates the CSS `perpective-origin` style for cube size changes or can be used for other recalibrations on the cube wrapper's `perpective-origin`.  |
| `resetTransformPart(node, transformPart, value, isAdditionalIfNotExist, transition)` | `node, string, string, boolean, string` | Reset transform part style. A value example for the transformPart `translateX` can be "100px" or a value for transformPart `rotateX` can be "90deg". If we also use the parameter `transition` with "1s", then we can use an animated effect. If we also set style "transition" before we call this method, then we can use also an animated effect for the `resize` QubeFace method. The parameter `node` must be the DOM node like in this example: `document.querySelector('#'+qube.id)`. This parameter is mendatory. The parameter `transformPart` corresponds as a part of the CSS transform styles: "skew"/"translate"/"rotate"/"translateX"/"rotateZ"/etc. This parameter is mendatory. The parameter `value` is the value of the defined `transform` part.  This parameter is mendatory. The parameter `isAdditionalIfNotExist` determines if the `transform` part can be added if it's not there before. This option is disabled on default, but it's usefull for some animated use cases to enable it. The parameter `transition` can define the duration of an animation, example "1s". If it's missing or `null`, then it prevents the animation. |
| `resize(newSizePx)` | `number` | The parameter `newSizePx` defines the new cube size in pixels. This also resets the `sizePx` QubeFace property with the parameter value. This parameter is mendatory. |



QubeControl
-----------
-----------

### PROPERTIES ###

| Property                | Type         | Description                                                                                       |
| ----------------------- | ------------ | ------------------------------------------------------------------------------------------------- |
| `id` | `string` | The unique QubeControl ID. This ID must be the same as the `id` of the HTML div container. This property is mendatory. |
| `effect` | `string` | Defines the kind of the transition effect. The possible values if this property corresponds to the values of the CSS property `transition-timing-function`. Default value is `ease-in-out`. |
| `backgroundColor` | `string` | The color of the cube as CSS background-color of the cube. Default value is `rgba(255,255,255,.85)`. |
| `spinDurationSeconds` | `number` | The spin animation duration in seconds. Default value is 0.4 seconds. |
| `sizePx` | `number` | The size of the cube in pixels. Default value is 400. |
| `enableEventsWhileSpinning` | `boolean` | This flag enables events while spinning. It's disabled at default, to prevent unwanted click/touch events. |
| `disableUnpresentFaces` | `boolean` | Set this flag to 'true' to disable all the form elements of the unfocused cube faces whenever the cube spins. This disabling can also handle already disabled form elements (like input or textarea). Default value is 'false'. |
| `borderWidth` | `number` | Cube border width in pixels as numeric value. When using a border, the cube size is retained (because the border is an inset). Default value is 0 (zero for no border). |
| `borderColor` | `string` | Cube border color as CSS border-color. Default color is white. |
| `borderStyle` | `string` | Cube border style as CSS border-style. Default value is `solid`. |
| `boxShadow` | `string` | The CSS box-shadow effect of the cube faces. Default value is `inset 0 0 20px rgba(0,0,0,.2)`. Set this value to null to define a cube without box-shadow effect. |
| `textAlign` | `string` | The CSS text-align to handle the text positions of all cube faces. Default value is 'center'. |
| `perspectivePx` | `number` | The perspective depth in pixels of the cube. Default value is 800. |
| `perspectiveOrigin` | `string` | The CSS perspective-origin of the cube. To change this property edit the horizontal perspective with a percentage value and the vertical perspective with a pixel value as '50% 100px'. The default value depends on the QubeControl/QubeFace `sizePx` property and was determined by the cube initialization. |
| `items` | `array` | Define one or more items content to page this contents. The content can be simple values as numbers or string texts, or it can be a HTML string or it can be an instance or JSON which corresponds to `QubeItem` object structure. For more information look to the QubeItem's definition. This propery must have a minimum of one element as string or as `QubeItem` object. |
| `stepIndex` | `number` | This property defines the index of the steps as item index, starts on position zero for the first element at default. The index must be a positive integer number. This defines the index of the current item of the QubeControl `items` array. Default value is 0. |
| `endElementContent` | `string` | This defines the content which can be seen at the end of all items, after the last element was reached and all pages are done. This can be content with text or HTML as string. Default value is an empty string. examples: "End", "✓" or some HTML in a string. |
| `isEndingWithExplosion` | `boolean` | Defines if the cube ends with an explosion animation and with a removing. This is enabled as default. |
| `upValues` | `array` | Result array that contains the values of the swipe or spin decisions of the 'up' direction. The content can be the `value` if the `QubeItem` object or the value of the QubeControl `items` array itself. |
| `downValues` | `array` | Result array that contains the values of the swipe or spin decisions of the 'down' direction. The content can be the `value` if the `QubeItem` object or the value of the QubeControl `items` array itself. |
| `rightValues` | `array` | Result array that contains the values of the swipe or spin decisions of the 'right' direction. The content can be the `value` if the `QubeItem` object or the value of the QubeControl `items` array itself. |
| `leftValues` | `array` | Result array that contains the values of the swipe or spin decisions of the 'left' direction. The content can be the `value` if the `QubeItem` object or the value of the QubeControl `items` array itself. |


### FUNCTIONS ###


| Function                | Type of parameter(s)    | Description                                                                                       |
| ----------------------- | ----------------------- | ------------------------------------------------------------------------------------------------- |
| `onSwipe(actionContent, swipeDirection)` | `JS-string/function, string` | This method sets a swipe action. for a swipe direction like up/down/left/right/vertical/horizontal/general. The parameter `actionContent` sets the action content as string with JavaScript content or as function type. The parameter `swipeDirection` makes a specific swipe action definition depending on swipe direction(s). This swipe direction options are: up/down/left/right/vertical/horizontal/general. The default value is 'general'. |
| `afterSwipe(actionContent, swipeDirection)` | `JS-string/function, string` | This method sets a swipe action after the swipe animation finished. It is for swipe directions like up/down/left/right/vertical/horizontal/general. The parameter `actionContent` sets the action content as string with JavaScript content or as function type. The parameter `swipeDirection` makes a specific swipe action definition depending on swipe direction(s). This swipe direction options are: up/down/left/right/vertical/horizontal/general. The default value is 'general'. |
| `onEnd(actionContent)` | `JS-string/function` | This adds custom actions at the end of the steps. The parameter `actionContent` sets the action content as string with JavaScript content or as function type. |
| `setFront(value)` | `string/HTML` | Set the front cube face dynamically with text or HTML. |
| `remove()` |   | Remove the cube. This removes all HTML containers of this QubeControl/QubeFace (like cube and his wrapper) and the DOM content. So all cube faces are also removed. |
| `clearItems()` |   | Clear all current defined `items` of the cube. |
| `resetIndex()` |   | Resets the `stepIndex` to the value 0. |
| `restart()` |   | Resets the `stepIndex` and direction values (`upValues`, `downValues`, `rightValues`, `leftValues`) and restarts with first item of the `items` array. |
| `fadeOut()` |   | Start fade-out effect. |
| `fadeIn()` |   | Start fade-in effect. |
| `explode(animTimeMsec, animEffect, particleDistancePx, isWithFadeOut)` | `number, string, number, boolean` | Starts an explosion effect and remove the cube. This destructs all six cube faces. The parameter `animTimeMsec` defines the animation time in milliseconds. Default value is 500 milliseconds. The parameter `animEffect` must corresponds to the values of the CSS property `animation-timing-function`. Default value is `ease-out`. The parameter `particleDistancePx` defines how far the six particles fly. Default value is `ease-out`. Default value depends on the cube size `sizePx`. The parameter `isWithFadeOut` defines if the animation should also use a fade-out effect. This option is enabled on default. |
| `getId()` |   | Returns the `id` of the QubeControl. |
| `getQubeFace()` |   | Returns the QubeFace object. Use this to define QubeFace properties. |
| `concatItems(arr)` | `array as string/object/QubeItem)` | This concats new `items` as array. The parameter `arr` defines an array with strings or objects with the object structure of QubeItem. |
| `stopSwipe(isStopping)` | `boolean` | Stops or reactivates swipe. The parameter `isStopping` stops the swipe effect. Default value of the parameter is 'true'. |
| `stopSwipeX(isStopping)` | `boolean` | Stops or reactivates vertical swipe. The parameter `isStopping` stops the swipe effect. Default value of the parameter is 'true'. |
| `stopSwipeY(isStopping)` | `boolean` | Stops or reactivates horizontal swipe. The parameter `isStopping` stops the swipe effect. Default value of the parameter is 'true'. |
| `stopSwipeRight(isStopping)` | `boolean` | Stops or reactivates swipe right. The parameter `isStopping` stops the swipe effect. Default value of the parameter is 'true'. |
| `stopSwipeLeft(isStopping)` | `boolean` | Stops or reactivates swipe left. The parameter `isStopping` stops the swipe effect. Default value of the parameter is 'true'. |
| `stopSwipeUp(isStopping)` | `boolean` | Stops or reactivates swipe up. The parameter `isStopping` stops the swipe effect. Default value of the parameter is 'true'. |
| `stopSwipeDown(isStopping)` | `boolean` | Stops or reactivates swipe down. The parameter `isStopping` stops the swipe effect. Default value of the parameter is 'true'. |
| `skipToNext(spinDirection)` | `string` | This skips to next item by ignoring the item value adding to the direction values (`upValues`, `downValues`, `rightValues`, `leftValues`) arrays. The parameter `spinDirection` defines the spin direction (down/up/left/right). Default value of the parameter is 'left'. |
| `spinToNext(spinDirection, isSkipping)` | `string, boolean` | This spins to next item and adds the item value to the direction values (`upValues`, `downValues`, `rightValues`, `leftValues`) arrays, dependent on the given `spinDirection` parameter. The parameter `spinDirection` defines the spin direction (down/up/left/right). Default value of the parameter is 'left'. The parameter `isSkipping` can prevent the adding to the direction values, if it's set to 'true'. Default value of the parameter is 'false'. |
| `getItemIndex(itemId)` | `string` | Returns the item index of the `items` array by the `id` of the item (QubeItem). |
| `resize(newSizePx)` | `number` | Resize the cube. The parameter `newSizePx` defines the new cube size in pixels. This also resets the `sizePx` QubeFace property with the parameter value. This parameter is mendatory. |
| `pushDirectionValue(directionName, isSkipping)` | `string, boolean` | Push an item value to one of 4 possible selected direction categories (`upValues`, `downValues`, `rightValues`, `leftValues`) by parameter `directionName`. This function contains also the item interpreter to handle the item index. The parameter `directionName` defines the target direction (of the array properties: `upValues`, `downValues`, `rightValues`, `leftValues`) of the item value. The parameter must be a direction value of 'up', 'down', 'right' or 'down'. This parameter is mendatory. The parameter `isSkipping` prevents with the value 'true', that we push a value, so we just handle the item interpreter and the item index. Default value of the parameter is 'false'. |
 
 

QubeItem
---------
---------

itemId
--------- string/number
ID for item identification.

content
--------- string/HTML-String
Text or HTML content of the displayed cube face.

value
--------- string/number/bool/object/array
Value of the item. 

lockUp
------ bool
Prevent up spin and prevent direction value selection. Is 'false' on default.

lockLeft
-------- bool
Prevent left spin and prevent direction value selection. Is 'false' on default.

lockRight
-------- bool
Prevent right spin and prevent direction value selection. Is 'false' on default.

lockDown
-------- bool
Prevent down spin and prevent direction value selection. Is 'false' on default.

ifUpThenItemId
--------------- string/number
Jump to `itemId` of the items array when the 'up' direction was selected.

ifLeftThenItemId
--------------- string/number
Jump to `itemId` of the items array when the 'left' direction was selected.

ifRightThenItemId
--------------- string/number
Jump to `itemId` of the items array when the 'right' direction was selected.

ifDownThenItemId
--------------- string/number
Jump to `itemId` of the items array when the 'down' direction was selected.

ifUpThenIndex
--------------- number
Jump to the index of the items array when the 'up' direction was selected.

ifLeftThenIndex
--------------- number
Jump to the index of the items array when the 'left' direction was selected.

ifRightThenIndex
--------------- number
Jump to the index of the items array when the 'right' direction was selected.

ifDownThenIndex
--------------- number
Jump to the index of the items array when the 'down' direction was selected.

up
---- string/HTML-String
The QubeStar 'up' arrow content as text or HTML. If it's 'null', then the interpreter takes the content from before.
	
left
---- string/HTML-String
The QubeStar 'left' arrow content as text or HTML. If it's 'null', then the interpreter takes the content from before.

right
----- string/HTML-String
The QubeStar 'right' arrow content as text or HTML. If it's 'null', then the interpreter takes the content from before.

down
---- string/HTML-String
The QubeStar 'down' arrow content as text or HTML. If it's 'null', then the interpreter takes the content from before.

holdDirectionContent
--------------------- bool
This QubeStar flag can holds all four direction contents by setting current item contents (which aren't 'null') as QubeStar direction content if it's 'true'. The default value is 'false'.

onUp
------ function
Define an action as function which was triggered as an event, when the 'up' direction was selected. This contains an empty function as default.

onLeft
------ function
Define an action as function which was triggered as an event, when the 'left' direction was selected. This contains an empty function as default.

onRight
------ function
Define an action as function which was triggered as an event, when the 'right' direction was selected. This contains an empty function as default.

onDown
------ function
Define an action as function which was triggered as an event, when the 'down' direction was selected. This contains an empty function as default.



QubeStar
---------
---------

### PROPERTIES ###

qubeControl
----------- object/QubeControl
Define the QubeControl object for the QubeStar. This object is mendatory.

id
---- string
The ID of the QubeStar.

arrowColor
----------- string
The color of the arrows as CSS color. Default value is `rgba(144, 238, 144, 0.5)`.

arrowFocusColor
---------------- string
The color of the arrow focus effect as CSS color. Default value is `#B0E0E6`.

upLabel
-------- string/HTML-String
The 'up' arrow label content as text or HTML.

downLabel
-------- string/HTML-String
The 'down' arrow label content as text or HTML.

rightLabel
---------- string/HTML-String
The 'right' arrow label content as text or HTML.

leftLabel
---------- string/HTML-String
The 'left' arrow label content as text or HTML.

isUpLabelCentric
----------------- bool
Enable centered label for the arrow 'up' part. Default value is 'false'.

isDownLabelCentric
----------------- bool
Enable centered label for the arrow 'down' part. Default value is 'false'.

isRightLabelCentric
----------------- bool
Enable centered label for the arrow 'right' part. Default value is 'false'.

isLeftLabelCentric
----------------- bool
Enable centered label for the arrow 'left' part. Default value is 'false'.

boardSizePx
------------ number 
Star board size in pixels. It's 'null' on default. If it's 'null', then we use the QubeControl property `sizePx` multiplied by three.

arrowWidthPercent
------------------ number
Direction arrows width in percent with a value from 0 till 10. It's 'null' on default. If it's 'null', then we use the default value '100'.

arrowHeightPercent
------------------ number
Direction arrows height in percent with a value from 0 till 10. It's 'null' on default. If it's 'null', then we use the default value '100'.

arrowTranslate
-------------- number
Translate direction arrows up or down with a value from -50 till 90. It's 'null' on default. If it's 'null', then we use the default value '0'.

hasClickableArrows
------------------ bool
Enable clickable arrows as default (by special overlay), otherwise just the arrow text is clickable. It's 'true' on default.

isPagingMode
------------- bool
This flag determines the direction button effect of the cube spinning as paging mode or categorize mode. If it's 'true', then the arrow action has the spin effect like a paging, otherwise the arrow action spins to the direction of the used arrow. It's 'false' on default.



### FUNCTIONS ###


onSwipe(actionContent, swipeDirection)
------------------------ JS-string/function, string
This method sets a swipe action. for a swipe direction like up/down/left/right/vertical/horizontal/general.
The parameter `actionContent` sets the action content as string with JavaScript content or as function type.
The parameter `swipeDirection` makes a specific swipe action definition depending on swipe direction(s). This swipe direction options are: up/down/left/right/vertical/horizontal/general. The default value is 'general'.

afterSwipe(actionContent, swipeDirection)
------------------------------ JS-string/function, string
This method sets a swipe action after the swipe animation finished. It is for swipe directions like up/down/left/right/vertical/horizontal/general.
The parameter `actionContent` sets the action content as string with JavaScript content or as function type.
The parameter `swipeDirection` makes a specific swipe action definition depending on swipe direction(s). This swipe direction options are: up/down/left/right/vertical/horizontal/general. The default value is 'general'.

skipToNext(spinDirection)
------------------------------------- string
This skips to next item by ignoring the item value adding to the direction values (`upValues`, `downValues`, `rightValues`, `leftValues`) arrays.
The parameter `spinDirection` defines the spin direction (down/up/left/right). Default value of the parameter is 'left'.

spinToNext(spinDirection, isSkipping)
------------------------------------- string, bool
This spins to next item and adds the item value to the direction values (`upValues`, `downValues`, `rightValues`, `leftValues`) arrays, dependent on the given `spinDirection` parameter.
The parameter `spinDirection` defines the spin direction (down/up/left/right). Default value of the parameter is 'left'.
The parameter `isSkipping` can prevent the adding to the direction values, if it's set to 'true'. Default value of the parameter is 'false'.

resize(newBoardSizePx, isScalingCubeBySameRelation)
--------------------------------------------------- number, bool
Resize method to resize the star board which also resizes the inner cube.
The parameter `newBoardSizePx` defines the new star board size in pixels dependent on the CSS perspective. This also resets the `sizePx` QubeControl/QubeFace property with the parameter value. This parameter is mendatory.
The parameter `isScalingCubeBySameRelation` defines with 'true' that we also scale the cube with the same size relation from before. Default value of the parameter is 'true'.


