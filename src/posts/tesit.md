---
date: 2020-05-01
title: TESIT
tags:
- Singapore
- Melay

---

### MOZILLA DEV

***

This interim response indicates that everything so far is OK and that the client should continue the request, or ignore the response if the request is already finished.

### W3 ORG

***

The client SHOULD continue with its request. This interim response is used to inform the client that the initial part of the request has been received and has not yet been rejected by the server. The client SHOULD continue by sending the remainder of the request or, if the request has already been completed, ignore this response. The server MUST send a final response after the request has been completed.

### WIKIPEDIA

***

This means that the server has received the request headers, and that the client should proceed to send the request body (in the case of a request for which a body needs to be sent; for example, a POST request). If the request body is large, sending it to a server when a request has already been rejected based upon inappropriate headers is inefficient. To have a server check if the request could be accepted based on the request's headers alone, a client must send Expect: 100-continue as a header in its initial request and check if a 100 Continue status code is received in response before continuing (or receive 417 Expectation Failed and not continue).

### KINSTA

***

“Continue.” This means that the server in question has received your browser’s request headers, and is now ready for the request body to be sent as well. This makes the request process more efficient since it prevents the browser from sending a body request even though the headers have been rejected.

### TUTORIALS POINT

***

Only a part of the request has been received by the server, but as long as it has not been rejected, the client should continue with the request.

### W3 SCHOOLS

***

The server has received the request headers, and the client should proceed to send the request body.

### TUTORIAL REPUBLIC

This means the client should continue with its request. The server returns this response code to inform the client that the initial part of the request has been received and has not yet been rejected by the server.

### UMBARCO

The 100 Continue status code means that the initial part of the request has been received by the server and that the client should proceed with the request or ignore the response if the request has already finished.

### BELUGACDN

This response will indicate that everything so far is okay and that there are no other issues so the client can continue the request. However, the client can also ignore the response if the request is already finished.

### FALAVIOCOPES

The server has received the request headers and the client should proceed to send the request body (in the case of a request for which a body needs to be sent; for example, a POST request). Sending a large request body to a server after a request has been rejected for inappropriate headers would be inefficient. To have a server check the request’s headers, a client must send Expect: 100-continue as a header in its initial request and receive a 100 Continue status code in response before sending the body. If the client receives an error code such as 403 (Forbidden) or 405 (Method Not Allowed) then it shouldn’t send the request’s body. The response 417 Expectation Failed indicates that the request should be repeated without the Expect header as it indicates that the server doesn’t support expectations (this is the case, for example, of HTTP/1.0 servers).