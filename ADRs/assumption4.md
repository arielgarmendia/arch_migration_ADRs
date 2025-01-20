# FRONTEND work: Wire new endpoints generated from removal of old endpoints in the MVC monolith

## Context and Problem Statement

Right after the execution of [`Assumption 2: Move endpoints residing in MVC monolith to specific domain microservices`](assumption2.md), we need to execute this one.

> Context

- We have a new set of endpoints gouped in domain specific context, either in new domain bounded microservices or added to existing domain microservices.
- Those endpoints represent operations coming from old backend emdpoints in the monolith.
- We assume we have well documented all these processes and we also have a set of i.e. *Postman* collections.

> Problem Statement

- We need to integrate all those new endpoints in html pages using frontend components based in *Vue*, *Angular* and/or *React* frameworks.

## Considered Options

* Identify the specific html page(s) where these endpoints will be pointing at.
* Create framework specific components to interact with these new endpoints.
* Bind html components to the data returned from the endpoints, using *JSON* model.

## Decision Outcome

- Well designed components.
- Correct error processing.
- Correct validation rules.
- Unit testing assurance.

## Confirmation

- Manage to reproduce the exact behaviour as with the old *MVC* application.

## Pros and Cons of the Options

> [!IMPORTANT] 
>
> **Global Pros**
> - Removing all the backend side of the *MVC* app will allow to speed up the loading process.
> - Clients will have a smoother navigation experience when browsing the website.
> - Faster maintenance process.

> [!CAUTION]  
>
> **Global Cons**
> - Depending on the size and complexity of the *MVC* backend, this enterprise could be time-consuming and somehow tedious.
> - Will require a big testing work, in order to obtain the same functionality as before.
> - Will probably need a full-stop in developing new features in the "old" *MVC* code, otherwise there´s a high risk of not including them in the new migration.
