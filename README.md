# hoverDelay
Jquery hover delay. When you hover over an element it will complete if you are using the JQuery animate, but it can be fired multiple times. This approach stops that. 
You could use the .stop(), but it stops the animation mid animation and then fires the callback function. This is also undesirable sometimes. 
You could use the .filter(':not(:animated)') approach as well, but this has problems with multiple fires can cause it to stop working for a short time. This is because it has the multiple firings in the queue. 
I tried clearing the queue, but it really wasn't very functional or clean.

So, I am using a setTimeout and a object variable. The object variable is changed on mouse enter and mouse exit. if it is not set appropriatly for the event it will not fire the setTimeout function.
