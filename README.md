# Several solutions for the transformation of an MVC monolith
Here we provide a few ADRs, based on several assumptions, after further analysis of the generic challenge description.

## The challenge: ARCHITECTURE MIGRATION:
- *"You must provide solutions for the transformation of an MVC monolith that includes several
domains into bounded context microservices architecture and SPA Frontend."*
- *"Our expectation is that you could provide several solutions with your assumptions, pros and cons
and a high-level delivery approach and steps."*

## Assumptions, strategies and migration paths proposals:

### We can devide the solutions in two iterations:

1. Backend:

	***IF*** **All API endpoints reside in domain specific microservices** ***THEN*** 

	a. For this specific case we need to only migrate the frontend side. Please refer to iteration 2.a.
	
	***ELSE***

	b. [`Assumption 1: Some API endpoints reside in domain specific microservices and others reside in the MVC monolith.`](ADRs/assumption1.md)

2. Frontend:
	a. ***IF*** (All API endpoints reside in domain specific microservices) ***THEN*** [`Assumption 2`](ADRs/assumption2.md)

	
	***ELSE***
	b. Comes right after iteration 1.b has been done. [`Assumption 3: Some API endpoints reside in domain specific microservices and others reside in the MVC monolith.`](ADRs/assumption3.md)