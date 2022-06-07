# HTTP

##Basic
1. Resources
2. Messages
3. Connections
4. Security
5. Hardware

## 1. Resources

URL - Uniform Resource Locator
http://www.food.com/

http://www.food.com/recipe/grilled-cauliflower
Lets breakdown this url

### 2. URL Scheme
http://  << URL Scheme
URL Scheme describes how to access a particular resource. In this case Hyper Text Transfer Protocol(HTTP).
Some more example of URL Scheme is 

ftp://server.com/download/xyz.pdf
ftp:// << File Transfer Protocol

mailto://xyz@example.com
mailto:// << for email address.


So everything after :// is specific to a particular Scheme.

### 3. Host
http://www.food.com/recipe/grilled-cauliflower

food.com << Host. It tells my browser which computer in the internet is hosting the resource.
My computer will use the Domain Name System(DNS) to know food.com == 204.78.50.82(Ip address)
so
http://www.food.com/recipe/grilled-cauliflower == http://www.204.78.50.82/recipe/grilled-cauliflower

### 4. URL Path
http://www.food.com/recipe/grilled-cauliflower

/recipe/grilled-cauliflower << url path.

### 5. Port Number :
http://food.com:80/recipe/grilled-cauliflower

:80 << port number. It's the default port num for HTTP request

### 6. Query
http://bing.com/search?q=asdjksahd

search << URL Path
?q=asdjksahd  << Query

### 7. Fragment
http://wikipedia.org/wiki/jabuticaba#Description

#Dscrption << Fragment

### 8. Character Encoding

The printable ASCII Character 

Lower case Alphabet, Upper case Alphabet, digits and some few special character $_.+'(),

Unfortunately you still can transmit UNSAFE character in url but they need to be "%" encoded or url encoded 

Space	%20  "  	%22   < 	%3C  >  	%3E etc.


For more info [Visit here](https://developers.google.com/maps/url-encoding)

Almost every web framework have API for URL encoding.

### 9. Content Type

When A Host/Server get an request it returns a resource and also a content type its also known as media type of the resource.
The content type server will specify rely on the Multipurpose Internet Mail Extension (MIME).

For more info[Visit here](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types#audio_and_video_types)

ex : application/pdf is for .pdf file

### 10. Content Negotiation

Different country/language can request server for same resources. Now question is which version server should return ?
Thats where the content negotiation mechanism comes in. 

A client can also send request with media type that it will accept.


### 11 Message Type

HTTP > HTTP1.1 define language that can understand every client and server on the internet.
It defines messages can exchange on the web.

There are two types of messages.
1. HTTP Request . Client sends to the server
2. HTTP Response. Server sends back to the client


### 12 HTTP Request Methods

GET : Retrieve a resource
POST : Update a resource
PUT : Store a resource
DELETE : Remove a resource
HEAD : Retrieve the headers for a resource

Many more but HTML specification only use GET and POST

### Safe vs Unsafe

GET is safe because its only allow to read and view not editing
POST is unsafe because its usually changes resources in the server

POST/Redirect/GET.
After POST operation server redirect to another url and then GET for displaying resource. this is called
POST/Redirect/GET

### Request Messages

[method] [URL] [version]  << Start line
[headers]
[body]

For GET request there is no [body] . There will be one or more [headers]
