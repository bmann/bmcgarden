---
wikipedia: https://en.wikipedia.org/wiki/Object-capability_model
tags:
  - programming
  - capabilities
---
The **object-capability model** is a computer security model. A capability[^capability-based-security] describes a transferable right to perform one (or more) operations on a given object. It can be obtained by the following combination:

[^capability-based-security]: [[Capability-based security]]

- An unforgeable reference (in the sense of object references or protected pointers) that can be sent in messages.
- A message that specifies the operation to be performed.

The security model relies on not being able to forge references.

- Objects can interact only by sending messages on references.
- A reference can be obtained by:

1. Initial conditions: In the initial state of the computational world being described, object A may already have a reference to object B.
2. Parenthood: If A creates B, at that moment A obtains the only reference to the newly created B.
3. Endowment: If A creates B, B is born with that subset of A's references with which A chose to endow it.
4. Introduction: If A has references to both B and C, A can send to B a message containing a reference to C. B can retain that reference for subsequent use.

In the object-capability model, _all_ computation is performed following the above rules.

Advantages that motivate [object-oriented programming](https://en.wikipedia.org/wiki/Object_(computer_science) "Object (computer science)"), such as encapsulation or [information hiding](https://en.wikipedia.org/wiki/Information_hiding "Information hiding"), [modularity](https://en.wikipedia.org/wiki/Modularity_(programming) "Modularity (programming)"), and [separation of concerns](https://en.wikipedia.org/wiki/Separation_of_concerns "Separation of concerns"), correspond to security goals such as [least privilege](https://en.wikipedia.org/wiki/Principle_of_least_privilege "Principle of least privilege") and [privilege separation](https://en.wikipedia.org/wiki/Privilege_separation "Privilege separation") in capability-based programming.

The object-capability model was first proposed by [Jack Dennis](https://en.wikipedia.org/wiki/Jack_Dennis "Jack Dennis") and Earl C. Van Horn in 1966[^dennis_vanhorn]

[^dennis_vanhorn]:  J.B. Dennis, E.C. Van Horn. [“Programming Semantics for Multiprogrammed Computations.” (PDF)](http://srl.cs.jhu.edu/pubs/SRL2003-03.pdf) Communications of the ACM, 9(3):143–155, March 1966. 