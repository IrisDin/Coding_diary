# info443

Abstraction：

Abstraction is the process of generalization. It lets us work with higher-level representations rather than low-level details.



&#x20;We can evaluate "separation" in terms of cohesion and coupling.

cohesion：

"The degree to which parts of an element are related and belong together."



coupling：

"The degree to which software elements are inter-connected (and inter-dependent)." a.k.a., the degree to which software elements are not self-contained.



Orthogonality：

If two things are orthogonal, a change to one won't change the other Orthogonality 26We want software elements to be orthogonal!



Encapsulation

Encapsulation is the process of compartmentalizing the elements of an abstraction. It hides the details in the abstraction.





## Key Design Concepts

\
**Minimal complexity**. The primary goal of design should be to minimize complexity for all the reasons just described. Avoid making "clever" designs. Clever designs are usually hard to understand. Instead make "simple" and "easy-to-understand" designs. If your design doesn't let you safely ignore most other parts of the program when you're immersed in one specific part, the design isn't doing its job.

**Ease of maintenance**. Ease of maintenance means designing for the maintenance programmer. Continually imagine the questions a maintenance programmer would ask about the code you're writing. Think of the maintenance programmer as your audience, and then design the system to be self-explanatory.

**Loose coupling**. Loose coupling means designing so that you hold connections among different parts of a program to a minimum. Use the principles of good abstractions in class interfaces, encapsulation, and information hiding to design classes with as few interconnections as possible. Minimal connectedness minimizes work during integration, testing, and maintenance.

**Extensibility**. Extensibility means that you can enhance a system without causing violence to the underlying structure. You can change a piece of a system without affecting other pieces. The most likely changes cause the system the least trauma.

**Reusability**. Reusability means designing the system so that you can reuse pieces of it in other systems.

**High fan-in**. High fan-in refers to having a high number of classes that use a given class. High fan-in implies that a system has been designed to make good use of utility classes at the lower levels in the system.

**Low-to-medium fan-out**. Low-to-medium fan-out means having a given class use a low-to-medium number of other classes. High fan-out (more than about seven) indicates that a class uses a large number of other classes and may therefore be overly complex. Researchers have found that the principle of low fan-out is beneficial whether you're considering the number of routines called from within a routine or the number of classes used within a class (Card and Glass 1990; Basili, Briand, and Melo 1996).

**Portability**. Portability means designing the system so that you can easily move it to another environment.

**Leanness**. Leanness means designing the system so that it has no extra parts (Wirth 1995, McConnell 1997). Voltaire said that a book is finished not when nothing more can be added but when nothing more can be taken away. In software, this is especially true because extra code has to be developed, reviewed, tested, and considered when the other code is modified. Future versions of the software must remain backward-compatible with the extra code. The fatal question is "It's easy, so what will we hurt by putting it in?"

**Stratification**. Stratification means trying to keep the levels of decomposition stratified so that you can view the system at any single level and get a consistent view. Design the system so that you can view it at one level without dipping into other levels.







