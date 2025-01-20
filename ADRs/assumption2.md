# BACKEND work: Move endpoints residing in MVC monolith to specific domain microservices

## Context and Problem Statement

> Context

As the word monolith stands, these are applications that encapsulate all services and layers in a single estructure.

Also, even when we decouple services into small external web services, and create modern microservice´s structures, we maintain some legacy access points in the monolith itself. This because either we cannot manage to identify specific domains or because we just let them live in the monolith.

> Problem Statement

If the above is a true assumption, then this is the time to do this migration work.

## Considered Options

* Identify the specific domain where these endpoints will reside.
* If a domain bounded microservice corresponding to a group of endpoints exists, then we need to move it to this one.
* If it doesn´t exist, we need to create one, and the corresponding infrastructure; then we have to move the endpoint(s) into the corresponding microservice.

## Decision Outcome

- The list of new endpoints, domain bounded, which will reside in the corresponding domain microservice.
- Full documentation of the above, including parameters and results.
- Use an *OpenAPI* structured document.
- Unit testing assurance.

### Confirmation

- Review de documentation.
- Access tests based on provided i.e. Postman collections.

## Pros and Cons of the Options

> [!IMPORTANT] 
>
> **Pros**
> - Backend developers will only focus their work in the domain microservices.
> - Domains will be more specific and will contain more robust implementations.

> [!CAUTION]  
>
> **Cons**
> - Depending on the size and complexity of the *MVC* backend, this enterprise could be time-consuming and somehow tedious.
> - Will require a big testing work, in order to obtain the same functionality as before.
> - Will probably need a full-stop in developing new features in the "old" *MVC* code, otherwise there´s a high risk of not including them in the new migration.
