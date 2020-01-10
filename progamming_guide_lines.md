Analysis :
	1. What's the problem
	2. What the user wants?
	3. What the user needs?
	4. What can the user afford?

Design:
	1. How do we solve the problem
	2. What should be the overall  structure of the system
	3. Which parts it consist?
	4. How parts communicate with each other

Programming: Express the design in code

Testing: Make sure that the system works  correctly under all circustances
required by systematically trying out


1.the calleee deals with errors

search: BUS FACTOR ,Escalation of commitment

Technichal debt

Common causes of technical debt include: (taken from https://en.wikipedia.org/wiki/Technical_debt)

1.  Developing under unfinished requirements
 In this case development stars before design. Often done to save time,
but later on stuff has to be reworked

2. Business pressures!,

Early release is required by Bussines personal not leaving time for
 necessary changes to be  complete, builds up technical debt comprising those uncompleted changes

3. Ignoracen of development proccess
Where businesses are blind to the concept of technical debt,
 and make decisions without considering the implications.

4.Tightly-coupled components,
 where functions are not modular, the software is not flexible enough to adapt to changes in business needs.


5. Lack of a test suite,
Changes without deep testing as the result of quick  bug fixes.

6. Lack of documentation, where code is created without supporting documentation. The work to create documentation represents debt.[6]

7. Lack of collaboration, where knowledge isn't shared around the organization and business efficiency suffers, or junior developers are not properly mentored.
8. Parallel development on multiple branches accrues technical debt because of the work required to merge the changes into a single source base. The more changes done in isolation, the more debt.
9. Delayed refactoring – As the requirements for a project evolve, it may become clear that parts of the code have become inefficient or difficult to edit and must be refactored in order to support future requirements. The longer refactoring is delayed, and the more code is added, the bigger the debt.[7]:29
10. Lack of alignment to standards, where industry standard features, frameworks, technologies are ignored. Eventually integration with standards will come, and doing so sooner will cost less (similar to 'delayed refactoring').[6]:7
11. Lack of knowledge, when the developer doesn't know how to write elegant code.[7]
12. Lack of ownership, when outsourced software efforts result in in-house engineering being required to refactor or rewrite outsourced code.
13. Poor technological leadership, where poorly thought out commands are handed down the chain of command.
14. Last minute specification changes, these have potential to percolate throughout a project but no time or budget to see them through with documentation and checks.


		Reckless                      | Prudent


Deliberate	"We don't have time for design"|"We must ship now and deal with consequences (later)"


Inadvertent	"What's Layering?"             |"Now we know how we should have done it"



Activities that might be postponed include documentation, writing tests, attending to TODO comments and tackling compiler and static code analysis warnings.


Other instances of technical debt include knowledge that isn't shared around the organization and code that is too confusing to be modified easily
