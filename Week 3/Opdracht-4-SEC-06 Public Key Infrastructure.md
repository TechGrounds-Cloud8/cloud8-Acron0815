# Public Key Infrastructure


A Public Key Infrastructure (PKI) is a system that makes it possible to generate, distribute and check digital certificates. These certificates serve as a digital identity for people and machines and are used to secure computer-aided communication.

The underlying idea is as follows: With the help of an asymmetric cryptosystem, messages on the Internet can be signed and encrypted. Signing guarantees that the message in this form really came from the specified sender. However, you need the public key of the sender for this. This could z. B. be sent by e-mail. At this point, however, the question arises of how to ensure that it is actually the sender's key and not a forgery by a fraudster. For this purpose, the key to be sent can itself be signed with a trustworthy key. In this way, a hierarchy of trustworthy institutions can be established. However, one must be able to rely on the authenticity of the keys of the highest institutions in this hierarchy.


### Essential components of a PKI are:

- Digital Certificates: Digitally signed electronic data that can be used to prove the authenticity of objects.

- Certification Authority (CA): Organization that provides the CA certificate and signs certificate applications.

- Registration Authority (RA): Organization where people can apply for certificates. This checks the correctness of the data in the desired certificate and approves the certificate application, which is then signed by the certification authority.

- Certificate revocation list: A list of certificates that were withdrawn before their validity expired, e.g. because the key material was compromised. In principle, a PKI must always offer a certificate status check. However, in addition to the CRL (offline status check), so-called Online status checks such as OCSP are used.

- Directory service: a searchable directory containing issued certificates, usually an LDAP server, more rarely an X.500 server.

- Documents: A PKI maintains one or more documents that describe the working principles of the PKI. The key points are the registration process, handling of the secret key material, centralized or decentralized key generation, technical protection of the PKI systems and any legal assurances. In X.509 certificates, the CPS can be linked in the extensions of a certificate. The following documents are sometimes common.:

-CP (Certificate Policy): In this document, the PKI describes its requirement profile for  its own way of working. It is used by third parties to analyze trustworthiness.

-CPS (Certificate Practice Statement): The specific implementation of the requirements in the PKI is described here. This document describes the implementation of the CP.

-PDS (Policy Disclosure Statement): This document is an excerpt from the CPS if the CPS is not to be published.


## Key Terminology

- ### SSL (Self-signed) Certificate

A self-signed SSL certificate is a certificate that is signed by the person who created it rather than a trusted certificate authority. Self-signed certificates can have the same level of encryption as the trusted CA-signed SSL certificate.

- ### Public Key Infrastructure (PKI)

Public key infrastructure (PKI) governs the issuance of digital certificates to protect sensitive data, provide unique digital identities for users, devices and applications and secure end-to-end communications. Public Key Infrastructure (PKI) is a set of roles, policies, hardware, software and procedures needed to create, manage, distribute, use, store and revoke digital certificates and manage public-key encryption. In short, PKI assigns identities to keys so that recipients can accurately verify the owners.


- ### X.509 Standard

X.509 is a standard defining the format of public-key certificates. X.509 certificates are used in many Internet protocols, including TLS/SSL, which is the basis for HTTPS, the secure protocol for browsing the web. They are also used in offline applications, like electronic signatures. An X.509 (also called digital) certificate contains a public key and an identity (a hostname, or an organization, or an individual), and is either signed by a certificate authority or self-signed.
X.509 is also the standard which defines the process in which a PKI should function.


## Application areas of PKI


- ### Secure email

A sent e-mail passes several server nodes on its journey. This can be e-mail servers, routers, firewalls or similar. The content of the e-mail can be read and also changed at each of these nodes as well as en route by eavesdropping on the network traffic.
To prevent this, use "secure e-mail". This means that the e-mail is encrypted to prevent it from being read. To ensure that the content of the message has not been modified and to ensure the identity of the sender, the message is signed.

- ### SSL
You know it from online shopping and online banking. You transfer personal and highly sensitive data (address, credit card number, PIN, TAN, ...) several times over the Internet - a medium in which everyone can read all the information (a certain level of specialist knowledge is of course required).
SSL was developed to keep sensitive data confidential and only make it accessible to those for whom it is intended. Essentially, it is a question of the components involved identifying each other before the connection is established, i.e. identifying them, and then only communicating in encrypted form. One can operate SSL in one-way or two-way authentication. Which mode is chosen depends on the configuration of the server. With one-way authentication, only one of the two components (client or server) presents a certificate. In almost all cases, this is the server. With mutual authentication, the server first identifies itself to the client and then the client identifies itself to the server. So far, this mode has been found quite rarely, but it is ideally suited to replacing the login using a user name and password with a certificate-based login on various websites.

- ### 2 factor authentication
The 2 factor authentication is a combination of the two authentication methods possession and knowledge. Smart cards from the Bavarian administration PKI can be used instead of an RSA token for 2-factor authentication, e.g. on the SSL proxy. Possession is the smart card, knowledge is represented by the PIN.

- ### IPsec
IPSec provides a security architecture for communication over IP networks. This is to ensure the protection goals of confidentiality, authenticity and integrity. The connection between PKI and IPSec represents the certificate-based authentication (similar to SSL) of the components involved.

- ### Windows Logon
The certificate-based Windows LogOn enables the user to log on to the PC with a certificate stored on a smart card instead of with a user name and password. One of the prerequisites is a PC and account integrated into the Active Directory.

- ### Server Authentication
With server authentication, the server presents the client with its certificate before the connection is successfully established, thus ensuring its authenticity.

- ### Client Authentication
With client authentication, the client presents its certificate to the server before the connection is successfully established, thus ensuring its authenticity. A distinction is made between the client authentication of a machine and that of a person.

- ### Document Signature
If someone sends you a document, you cannot be sure whether the document is genuine and whether it was written by the person who claims it. By signing documents, i.e. electronically signing them, as is possible in MS Word or Adobe Acrobat, for example, you can ensure authenticity and integrity.

- ### Code Signing
A code signing certificate allows you to sign your software. This is particularly useful for ActiveX components that are to be distributed over the web. With signed software components, the user can be sure who created the software and whether the software was modified.
