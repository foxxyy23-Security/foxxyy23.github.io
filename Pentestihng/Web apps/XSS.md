- what is it?
    - allows the attacker to inject and execute javascript code in the browser of a user
    - allows the attacker to take control of the application
- what kinds?
    - reflected
        - code you are injecting comes from the current HTTP request

![1b168d0d90f83c5a7a4acc9df4e187ff.png](../../_resources/1b168d0d90f83c5a7a4acc9df4e187ff.png)

- you send a request, you get a response
    - the script is in the response
- stored
    - payload is stored somewhere else
        - could be in a database to be used later
        - or just on the server side
- DOM-based
    - everything happens in the browser
- how to tell them apart?
    - DOM will only happen in the browsers, so there will not be any requests going to the server
    - There will be no traffic in Burp or developer tools
- AI definition(s)
Stored XSS, where the malicious script is permanently stored on the target servers, and DOM-based XSS, where the vulnerability is in the client side code rather than the server side code.


### DOM Lab #1
![fd43fcbef3b084944bbba1b19b8a991c.png](../../_resources/fd43fcbef3b084944bbba1b19b8a991c.png)
![8e432fb307914c840e9549b54c326306.png](../../_resources/8e432fb307914c840e9549b54c326306.png)

How to send a user to another website
![78467e542ce1db5920f266c812a131c1.png](../../_resources/78467e542ce1db5920f266c812a131c1.png)

### Stored XSS LAB
We need to see if we have html injection first
- [<h1>test</h1>]
![b48f8a9b32afef0256e9838dd5310ff1.png](../../_resources/b48f8a9b32afef0256e9838dd5310ff1.png)

 - How do we know if its XSS
	- go to our separate container and see if it appears there

![4699f4e82124b3d3da718ad194dc0546.png](../../_resources/4699f4e82124b3d3da718ad194dc0546.png)
which it does without any commands
![c1d6acdb230a50699f80cf0be0e6cc66.png](../../_resources/c1d6acdb230a50699f80cf0be0e6cc66.png)
![cc88b847854425d1a2d169759eb4004b.png](../../_resources/cc88b847854425d1a2d169759eb4004b.png)

to see if its stored- go to the other container and refresh
![c4ca9aafc852992a109c831450f951ea.png](../../_resources/c4ca9aafc852992a109c831450f951ea.png)

### Challange
![91379dbd5ac015c16116911a246b6076.png](../../_resources/91379dbd5ac015c16116911a246b6076.png)
- this script creates an image that loads from that url while brining along the document.cookie parameter or the admin_cookie

[testing](:/5f672b968b9346d4ae96381971e6cafa)