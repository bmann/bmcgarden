---
wikipedia: https://en.wikipedia.org/wiki/Capability-based_security
tags:
  - programming
  - capabilities
---
**Capability-based security** is a concept in the design of [secure computing](https://en.wikipedia.org/wiki/Computer_security "Computer security") systems, one of the existing [security models](https://en.wikipedia.org/wiki/Computer_security_model "Computer security model"). A **capability** (known in some systems as a **key**) is a communicable, unforgeable [token](https://en.wikipedia.org/wiki/Access_token "Access token") of authority. It refers to a value that [references](https://en.wikipedia.org/wiki/Reference_(computer_science) "Reference (computer science)") an [object](https://en.wikipedia.org/wiki/Object_(computer_science) "Object (computer science)") along with an associated set of [access rights](https://en.wikipedia.org/wiki/Access_control "Access control"). A [user](https://en.wikipedia.org/wiki/User_(computing) "User (computing)") [program](https://en.wikipedia.org/wiki/Computer_program "Computer program") on a [capability-based operating system](https://en.wikipedia.org/wiki/Capability-based_operating_system "Capability-based operating system") must use a capability to access an object. Capability-based security refers to the principle of designing user programs such that they directly share capabilities with each other according to the [principle of least privilege](https://en.wikipedia.org/wiki/Principle_of_least_privilege "Principle of least privilege"), and to the operating system infrastructure necessary to make such transactions efficient and secure. Capability-based security is to be contrasted with an approach that uses [traditional UNIX permissions](https://en.wikipedia.org/wiki/File-system_permissions "File-system permissions") and [Access Control Lists](https://en.wikipedia.org/wiki/Access-control_list "Access-control list").

Although most operating systems implement a facility which resembles capabilities, they typically do not provide enough support to allow for the exchange of capabilities among possibly mutually untrusting entities to be the primary means of granting and distributing access rights throughout the system. A capability-based system, in contrast, is designed with that goal in mind.

## Introduction

Capabilities achieve their objective of improving system security by being used in place of forgeable [references](https://en.wikipedia.org/wiki/Reference_(computer_science) "Reference (computer science)"). A forgeable reference (for example, a [path name](https://en.wikipedia.org/wiki/Path_(computing) "Path (computing)")) identifies an object, but does not specify which access rights are appropriate for that object and the user program which holds that reference. Consequently, any attempt to access the referenced object must be validated by the operating system, based on the [ambient authority](https://en.wikipedia.org/wiki/Ambient_authority "Ambient authority") of the requesting program, typically via the use of an [access-control list](https://en.wikipedia.org/wiki/Access-control_list "Access-control list") (ACL). Instead, in a system with capabilities, the mere fact that a user program possesses that capability entitles it to use the referenced object in accordance with the rights that are specified by that capability. In theory, a system with capabilities removes the need for any access control list or similar mechanism by giving all entities all and only the capabilities they will actually need.

A capability is typically implemented as a [privileged](https://en.wikipedia.org/wiki/Privilege_(computing) "Privilege (computing)") [data structure](https://en.wikipedia.org/wiki/Data_structure "Data structure") that consists of a section that specifies access rights, and a section that uniquely identifies the object to be accessed. The user does not access the data structure or object directly, but instead via a [handle](https://en.wikipedia.org/wiki/Handle_(computing) "Handle (computing)"). In practice, it is used much like a [file descriptor](https://en.wikipedia.org/wiki/File_descriptor "File descriptor") in a traditional operating system (a traditional handle), but to access every object on the system. Capabilities are typically stored by the operating system in a list, with some mechanism in place to prevent the program from directly modifying the contents of the capability (so as to forge access rights or change the object it points to). Some systems have also been based on [capability-based addressing](https://en.wikipedia.org/wiki/Capability-based_addressing "Capability-based addressing") (hardware support for capabilities), such as [Plessey System 250](https://en.wikipedia.org/wiki/Plessey_System_250 "Plessey System 250").

Programs possessing capabilities can perform functions on them, such as passing them on to other programs, converting them to a less-privileged version, or deleting them. The operating system must ensure that only specific operations can occur to the capabilities in the system, in order to maintain the integrity of the security policy.

Capabilities as discussed in this article should not be confused with Portable Operating System Interface (POSIX) Capabilities. The latter are coarse-grained privileges that cannot be transferred between processes.

## Implementations

Notable research and commercial systems employing capability-based security include the following:

- [Tahoe-LAFS](https://en.wikipedia.org/wiki/Tahoe-LAFS "Tahoe-LAFS"), an open-source capability-based filesystem
- [GNOSIS](https://en.wikipedia.org/wiki/GNOSIS "GNOSIS"), an operating system developed at [Tymshare](https://en.wikipedia.org/wiki/Tymshare "Tymshare")
    - [KeyKOS](https://en.wikipedia.org/wiki/KeyKOS "KeyKOS"), successor to GNOSIS
        - EROS, The [Extremely Reliable Operating System](https://en.wikipedia.org/wiki/Extremely_Reliable_Operating_System "Extremely Reliable Operating System"), successor to KeyKOS
            - [CapROS](https://en.wikipedia.org/wiki/CapROS "CapROS"), a project to further develop the EROS code base for commercial use
- [Cambridge CAP computer](https://en.wikipedia.org/wiki/Cambridge_CAP_computer "Cambridge CAP computer")
- [Hydra (operating system)](https://en.wikipedia.org/wiki/Hydra_(operating_system) "Hydra (operating system)"), part of the C.mmp project at Carnegie Mellon University
- StarOS, part of the CM* project at [Carnegie Mellon University](https://en.wikipedia.org/wiki/Carnegie_Mellon_University "Carnegie Mellon University")
- IBM [System/38](https://en.wikipedia.org/wiki/System/38 "System/38") and [AS/400](https://en.wikipedia.org/wiki/AS/400 "AS/400")
- [Intel iAPX 432](https://en.wikipedia.org/wiki/Intel_iAPX_432 "Intel iAPX 432")
- [Plessey System 250](https://en.wikipedia.org/wiki/Plessey_250 "Plessey 250")
- [Flex](https://en.wikipedia.org/wiki/Flex_machine "Flex machine")
- [L4 microkernel family](https://en.wikipedia.org/wiki/L4_microkernel_family "L4 microkernel family"):
    - OKL4 from Open Kernel Labs
    - seL4 from NICTA
    - Fiasco.OC and NOVA from [TU Dresden](https://en.wikipedia.org/wiki/TU_Dresden "TU Dresden")
- [Amoeba](https://en.wikipedia.org/wiki/Amoeba_(operating_system) "Amoeba (operating system)") distributed operating system
- [FreeBSD](https://en.wikipedia.org/wiki/FreeBSD "FreeBSD") [Capsicum](https://en.wikipedia.org/wiki/Capsicum_(Unix) "Capsicum (Unix)")
- [Genode](https://en.wikipedia.org/wiki/Genode "Genode")
- [Google Fuchsia](https://en.wikipedia.org/wiki/Google_Fuchsia "Google Fuchsia")
- [HarmonyOS](https://en.wikipedia.org/wiki/HarmonyOS "HarmonyOS") ([HarmonyOS NEXT](https://en.wikipedia.org/wiki/HarmonyOS_NEXT "HarmonyOS NEXT")) derived from [OpenHarmony](https://en.wikipedia.org/wiki/OpenHarmony "OpenHarmony") at customised level with capability-based like features via [Access token manager](https://en.wikipedia.org/wiki/Access_token_manager "Access token manager")
- [Phantom OS]
- [[WebAssembly]] System Interface (WASI)