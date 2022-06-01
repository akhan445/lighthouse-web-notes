# Cookies

HTTP --> stateless
- Each request is **independant**
- Requests can happen in **any order**

Communication between browser and application ---> through HTTP.

**Cookies** are a feature of HTTP.
- This helps distinguish each user's HTTP requests

HTTP server can tell client to remember certain keys and values ("cookies") using **`Set Cookie` header in http response**.
- All subsequent http requests from client --> server, these k:v are included in the `Cookie` header
- The server asks the client to keep reminding the server of client's identity (or other information) with every **subsequent request**

![http-cookies](https://upload.wikimedia.org/wikipedia/commons/thumb/b/bc/HTTP_cookie_exchange.svg/640px-HTTP_cookie_exchange.svg.png)

**Tracking/Third-Party Cookies** are common ways to compile long-term records of individuals' browsing histories.
- These are common with companies that have banner ads
    - if you visit multiple sites with the same ad displaying the third party advertisement can store the git 

