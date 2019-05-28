RS SCHOOL
===
EVENTS
---
### Everything starts from the event

#### Entrance

Our life is a series of events, we born - the event, we go to school for the first time - this is event, every year we have a very special day - the day of our birth - this is event, we're getting married - the event, we go - the event, we die - sad, but this is also the event. Programs, internet applications are “living” like people and just like people have events throughout their “life”. The ability to work with events that occur with applications is a very important part in writing any application.

#### Events

Imagine that we wrote in the address bar https://rs.school/ and clicked on “enter”, and the page of the RS School website opened. And right at this time an event is happening, yes, yes, the event “**DOMContentLoaded**” and what is happening at this time, you going to ask, and this is the answer - the browser has completely loaded the HTML and has built the DOM-tree of elements. The truth is that the DOMContentLoaded event is as simple as a cork — the DOM-tree has completely built and here it is — the event. And what's next? Then an event would happen for the object window. And it is called “**load**”. This event will happen when the browser loads the entire page, including the resources on it: styles, images, frames, etc. Finally, when a person leave the page the event called “**unload**” will occur. So that’s the way the page of the site “rs.school” living it’s life from the birth to death.

There are a huge variety of events and I can not cover even a small part in this presentation. Therefore who is interested in that always can find and read about events in Internet here, for example: https://www.w3schools.com or here https://developer.mozilla.org/en-US/docs/Web/Events.

#### And now a little bit more details about some of the events.

When the user pushed the button, when he ran a mouse over any element of the page, all these events can be processed and some actions can be taken if the event handler installed  in the page element like “pressed button” or “cursor over me”.

Let me give you an example of some mouse action events:

* click - a single mouse click (the mouse button on the left side pressed and released);
* dblclick - double click;
* contextmenu - right-click;
* mouseover - moving of the mouse cursor within the current element;
* mouseout - the mouse cursor is outside the current element.

Here are some keystroke events on the keyboard:

* keydown — a key pressed on the keyboard;
* keyup - a key released;
* keypress - a key on the keyboard pressed and released;

#### Examples of events are given, and let’s find out how to process them.

There are three approaches to assign an event handler to an element:

1. Through the attribute of an HTML tag;
2. Through the property of the object;
3. According to the W3C standard adding addEventListener().

And now more details about each of the method.

1. ##### Through the attribute of the HTML tag
       Здесь первый слайд по установке обработчика

In the example we have a page with a single button on it and using the action attribute “onlick” we set the event handler for the click action on the given page object. It turns out as soon as someone clicks the button, the event handler for the event will work, namely, those actions will occur (changing the background color of the body of the page), which are described in the function “changeColor”.

2. ##### Through the object property
       Здесь второй слайд по установке обработчика
The example is similar to the example above, we have a page with a single button on it. In tag, the script variable  the btn assigned a page object — a button, and for property the “onclick” this object, we set the handler as an anonymous function. When the user clicks on the button, the function body will be executed (the page will change color).

These two methods are relevant and can be used, but they have several disadvantages: 
* It’s difficult to write complex handlers;
* There is only one handler per one event.

All of the above methods work in modern browsers but it’s recommended to use the approach that will be used below. 

3. ##### According to the W3C standard.
The method “**addEventListener**” registers a specific event handler for any document object, object like document or like window, in general, for any object that supports events.

Syntax: 

target.addEventListener (type, listener[, useCapture]);

* type

string representing the type of event being listened.
* listener

an object that receives a notification when an event of the specified type has occurred. This should be an object that implements interface the EventListener or just a JavaScript function.

The third parameter is not mandatory and I will not be consider it’s function. Maybe later.

This method allows you to install an unlimited number of event handlers on a single document object.

Finally, here’s an example using addEventListener, similar to the examples above. For the button “Set new color”, we use the method “addEventListener” with the type of the event being listened to “click”and as the second parameter an anonymous function that will change the background color to another.

#### Removing an event handler

If we can install multiple event handlers then we can remove them. And we can do this using the **removeEventListener** method. The syntax for this method is the same as for the addEventListener method.

#### Object Event

The event object is always passed to the event handler as the first parameter and contains a lot of useful information about where and what event happened.

Here are examples for 3 methods of setting event handlers

       Здесь примеры как получить объект event в 3-х вариантах навешевания обработчика


From the event object, the handler can find out on which element it has happened, what were the coordinates of the mouse, which key was pressed and extract other useful information.

For example, for an event by mouse click (onclick), the property event.target contains there is a DOM element on which this click occurred.

#### And finally let’s talk about default browser action

Browser has its own default behavior for various events.

For example, click on the link - change the URL, click the right mouse button - show the context menu, etc.

In some cases, the browser response to the event can be removed in the handler using the following code: **event.preventDefault()**.

The topic of event handlers is quite large and today I touched the basics only. 
To be continued.

Thanks for attention.