# REST API Terminology

Fork and clone this repository. Then, push to github with all bad answers deleted and only the correct answers showing.


## Part I

**1. What does it mean REST?**

  REpresentational State Transfer, it is a software architecture style which allows to communicate between computer systems on the web, separating concerns and states between clients and servers, in other words, client concers have nothing to do with the server concerns, allowing direct communication between them.


**2. Who coined the REST term?**

  Roy Fielding for his doctoral tesis.

**3. In which protocol REST is based?**

  HTTP

**4. What are the main building blocks of a REST Architecture?**

  Resources (URI, which goes after the slash in the endpoint of an API)

**5. Identifying a resource is easy; you know how to access it and you even know how to request for a specific format. Since REST is using HTTP protocol as a standing point, there are some actions related to resources: CRUD operations.**

Complete the below table:


|HTTP Verb|Proposed Action|
|---------|---------------|
|GET| Consult and read. |
|POST| Create. |
|PUT| Edit/Update. |
|DELETE| Remove. |

**6. Status Code**

Another interesting standard that REST can benefit from when based on HTTP is the usage of HTTP status codes.

+ What’s is a status code?

+ Explain with your own words, the meaning of next codes:

|Status Code|Description|
|-----------|-----------|
|404| Page doent exists. |
|200| Succesful petition. |
|500| Internal Server Error. |

**7. Status Code are grouped in five sets.**

Write what are their meaning.

|Group|Description|
|-----|-----------|
|1XX| Means a petition was received and the process continues. |
|2XX| Petition is correct, was received and is understandable and accepted. |
|3XX| Clients have to complete the actions for redirecting. |
|4XX| Clients errors, like sintaxis or forbidding a client to do something. |
|5XX| Server errors, which menas that the petitition is valid but can't be completed due to an internal issue in the server. |

**8. HTTP Status Codes and Their Related Interpretation**

There are the most common status codes in HTTP responses. Please, fill with the required description.

|Status Code|Meaning|
|-----------|-------|
|200| Ok, which is the standard response to correct petitions. |
|201| Created (new resource has been created). |
|204| Petition completed succesfuly but there's no content. |
|301| Moved Permanently, so we have to be redirected to another URI. |
|400| Bad Request. |
|401| Unauthorized. |
|403| Forbidden, due to user privileges. |
|404| Not Found. |
|405| Method not allowed. |
|500| Internal server error. |

###### [To see the full list of HTTP status codes and their meaning, please refer to the RFC of HTTP 1.1](http://tools.ietf.org/html/rfc7231#section-6)

**9. How are called the points of contact between all client apps and the API?**

  endpoint

**10. The following is a good example or bad example of a named access point? And why?**

_meant to list the books in a bookstore_

+ `GET /books/action1`

  Bad example, because we don't know what does "action 1" means.

**11. What JSON does it mean?**

  JavaScript Node Notation, it is used for data exchange.

## Part II

**12. Uniform Interface**

Easy-to-remember access points are important, but so is being consistent when defining them.

You have to “refactor” the next bad design of an API. **It’s not  a good practice to name the endpoints based on the actions taken instead of the resource handled.**

At a first glance, the might not seem that bad, but consider how poor the interface is going to become as new features and resources are added to the system. Each new addition to the system causes extra endpoints to the API’s interface.

To solve this problem, you can apply the REST style to the endpoints, and thanks to HTTP, you also have verbs to indicate actions.

|Old Style|REST Style|
|---------|----------|
|`/getAllBooks`| GET /books |
|`/submitNewBook`| POST /books |
|`/updateAuthor`| PUT /authors/:id |
|`/getBooksAuthors`| GET /books/:id/authors |
|`/getNumberOfBooksOnStock`| GET /books |
|`/addNewImageToBook`| PUT /books/:id/cover |
|`/getBooksImages`| GET /books/:id/cover |
|`/addCoverImage`| POST /books/:id/cover |
|`/listBookCovers`| GET /books/:id |

Note: The :id means linking one resource to another.

**13. Anatomy of a `REQUEST`**

Make a `curl` request to _GitHub API_

```sh
$ curl -X GET https://api.github.com
```

According to the responded request, answer what does it mean the next parts from the handler:

+ _`Content-Type`_. _Write it here_
+ _`Status`_. _Write it here_
+ _`Date`_. _Write it here_
+ _`Content-Length`_. _Write it here_


###### If response is not showing those parts, ask to google how to print them in console.

```sh
# Paste the response
```
