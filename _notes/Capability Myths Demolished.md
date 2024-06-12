---
tags:
  - paper
  - capabilities
excerpt: "We address three common misconceptions aboutcapability-based systems: the Equivalence Myth (accesscontrol list systems and capability systems are formallyequivalent), the Confinement Myth (capability systemscannot enforce confinement), and the IrrevocabilityMyth (capability-based access cannot be revoked). TheEquivalence Myth obscures the benefits of capabilitiesas compared to access control lists, while the Confinement Myth and the Irrevocability Myth lead people tosee problems with capabilities that do not actually exist.The prevalence of these myths is due to differing interpretations of the capability security model. To clear upthe confusion, we examine three different models thathave been used to describe capabilities, and define a setof seven security properties that capture the distinctionsamong them. Our analysis in terms of these propertiesshows that pure capability systems have significantadvantages over access control list systems: capabilitiesprovide much better support for least-privilegeoperation and for avoiding confused deputy problems."
author:
  - Mark Miller
  - Ka-Ping Yee
  - Jonathan Shapiro
link: https://srl.cs.jhu.edu/pubs/SRL2003-02.pdf
---
* [[Mark Miller]], Combex, Inc.
* Ka-Ping Yee, University of California, Berkeley
* Jonathan Shapiro, Johns Hopkins University
## Abstract

We address three common misconceptions about capability-based systems: the *Equivalence Myth* (access control list systems and capability systems are formally equivalent), the *Confinement Myth* (capability systems cannot enforce confinement), and the *Irrevocability Myth* (capability-based access cannot be revoked). The Equivalence Myth obscures the benefits of capabilities as compared to access control lists, while the Confinement Myth and the Irrevocability Myth lead people to see problems with capabilities that do not actually exist. The prevalence of these myths is due to differing interpretations of the capability security model. To clear up the confusion, we examine three different models that have been used to describe capabilities, and define a set of seven security properties that capture the distinctions among them. Our analysis in terms of these properties shows that pure capability systems have significant advantages over access control list systems: capabilities provide much better support for least-privilege operation and for avoiding confused deputy problems.

## A Note on the word "Capability"

Given these various interpretations of the capability model, the reader may wonder what one should adopt as the most legitimate meaning for the term capability. We should also explain why we feel justified in declaring the Irrevocability Myth and Confinement Myth to be false, rather than merely false in certain cases. We would argue that the “true” capability model is the object-capability model, because all known major capability systems take the object-based approach (for examples, see [^1] [^4] [^9] [^11] [^16] [^17] [^19] [^21]). In all of these systems, a capability is an object reference – not something that behaves like a key or ticket in the real world. Definitive books on capability-based systems [6, 16] also describe these systems from the objectcapability perspective, and explicitly characterize them as “object-based”.

We know of no security mechanisms outside of the object-capability model that have described themselves using the word capability except for “POSIX capabilities”, “Netscape capabilities”, and “split capabilities” [14]. POSIX capabilities are not generally described as “[[Capability-based security]]”. The “Netscape capabilities” extensions to Java were fairly short-lived and have not been presented in the research literature as a capability system. Moreover, both “POSIX capabilities” and “Netscape capabilities” have never been presented as security mechanisms that can stand on their own, instead only serving as an extension to existing security systems. The split capabilities model is explicitly presented in contrast to the pure capability model [14].

## References 
1. [^1]: M. Anderson, R. Pose, C. S. Wallace. A Password Capability System. The Computer Journal, 29(1), 1986, p. 1–8.
2. W. E. Boebert. On the Inability of an Unmodified Capability Machine to Enforce the ＊-Property. Proceedings of 7th DoD/NBS Computer Security Conference, September 1984, p. 291–293. Online at: http://zesty.ca/capmyths/boebert.html
3. A. Chander, D. Dean, J. C. Mitchell. Proceedings of the 14th Computer Security Foundations Workshop, June 2001, p. 27–43.
4. The E Language: Open Source Distributed Capabilities. http://erights.org/.
5. C. Ellison, B. Frantz, B. Lampson, R. Rivest, B. Thomas, T. Ylonen. SPKI Certificate Theory. IETF RFC 2693. Online at: http://www.ietf.org/rfc/rfc2693.txt
6. E. F. Gehringer. Capability Architectures and Small Objects. UMI Press, 1982.
7. L. Gong. A Secure Identity-Based Capability System. Proceedings of the 1989 IEEE Symposium on Security and Privacy, p. 56–65.
8. M. Granovetter. The Strength of Weak Ties. American Journal of Sociology 78, 1973, p. 1360–1380.
9. N. Hardy. The KeyKOS Architecture. ACM Operating Systems Review, September 1985, p. 8–25. Online at: http://www.agorics.com/Library/KeyKos/architecture.html
10. N. Hardy. The Confused Deputy (or why capabilities might have been invented). Operating Systems Review 22(4), October 1988, p. 36–38.
11. G. Heiser, K. Elphinstone, S. Russel, J. Vochteloo. Mungi: A Distributed Single Address-Space Operating System. Proceedings of the 17th Australasian Computer Science Conference, p. 271–280.
12. A. J. Herbert. A Microprogrammed Operating System Kernel. Ph. D. thesis, University of Cambridge Computer Laboratory, September 1982.
13. P. Karger. Improving Security and Performance for Capability Systems. Technical Report 149, University of Cambridge Computer Laboratory, 1988. (Ph. D. thesis.)
14. A. H. Karp, R. Gupta, G. J. Rozas, A. Banerji. Using Split Capabilities for Access Control. IEEE Software 20(1), January 2003, p. 42–49.
15. B. Lampson. Protection. Proceedings of the 5 th Annual Princeton Conference on Information Sciences and Systems, 1971, p. 437–443.
16. H. Levy. Capability-Based Computer Systems. Digital Press, Bedford, Massachusetts, 1984. Online at: http://www.cs.washington.edu/homes/levy/capabook/
17. A. S. Tanenbaum, S. J. Mullender, R. van Renesse. Using Sparse Capabilities in a Distributed Operating System. Proceedings of 6 th International Conference on Distributed Computing Systems, 1986, p. 558–563. Online at: ftp://ftp.cs.vu.nl/pub/papers/amoeba/dcs86.ps.Z
18. D. D. Redell. Naming and Protection in Extendible Operating Systems. Project MAC TR-140, MIT, November 1974. (Ph. D. thesis.)
19. J. Rees. A Security Kernel Based on the LambdaCalculus. Technical Report AIM-1564, MIT, March 1996. (Ph. D. thesis.)
20. J. H. Saltzer, M. D. Schroeder. The Protection of Information in Computer Systems. Proceedings of the IEEE 63(9), September 1975, p. 1278–1308.
21. J. S. Shapiro, J. M. Smith, D. J. Farber. EROS: A Fast Capability System. Proceedings of the 17th ACM Symposium on Operating Systems Principles, December 1999, p. 170–185.
22. J. S. Shapiro, S. Weber. Verifying the EROS Confinement Mechanism. Proceedings of the 2000 IEEE Symposium on Security and Privacy, p. 166–176.
23. K. Sitaker. Thoughts on Capability Security on the Web. Online at: http://lists.canonical.org/pipermail/kragen-tol/2000-August/000619.html
24. D. S. Wallach, D. Balfanz, D. Dean, E. W. Felten. Extensible Security Architectures for Java. In Proceedings of the 16th Symposium on Operating Systems Principles, 1997, p. 116–128. Online at: http://www.cs.princeton.edu/sip/pub/sosp97.html
25. D. Wagner, D. Tribble. A Security Analysis of the Combex DarpaBrowser Architecture. Online at: http://www.combex.com/papers/darpa-review/
26. K.-P. Yee, M. S. Miller. Auditors: An Extensible, Dynamic Code Verification Mechanism. Online at: http://www.erights.org/elang/kernel/auditors/index.html

![PDF - Capability Myths Demolished](/assets/2024/cap-myths-demolished-SRL2003-02.pdf)