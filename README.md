# rest
RESTful operations cheat sheat

<br/>
##### `GET` /users
---
Collection of ressources <br/> Represented as an array
###### Possible status codes
Use `200 OK` when the collection exists

<br/>
##### `GET` /users/:id
---
Single resource by id
###### Possible status codes
Use `200 OK` when the resource exists <br/>
Use `404 Not found` when the resource with id :id does not exist

<br/>
##### `POST` /users
---
Create resource
###### Possible status codes
Use `201 Created` when the resource was created successfully - Body includes the full resource with id <br/>
Use `412 Precondition failed` when the resource is missing some parameters or has invalid values

<br/>
##### `PUT` /users/:id 
##### `PUT` /users 
---
Update (replace) the resource <br/>
Create a resource with a specific id <br/>
All fields must be given (no merge) <br/>
###### Possible status codes
Use `200 OK` when returning the updated resource
Use `201 Created` when the resource is created with a specific id
Use `204 No content` when no data is returned in the body
Use `412 Precondition failed` when he resource is missing some parameters or has invalid values

<br/>
##### `PATCH` /users/:id
---
Partially update the resource <br/>
Only update the fields given (merge)

>PUT vs PATCH are commonly misused since some older browser did not support PATCH.

###### Possible status codes
Use `200 OK` when returning the updated resource
Use `204 No content` when no data is returned in the body
Use `412 Precondition failed` when the resource is missing some parameters or has invalid values

<br/>
##### `DELETE` /users
---
Delete the collection <br/>
Probably should not be implemented
##### `DELETE` /users/:id
---
Delete the resource
###### Possible status codes
Use `204 No content` when the delete is synchronous and successful
Use `200 Accepted` when the delete will be asynchronous and the resource has been flagged as deleted but is not yet deleted
Use `200 OK` when returning information aboout the deleted resource

For more sophiticated use cases refer to : [MDN HTTP Response Code](https://developer.mozilla.org/en-US/docs/Web/HTTP/Response_codes)
