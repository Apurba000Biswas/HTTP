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

### URL Scheme
http://  << URL Scheme
URL Scheme describes how to access a particular resource. In this case Hyper Text Transfer Protocol(HTTP).
Some more example of URL Scheme is 

ftp://server.com/download/xyz.pdf
ftp:// << File Transfer Protocol

mailto://xyz@example.com
mailto:// << for email address.


So everything after :// is specific to a particular Scheme.

### Host
http://www.food.com/recipe/grilled-cauliflower

food.com << Host. It tells my browser which computer in the internet is hosting the resource.
My computer will use the Domain Name System(DNS) to know food.com == 204.78.50.82(Ip address)
so
http://www.food.com/recipe/grilled-cauliflower == http://www.204.78.50.82/recipe/grilled-cauliflower

### URL Path
http://www.food.com/recipe/grilled-cauliflower

/recipe/grilled-cauliflower << url path.
