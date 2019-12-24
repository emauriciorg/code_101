
Notes from the book  Head First Design Patterns  by Elisabeth Freeman and Kathy Sierra

Design principle
Identify the aspects of your  application  that vary  and separethem  from what stays the same
Program to an interface not to an implementation
Favor composition over inheretance , this is for flexibility ( compisition is a class composed by others clases  or interfaces)
Design Principle
Strive for loosely coupled designs
between objects that interact.

Design Principle
Classes should be open
for extension, but closed for
modifi cation
Classes should be open for
extension but closed for
modification

Design Principle / dependenct inversion principle
Depend upon abstractions. Do not
depend upon concrete classes.High level components shall not depend on low level components, rather both depend on abstraction

Design Principle
Principle of Least Knowledge -
talk only to your immediate friends

design principle,
hollywood, dont call us, we call you

desifgn ptinviplr
sa class has only one reason to change
First pattern
The Strategy Pattern defines a family of algorithms,
encapsulates each one, and makes them interchangeable.
Strategy lets the algorithm vary independently from
clients that use it

The Observer Pattern defines a one-to-many
dependency between objects so that when one
object changes state, all of its dependents are
notified and updated automatically.

The Iterator Pattern provides a way to
access the elements of an aggregate object
sequentially without exposing its underlying
representation.

The Decorator Pattern attaches additional
responsibilities to an object dynamically.
Decorators provide a fl exible alternative to
subclassing for extending functionality

The Factory Method Pattern (inherentance then overriding)defi nes an interface
for creating an object, but lets subclasses decide which
class to instantiate. Factory Method lets a class defer
instantiation to subclasses

Simple factory "pattern"/ idiom is a one shot deal, but factory deals with multiple

The Abstract Factory (through object composition) Pattern provides an interface
for creating families of related or dependent objects
without specifying their concrete classes.

The Singleton Pattern ensures a class has only one
instance, and provides a global point of access to it.

The Command Pattern encapsulates a request as an
object, thereby letting you parameterize other objects
with different requests, queue or log requests, and support
undoable operations
classes/objetct to create in factory, aka object composition vs inheretanse

The Adapter Pattern converts the interface of a class
into another interface the clients expect. Adapter lets
classes work together that couldn’t otherwise because of
incompatible interfaces

The Facade Pattern provides a unifi ed interface to a
set of interfaces in a subsytem. Facade defi nes a higherlevel interface that makes the subsystem easier to use.


The Template Method Pattern defi nes the skeleton
of an algorithm in a method, deferring some steps to
subclasses. Template Method lets subclasses redefi ne
certain steps of an algorithm without changing the
algorithm’s structure. (coffee vs tea, common caffeine)

The Composite Pattern allows you to
compose objects into tree structures to
represent part-whole hierarchies. Composite
lets clients treat individual objects and
compositions of objects uniformly


he Hollywood Principle
Don’t call us, we’ll call you

state pattern - Allow an object to alter its
behavior when its internal state changes.
The object will appear to change its
class

The Proxy Pattern provides a surrogate or
placeholder for another object to control access to it

compound pattern

n combines two
or more patterns into a solution that
solves a recurring or general problem.

MVC

A Pattern is a solution to a problem in a context

If you find yourself in a context with a problem that has a goal
that is affected by a set of constraints, then you can apply
a design that resolves the goal and constraints and leads to a
solutio


The Design Pattern
definition tells us that
the problem consists of a
goaland aset of constraints.
Patterns gurus have a term
for these: they call them
forces. Why? Well, we’re sure
they have their own reasons, but if
you remember the movie, the force
“shapes and controls the Universe.”
Likewise, the forces in the pattern
definition shape and control the solution.
Only when a solution balances both sides of
the force (the light side: your goal, and the dark
side: the constraints) do we have a useful pattern.
This “force” terminology can be quite confusing
when you first see it in pattern discussions, but
just remember that there are two sides of the force
(goals and constraints) and that they need to be
balanced or resolved to create a pattern solution. Don’t
let the lingo get in your way and may the force be with you!
