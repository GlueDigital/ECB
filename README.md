![Starting line](/line.png)

## Glue Digital

Rúa López de Neira, 3 - Oficina 212

36202 Vigo, Pontevedra. Spain

(+34) 886 128 886

[https://glue.digital](https://glue.digital)


---

![ECB Logo](/title.png)

## Wiki

Author: Javier Blanco Thomas, CEO. Glue Digital. [javi@glue.digital](javi@glue.digital) +34616902622

## INTRODUCTION

A Zero Knowledge Proof (ZKP) system is a cryptographic protocol that establishes a method for one party to prove to another one that a statement is true, without revealing anything other than the veracity of that statement.

The inception of ZKPs began with the academic paper _“The Knowledge Complexity of Interactive Proof-Systems”1_ published in 1985, which basically exposes an efficient method of communicating a test between two machines.

It is basically a protocol through which a digital authentication process can be facilitated, and in general certain information, without the use of passwords or other confidential data. As a result of this, no information, whether from the sender or the recipient, can be compromised.

ZPF protocols are a key development on the future financial system Europe must create, because **they allow frictionless data sharing between peers without actually sharing more data than it is needed**, preventing them to generate massive data silos.

The following paper is a technical overview of a protocol we are working on, therefore it will not go into mathematical proofs or excessive bibliography. Some of the ideas contained here do not really meet the requirements to be considered ZKP, so we will refer to them as Near Zero Knowledge Proofs.

## PROBLEM TO SOLVE

When we talk about financial transactions and lending system or financial processes in which there is no initial trust among the parties involved and one of them has to demonstrate a certain solvency, we find a scenario in which the user who has to prove his solvency normally has to send to the other part a huge amount of information, generating as a result a **bureaucratic problem**, a **friction problem**, which **reduces effective competition** and above all generates by giving these companies a lot of sensitive data.

These credit companies begin to function as data silos, managing vital information for users, related to their habits, their finances... Furthermore, some of these financial entities are trying to work as data aggregators using PSD2 enhanced technologies, worsening this privacy issue.

Experience shows us that bearing in mind these credit entities have ways of using this sensitive data against users at any given time they will do it2, and also that big data silos have an increasing propensity to be hacked, we strongly believe the best solution is to limit their access to personal data, as close to Zero as possible. The greatest motivation for building this protocol is the creation of an environment where we can create transactions with less friction, less bureaucracy, more competition and always respecting the users privacy.

## PROPOSED SOLUTION

When we talk about ZKP, there are always 2 parties: the prover and the verifier. The prover wants to prove a certain fact before the verifier, without giving him access to anything but a proof, and the verifier wants proof of a certain fact or statement, in order to reduce uncertainty about a risk operation.

Our proposed solution consists in a framework, an infrastructure layer on top (or integrated) of the digital euro blockchain that allows compatible wallets to become provers and banks taking the role of verifiers, so that, when a provider wants to initiate a request that requires information from the verifier, first, the party asks for permission, and then it receives a certain proof that will help to start a certain transaction in these entities.

These proofs can be of 3 types:

* **Range proofs:** in which the verifier asks for a range, for example, that an indicative number of solvency is between one value and another, but without indicating the value.
* **Single proofs:** in which verifier you want to know a specific statement, these proofs can be considered as NZKP.
* **Structured proofs:** in which the verifier throws a complex question to the prover, and it has demonstrated with a test from which we can extract a statement. These structured tests are the most interesting, since we can ask when testing information about several accounts/wallets that the user has and sending to the verifier only a signal of solvency. As the mathematical test becomes more complex, the disaggregated data is more difficult to obtain.

This protocol is also defined by keeping the verifier audited, every time a verifier wants to launch a challenge, he has to indicate:

* **Who is the prover? Which wallet(s) does the user own?**
* **What do you want to ask?** This part is defined by the challenge itself and a clear explanation, so any user can understand what the verifier is looking for.
* **Why do you want to ask?** The verifier always has to explain his motivation, in such a way that the user understands that it benefits him.

Faced with this information combo, the prober gives permission to his wallet, to his bank account to respond to that challenge, sending only the proof. In case a Digital European ID system is already developed, we could link the protocol to it, so various wallets can respond to the challenge.

Under the protocol we create a blockchain that records all operations, so that either of the 2 parties or the regulator can access them, leaving legal proof that this verification has been done. These tests can also be used for a third party to guarantee the operation, allowing sophisticated financial operations that do not compromise the personal data of the users while at the same time enabling them to work with this technology.

We would propose the protocol as a free and open software development, so that any financial service provider can use it. Above the protocol we would create a layer of our own services for the ECB and example services and SDKs.

## THE ECONOMICS BEHIND THE PROTOCOL

When we design the economics of this protocol, 3 fundamental facts appear:

* The energy and infrastructure cost of cryptography embedded in the protocol is not negligible.
* We do not want to create a network that is filled with Spam.
* We want to create a network where we can maintain a fair regime of competition, and make it armored and resilient, so new rules can be applied if the fair game is disrupted.

This leads to the fact that we should go to a model of fees per operation, payable to the infrastructure provider.

Every time a verifier wants to launch a challenge, he pays a certain amount, if the user accepts this amount it is reduced, otherwise not, in this way we encourage the verifier to send relevant messages. In order to keep the network as less saturated and to make it scalable and functional, the cost of each operation is variable and depends on its availability. If costs rise, it will be easy for new players to enter.

A nodal structure is proposed, without barriers to entry, so that almost any qualified company can put up a node and add processing capacity to the network, at the same time that we encourage healthy competition.

## USE CASES

The following use cases are very basic applications of the protocol, applied to retail users. As can be seen, its application reduces friction, data leaks, improves competition and reduces the necessary bureaucracy for operations where trust is important.

_Apply for a rental_:

A user, the prover, wants to rent an apartment, this user has a salary of €2,000 per month, and the apartment costs €500 (lucky guy). His future landlord wants relevant information about his financial situation, and also an insurance firm only insures the payment of the rent if the user demonstrates solvency.

Using our protocol, the user would only have to give the landlord permission to prove that their monthly income moves in a certain range, perhaps starting at triple the rental price and going to infinity.

When the landlord wants to know this information, he contacts his financial institution, which in turn launches a request about the user's wallet, indicating the challenge and the reason for it. When this is answered, the landlord has irrefutable proof of the solvency of the user, without having to know how much he earns per month or any other information, being able to pass that proof to a third party interested, for example, in assuming a certain risk of non-payment.

_Apply for a consumer loan_:

The user wants to access consumer finance, but does not want to reveal more information. The financial institution wants to know if that person has the ability to repay that loan. To do this, it launches a request to the user's wallet where it asks for information on whether the user has payment obligations with any other institution, as well as the range in which these obligations move and the income received monthly, also in ranges.

With these proofs the lender can know if the person has the ability to repay the debt, without having to access any major personal information, or access to their bank accounts or any type of file.

_Service payment_:

The service provider wants to proceed to perform a service that cannot be charged in advance, the user does not want to pay it in advance either, but is willing to allow the service provider to see if it is solvent.

In this case, the service provider, through its financial institution, launches a challenge in which it points to a certain solvency or amount in the account to which it is going to charge. Our protocol will only return a ‘Yes’ or a ‘No’ response. If it is ‘No’, the service provider may not want to provide the service. Thus, the service provider can evaluate the solvency of the user and the user can wait to see the service finished to pay for it.

_Apply for a public aid_:

In the event that a user wants to apply for public aid, we can use the protocol to, without knowing anything else about the user, to know if he qualifies, by income level to receive a next monthly payment, or if by having extra income this month he can fend for himself. Using this protocol, automatic minimum income systems could be extended and broadly automated.

1 Shafi Goldwasser, Silvio Micali, and Charles Rackoff
[http://users.cms.caltech.edu/~vidick/teaching/101_crypto/GMR85_ZeroKnowledge.pdf](http://users.cms.caltech.edu/~vidick/teaching/101_crypto/GMR85_ZeroKnowledge.pdf)

2 Elena Boldyreva
[https://www.researchgate.net/publication/330032180_Cambridge_Analytica_Ethics_And_Online_Manipulation
_With_Decision-Making_Process](https://www.researchgate.net/publication/330032180_Cambridge_Analytica_Ethics_And_Online_Manipulation_With_Decision-Making_Process)
