# HTTP

## **HyperText**

HyperText is text which contains links to oher texts. It is not constrained to being linear.

## **What is HTTP?**

HTTP is a protocol used to read and write "resources" (data) in a simple, text-based manner.
- used for all sort of documents like HTML, CSS, JS files and anything that browser is able to download.

HTTP is a **request-response** based protocol.

1. Client (user-agent) makes request to HTTP server along with message asking for some resource (i.e webpage)
    - User-agent can also be a proxy (most of the time that is the web browser)
2. Server responds and send client requested resource

![http-requext](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview/client-server-chain.png)

## **HTTP Requests**

When a client wants to communicate with a server, it issues a request.

Every request has many components but there are two currently looking at:
- **PATH**- says what resource the client wants to act on
- **METHOD**- says what action it would like to perform

## **HTTP Methods/Verbs**

There are 9 HTTP methods but current focus on first 4.

1. **`GET`**
    - Used to get some data from the server.
2. **`POST`**
    - Used to create data.
3. **`PUT`**
    - Used for editting/updating data.
4. **`DELETE`**
    - Delete some existing data.
5. `HEAD`
6. `CONNECT`
7. `OPTIONS`
8. `TRACE`
9. `PATCH`

## **Paths and URL Structure**

In order to make a request, you need to know the URL of the resource being requested.
- URL is address of a unique resource on the web
- URL = *Uniform Resource Locator*
- **Path** is part of the URL

![url](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_URL/mdn-url-all.png)

**NOTE:** *You might think of a URL like a regular postal mail address: the scheme represents the postal service you want to use, the domain name is the city or town, and the port is like the zip code; the path represents the building where your mail should be delivered; the parameters represent extra information such as the number of the apartment in the building; and, finally, the anchor represents the actual person to whom you've addressed your mail.*

***Scheme***- protocol, usually http or https but can also be others like `mailto:`

***Authority***- usually domain name or host (IP address) and port if included.
  - domain name indicates which web server is being requested
  - port is technical "gate". Omitted for standard ports (80=http, 443=https)

***Path to resource***- path to the resource **on the web server**. Physical location of the file.

***Parameters***- list of key value pairs seperated by **&**.

***Anchor***- Anchor to another part of the resource.
- like a "bookmark" for the resource so the browser shows the "bookmarked" content.

## **Absolute vs Relative URL**

**Absolute URL** is in a place like the browser which has no context so you must provide the entire url to get the resource.

**Relative URL** are urls with context. Within our web directory and html files we can refer to other files within our directly without the need to provide the entire url (usually with a `/..`).

## **HTTP Responses**

When a server recieves a request from client, **it reads the path and method** to figure out what to do.
- i.e `GET /dogs` request may lead to server trying to fetch data about the dogs it has. After it has performed the requested action, it sends the response back. Lots of information in the response including
  - status codes
  - body

#### Status Codes

One of the information included in the response is the status code.
- The status code is how the server comminicates successful/failure operation to the client. 

[HTTP status codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_Error) :
1. 1xx informational response – the request was received, continuing process
2. 2xx successful – the request was successfully received, understood, and accepted
3. 3xx redirection – further action needs to be taken in order to complete the request
4. 4xx client error – the request contains bad syntax or cannot be fulfilled
5. 5xx server error – the server failed to fulfil an apparently valid request

Some of the most common ones are:
- `200`: Everything worked great
- `201`: The request has succeeded and a new resource has been created as a result
- `404`: **Error**, resource was not found (UNKNOWN PATH)
- `500`: Server had an error

#### Response Body

The **body** is where the data requested by client is stored


## **Headers**

Requests --> path and method
Response --> status code and body

Both req and res let programmer inject addition data as "headers" in `key-value` pair format
- (eg: `Accept-Language: fr`, `Content-Type: text/html`, etc.)
