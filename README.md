# singleton-pattern

Implementation through the inner class.

What is the peculiarity of the inner class? It allows us, again, to implement 
a lazy implementation due to the peculiarities of Java itself. 
The fact is that internal classes are loaded only when we refer to them for the 
first time - in contrast to the "external" classes, which are loaded immediately when the program starts.

It is thread-safe - due to the same feature. Why? There is such a problem - if several threads simultaneously “knock” 
on the same object, one of them can get an underloaded object. 
But there is no such thing - due to the peculiarities of loading the inner classes.
