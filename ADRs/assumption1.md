# BACKEND work: Removal of Views and Conrtrollers use of ViewModel, ViewData and/or ViewBag structures. Move the processes to specific domain microservices

## Context and Problem Statement

> Context:

When usinig an *MVC .Net* monolith strategy, the controllers send to the views important information in saveral structures created for this purpuse.

- *ViewModel*: here we normally send to the view collections or specific daya objects, in order to create information tables, specific configuration info, etc.
- *ViewData* and *ViewBag*: Used in a similar way, we pass information to the views in a dynamic way.

> Problem Statement:

- This usually has a performace impact, as it requires framework processing an more layers involved in the process.
- Dynamic structures should be avoided, giving preference to strongly typed values or *JSON* structures.

## Considered Options

* Identify for each controller/view pair, a domain bounded microservice, if it doesn´t exist then we need to create a new one.
* Create new endpoints for handling and returning configuration structures, data lists or single objects, al related to a specific domain.
* Document the outcome, to allow in a next iteration the insertion of the references to these endpoints.
* Endopoints must retorn *JSON* structures.

## Decision Outcome

- The list of new endpoints, domain bounded, which will reside in the corresponding domain microservice.
- Full documentation of the above, including parameters and results.
- Use an *OpenAPI* structured document.

### Confirmation

- Review de documentation.
- Access tests based on provided i.e. Postman collections.

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
> - Will require a mix of resources with different backgrounds, from backend devs with frontend knowledge and frontend devs specialised in the front framwork to be used.
> - Will require a big testing work, in order to obtain the same functionality as before.
> - Will probably need a full-stop in developing new features in the "old" *MVC* code, otherwise there´s a high risk of not including them in the new migration.