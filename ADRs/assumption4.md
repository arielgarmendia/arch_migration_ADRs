# FRONTEND work: Wire new endpoints generated from removal of old endpoints in the MVC monolith

## Context and Problem Statement

> Context

> Problem Statement

## Considered Options

* {title of option 1}
* {title of option 2}
* {title of option 3}
* … <!-- numbers of options can vary -->

## Decision Outcome

Chosen option: "{title of option 1}", because {justification. e.g., only option, which meets k.o. criterion decision driver | which resolves force {force} | … | comes out best (see below)}.

## Confirmation

- This work will follow [`Backend Assumption 1`](ADRs/assumption1.md) and [`Backend Assumption 2`](ADRs/assumption2.md) work.

{Describe how the implementation / compliance of the ADR can/will be confirmed. Is there any automated or manual fitness function? If so, list it and explain how it is applied. Is the chosen design and its implementation in line with the decision? E.g., a design/code review or a test with a library such as ArchUnit can help validate this. Note that although we classify this element as optional, it is included in many ADRs.}

## Pros and Cons of the Options

> [!IMPORTANT] 
>
> **Global Pros**
> - Removing all the backend side of the *MVC* app will allow to speed up the loading process.
> - Clients will have a smoother navigation experience when browsing the website.
> - Faster maintenance process.
> - Backend developers will only focus their work in the domain microservices.
> - **The frontend could be divided into smaller domain bounded micro-frontends, each one using it´s corresponding domain microservices, allowing more specialisation in the tribes/teams**.

> [!CAUTION]  
>
> **Global Cons**
> - Depending on the size and complexity of the *MVC* backend, this enterprise could be time-consuming and somehow tedious.
> - Will require a mix of resources with different backgrounds, from backend devs with frontend knowledge and frontend devs specialised in the front framwork to be used.
> - Will require a big testing work, in order to obtain the same functionality as before.
> - Will probably need a full-stop in developing new features in the "old" *MVC* code, otherwise there´s a high risk of not including them in the new migration.
