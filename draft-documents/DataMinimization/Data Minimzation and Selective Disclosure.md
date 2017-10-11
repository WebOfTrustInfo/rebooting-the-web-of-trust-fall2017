# Data Minimization and Selective Disclosure

**Contributors**
* Lionel Wolberger, Independent
* Brent Zundel, Evernym/Sovrin
* Zachary Larson, Independent
* Irene Hernandez, Independent 
* Katryna Dow, Meeco

## Introduction
Data minimization and selective disclosure (D&S, DataMin, SelDis) are very cool applications of crypto to do magic tricks, such as proving a person is over 25 years old without revealing their birthday or even which credential vouched for the person.
These capabilities are needed for creating, storing, presenting, and verifying user-controlled credentials among other things: DataMin is one of three mitigations against privacy threats in RFC6973, it is featured in article 5, 25 of the GDPR, the USA Privacy Act of 1974 and often appears in FIPPs. This group's goal is to standardize D&S techniques for the Verifiable Claims work (to be used in Blockchain systems supporting self-sovereign identity), an official work item of the W3C Credentials Community Group. Some topics we plan to address include Merkle trees for redaction, Progressive disclosure, CL Signature schemes (Camenisch-Lysyanskaya), ZK (zero knowledge) protocols such as Fiat-Shamir, ZK Snarks and Starks.
Current known participants in this work item are:
* Lionel Wolberger
* Jan Camenisch
* Maria Dubovitskaya

## Definitions
### What is data minimization?
Data minimization is the act of limiting the amount of shared data strictly to the minimum necessary in order to successfully accomplish a task or goal.   
Data minimization has three parts:
* Content minimization – the amount of data should be strictly the minimum necessary.
* Temporal minimization – the data should be stored by the receiver strictly during the minimum amount of time necessary to execute the task
* Scope minimization – the data should only be used for the strict purpose of the active task. 
Data minimization is largely a policy decision.
See appendix for collected definitions of data minimization.

### What is selective disclosure?
Selective disclosure is the ability of an individual to granularly decide what information to share. Selective disclosure is a means by which data minimization can be achieved.
See appendix for collected definitions of selective disclosure.
### What is progressive disclosure
Progressive disclosure is the ability of an individual to gradually increase the amount of relevant data revealed as trust is built or value generated. 
See appendix for collected definitions of progressive disclosure.

## Implementation
This section is for Lionel's awesome pictures and descriptions of the flow in our use case

## Method
### Background
#### Number Theory
* Integer Factorization
* Prime Numbers
* Discrete Logarithms
* Quadratic Residues
* Finite Field Arithmetic
* Elliptic Curves
#### Cryptography
* Symmetric Encryption
* Asymmetric Encryption
* Digital Signatures
    * Diffie Helman
    * ECDSA
        * EdDSA
    * CL
    * BLS
* Zero-Knowledge Proofs
    * Fiat Shamir
    * Proof of knowledge of discrete logarithms
    * ZK Snarks
    * ZK Starks
* Hashing
* Merkle Trees
* Accumulators
   * Commitments
   * Witnesses
* Quantum Computing and Cryptography
   * Shor's Algorithm
### Verifiable Claims in Sovrin
#### Indy SDK


## Appendix
### Collected Definitions
#### Data Minimization
* GDPR Rec.39; Art.5(1)(c) definition: “The personal data should be adequate, relevant and limited to what is necessary for the purposes for which they are processed. This requires, in particular, ensuring that the period for which the personal data are stored is limited to a strict minimum. Personal data should be processed only if the purpose of the processing could not reasonably be fulfilled by other means.”
* Reducing your overall footprint of data outside of your control. Can be accomplished by using selective disclosure
* Reducing the amount of data you are sending in a payload to only the one is needed. That prevents leakage of confidential information
* Providing people with the information they need without revealing non necessary info.  If I need to prove if I am old enough without
* Best practices – your should deeply inspect your use case and come to a conclusion as to what is the minimum data you need to accomplish your goal. Don’t be greedy. Data is proved to be toxic
* Mathematical – finding a way to express the data that you wish as an equation related to the data you have
* Minimizing the amount of data to achieve your goal or communicate what you need to.
* Designing systems to operate efficiently in order to maximize privacy
* Choosing to only share the minimal amount of data about yourself or something during an interaction. 
* Trying to keep the amount of info that is being disclosed as limited as possible to the requirements of the vulnerability. The minimum is what is will lead them to move to action. 
* Always happens in a context: a relationship where the two parties are considering interacting in some way. Sending only the signals that I want to send and that are needed by the other party, hem to interact with me in a particar 
* The least amount of data needed for a system to function
* Collecting the least amount of date for the highest outcome. 
#### Selective Disclosure
* Ability to decide what info you give and how it can be used.
* Smart disclosure, allows to select what information to give based on logic. 
* Blind search. You can decide who gets to see what. 
* Means by which we achieve data minimization. Form of policies. Ability to mask attributes that you do not have to share.
* Relates to mathematical definition – the computational ability to reveal only parts of your data profile. 
* Act of communicating or revealing only what you intend to and not any peripheric data
* Having granular control over the ways in which data is shared
* Is a pattern for user interfaces allowing people to choose what to share about them during an interaction
* Method for achieving data minimization where only certain signals are being shared and there is control of who it is being shared with. That control is never perfect. The communication channel matters
* An entity having ranular control on what’s revealed
* The individual having the freedom to decide what to share or the acquirer using data minimization approach requesting the minimum amount amount of data for the maximum impact
#### Progressive Disclosure
* Procedure for increasing revelation of relevant data as the communication proceeds. As we continue to communicate we decide to reveal more information. It becomes more generous as trust builds. 
* Being able to reveal more data as you need to given certain conditions
* Information is disclosed as needed when needed.
* You can choose to increase the amount of data you disclose over time as needed. 
* Taking as little vulnerability as possible at the beginning, then gaining information and becoming willing to take on additional vulnerability by revealing more information.  Progressive trust - Trust is built thorugh step by step interactions where we start making ourselves vunerable in a very small way and we observe how this works out. Based on results we consider making ourselves further vulnerable or not. It is about increasing levels of familiarity and prediction making ( I am better able to predict your behavior). 
* Releasing information as needed
* Escalation of the previous steps in line with the value increasing. 

### References:
    * [Data Minimization and Selective Disclosure Repo] (https://github.com/w3c-ccg/data-minimization)
    * Camenisch, Lysyanskaya. [An Efficient System for Non-transferable Anonymous Credentials with Optional Anonymity Revocation] (http://www.cs.ru.nl/~jhh/pub/secsem/camenish2001idemix-clean.pdf)
    * 2010 Pfitzmann, Hansen. [A terminology for talking about privacy by data minimization: Anonymity, Unlinkability, Undetectability, Unobservability, Pseudonymity, and Identity Management] (https://www.researchgate.net/publication/234720523_A_terminology_for_talking_about_privacy_by_data_minimization_Anonymity_Unlinkability_Undetectability_Unobservability_Pseudonymity_and_Identity_Management)
    * 2013 Cooper, Tschofenig, Aboba, Peterson, Morris, Hansen, Smith, Janet. [RFC6973] (https://tools.ietf.org/html/rfc6973). The draft can also be helpful, "This document focuses on introducing terms used to describe privacy properties that support data minimization." 2012 Hansen, Tschofenig, Smith, Cooper. Privacy Terminology and Concepts. Network Working Group Internet-Draft Expires: September 13, 2012. https://tools.ietf.org/html/draft-iab-privacy-terminology-01
    * Redaction Signature Suite 2016, Draft Community Group Report 26 June 2017. Longley, Sporny. Link: https://w3c-dvcg.github.io/lds-redaction2016/  "This specification describes the Redaction Signature Suite created in 2016 for the Linked Data Signatures specification. It enables a sender to redact information in a message without invalidating the digital signature."
