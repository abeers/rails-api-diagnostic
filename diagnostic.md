# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

What is the purpose of a backend?

```bash
// A backend allows data to persist, so a user can update data, log out, log back
// in, and see their updated data again.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```bash
// The model
```

Which layer in the MVC pattern communicates with the model?

```bash
// The controller
```

Why don't we use views in our interpretation of the MVC pattern?

```bash
// We create our own views with HTML/CSS/Javascript, so we do not use the
// default views.
```

What does C.R.U.D stand for?

```bash
// Create, Read, Update, Destroy
```

In which part of the MVC pattern can we find C.R.U.D actions?

```bash
// The model will perform the C.R.U.D actions on the database.
```

List at least 5 standard actions that C.R.U.D corresponds to?

```bash
// HTTP: POST, GET (INDEX), GET (SHOW), PATCH, DELETE
// SQL: CREATE, SELECT (*), SELECT (WHERE), UPDATE, DELETE
```

A user action fires a `GET` request for `/persons/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```bash
// - User clicks/submits a form/requests the data in some way on the client.
// - The client interprets the request and prepares a GET request to send to the server.
// - The server makes sure the request is in the expected format. If it cannot
//   understand the request, it returns an error to the client. If it can, it converts
//   it to SQL (SELECT * FROM persons WHERE id=1) and passes it to the controller.
// - The controller passes the request to the model.
// - The model retrieves the desired person and passes it back to the controller.
//   if the person does not exist, it will return an error.
// - The controller passes the person to the server.
// - The server returns the person and an HTTP status code (20*) to the client.
//   If the person could not be found, it will return an HTTP status code of 40*.
// - The client likely has a way of indicating to the user that the person has
//   been retrieved and renders the screen accordingly.
```

What is the command to generate a new rails-api app?

```bash
// rails new
```

What is the command to start an instance of a rails server?

```bash
// rails server
```

What are the commands to drop, create and migrate a database? (3 bullet points)

```bash
// db:drop
// db:create
// db:migrate
```

What is the command to scaffold a pet with a name and age attributes (hint:
Also think of the data types for each attribute)?

```bash
// rails generate scaffold Pet name:string age:integer
```
