---
title: "Correctly Compiling Proofs About Programs Without Proving Compilers Correct"
collection: publications
permalink: /publication/2024-09-14-correctly-compiling-proofs
excerpt: "This paper explores a technique to get guarantees about compiled programs even in the presence of an unverified, or even incorrect, compiler. Our workflow compiles programs, specifications, and proof objects, from an embedded source language and logic to an embedded target language and logic. We implement two simple imperative languages, each with its own Hoare-style program logic, and a framework for instantiating proof compilers out of compilers between these two languages that fulfill certain equational conditions in Coq. "
date: 2024-09-14
venue: 'Interactive Theorem Proving 2024'
paperurl: 'http://audreyseo.github.io/files/proof_compilers_itp_2024.pdf'
citation: '<b>Seo, Audrey</b>, Lam, Chris, Grossman, Dan, and Ringer, Talia. (2024). &quot;Correctly Compiling Proofs About Programs Without Proving Compilers Correct.&quot; <i>Interactive Theorem Proving 2024</i>.'
# bibfile: 'http://audreyseo.github.io/files/citations/proof_compilers_itp_2024.txt'
filename: proof_compilers_itp_2024.pdf
---


Guaranteeing correct compilation is nearly synonymous with compiler verification.
However, the correctness guarantees for certified compilers and translation validation can be stronger than we need. While many compilers do have incorrect behavior, 
even when a compiler bug
occurs it may not change the program's behavior meaningfully with respect to its specification. Many real-world specifications are necessarily partial in that they do not completely specify all of a program's behavior. While compiler verification and formal methods have had great success for safety-critical systems, there are magnitudes more code, such as math libraries, compiled with incorrect compilers, that would benefit from a guarantee of its partial specification.

This paper explores a technique to get guarantees about compiled programs even in the presence of an unverified, or even incorrect, compiler. Our workflow compiles programs, specifications, and proof objects, from an embedded source language and logic to an embedded target language and logic. We implement two simple imperative languages, each with its own Hoare-style program logic, and a framework for instantiating proof compilers out of compilers between these two languages that fulfill certain equational conditions in Coq. 
We instantiate our framework on four compilers: one that is incomplete, two that are incorrect, and one that is correct but unverified. We use these instances to compile Hoare proofs for several programs, and we are
able to leverage compiled proofs to assist in proofs of larger programs. Our proof compiler framework is formally proven sound in Coq.
We demonstrate how our approach enables strong target program guarantees even in the presence of incorrect compilation,
opening up new options for which proof burdens one might shoulder instead of, or in addition to, compiler correctness.