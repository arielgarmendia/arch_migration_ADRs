# FRONTEND work: Wire new endpoints generated from removal of old backend structures

## Context and Problem Statement

Right after the execution of [`Assumption 1: Removal of Views and Conrtrollers use of ViewModel, ViewData and/or ViewBag structures. Move the processes to specific domain microservices`](ADRs/assumption1.md), we need to execute this one.

> Context

- We have a new set of endpoints gouped in domain specific context, either in new domain bounded microservices or added to existing domain microservices.
- Those endpoints represent operations coming from old nackend structures such as *ViewMode*, *ViewData* and/or *ViewBag*.
- We assume we have will documented all these processes and we also have a set of i.e. *Postman* collections.

> Problem Statement

- We need to integrate all those new endpoints in html pages using frontend components based in *Vue*, *Angular* and/or *React* frameworks.
- Connsider this the post rendering of the *Views* in *MVC* pattern.

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
> **Pros**
> - Removing all the backend side of the *MVC* app will allow to speed up the loading process.
> - Clients will have a smoother navigation experience when browsing the website.
> - Faster maintenance process.

> [!CAUTION]  
>
> **Cons**
> - Depending on the size and complexity of the *MVC* backend, this enterprise could be time-consuming and somehow tedious.
> - Will require a big testing work, in order to obtain the same functionality as before.
> - Will probably need a full-stop in developing new features in the "old" *MVC* code, otherwise there´s a high risk of not including them in the new migration.
