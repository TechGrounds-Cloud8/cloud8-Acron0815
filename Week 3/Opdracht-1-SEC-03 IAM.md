# Identity and Access Management

![Retina Scan](../00_includes/SEC-03%20IAM/Fun.PNG)


## 1.	The difference between authentication and authorization.

![Authen. en Author.](../00_includes/SEC-03%20IAM/Authentication-and-Authorization.PNG)


Authentication and Authorization,

It happens to all of us every day! 
We are constantly being identified, authenticated and authorised by different systems. And yet many people including myself confuse the meanings of these words, often using the terms identification or authorisation when in fact they are talking about authentication.

So what do the terms identification, authentication and authorization mean and how do the processes differ from each other?

Let's ask Wikipedia first:

- "Identification is the determination of the identity of an object or person."

- "Authentication, is the act of proving the identity of a computer system user" (e.g. by comparing the entered password with the password stored in the database).

- "Authorization, grants the access rights/privileges to resources after verification".


### Identification, authentication, and authorisation explained using the team members of my Team. “Cloud Gorillas”

For the sake of simplicity, let's start from the following example: 
Let's assume a user wants to log in to his Google account. Google is a good example because the login process is neatly divided into several basic steps:

1.
First, the system asks for a login. The user enters his login name (here the email address) and system recognises the account. This is the identification process.

2.
Then Google asks the user for a password. By entering the password, which serves as proof here, the user authenticates himself. Google then compares the password entered with the database. If it matches the stored data, the system knows that the user is possibly the owner of the account. This is the so-called authentication.

3. 
In most cases, Google then also asks for a one-time verification code (SMS or authentication app).
 If the user also enters this correctly, the system is finally 100% sure that the person logged in is actually the owner of the account. This is two-factor authentication.
Finally, the system gives the user the right to read messages in their inbox and the like. This is authorisation.

 - Authentication without prior identification makes no sense. After all, it would be pointless to start checking before the system knows whose authenticity to check. One must first introduce oneself to the other person.

In the same way, identification without authentication would be silly. 
Anyone could use any login data that exists in the database. The system might still require a password, but someone could sneak a peek at the password or simply guess it. Therefore, it is safer if the authentication process asks for further proof that only the real user can have, such as a unique verification code.

In contrast, authorisation without identification, let alone authentication, is perfectly possible. 
For example, you may make your document publicly available in Google Drive so that it can be accessed by anyone. In this case, you may see a notice that your document is being viewed by an anonymous Cloud Gorilla. Even if the Cloud Gorilla is anonymous, the system has authorised him, i.e. granted him the right to read the document.

However, if you had only granted the right to read to certain users, the Cloud Gorilla would have had to identify himself (by specifying his login) and authenticate himself (by specifying the password and verification code). The system would subsequently authenticate the user (based on the matching and after checking the details against the database) and authorise the Cloud Gorilla (to read the document).

When it comes to reading the contents of your inbox, Google will never authorise an anonymous Cloud Gorilla. The Cloud Gorilla would then have to impersonate you with your login and password and would no longer be an anonymous Cloud Gorilla because Google would authorise it as you.

So now you know how identification differs from authentication and authorisation. One more important point: authentication is perhaps the most important process in terms of your account security. If you use a weak password for authentication, a Cloud Gorilla could crack your account. Therefore, I recommend:

1- Using strong and unique passwords for all accounts you have.

2- If you have trouble remembering your passwords, a Password manager is there to help you. 
A password manager can also help you generate passwords.

3- Enable two-factor authentication with one-time verification 
    code through SMS. 

Otherwise, an anonymous Cloud Gorilla “except for me 😉”) , who got his paws on your password can browse your mail or do something even more nasty.


## 2.	The three factors of authentication and how MFA improves security.

![MFA](../00_includes/SEC-03%20IAM/Multi-factor-authentication-(MFA).PNG)

What is MFA?

Multi-factor authentication (MFA) is a security mechanism that authenticates individuals through more than one required security and validation process. Because authentication with only a user name and password is insecure and susceptible to hacker attacks.

Why is MFA Important?

The main benefit of MFA is it will enhance your (organization's) security by requiring your users to identify themselves by more than a username and password. While important, usernames and passwords are vulnerable to brute force attacks and can be stolen by third parties. Enforcing the use of an MFA factor like a thumbprint or physical hardware key means increased confidence that your organization will stay safe from cyber criminals.


How Does MFA work?

MFA works by requiring additional verification information (factors). One of the most common MFA factors that users encounter are one-time passwords (OTP). OTPs are those 4-8 digit codes that you often receive via email, SMS or some sort of mobile app. With OTPs a new code is generated periodically or each time an authentication request is submitted. The code is generated based upon a seed value that is assigned to the user when they first register and some other factor which could simply be a counter that is incremented or a time value.

- Three Main Types of MFA Authentication Methods
(Most MFA authentication methodology is based on one of three types of additional information)

1- 	Things you know (knowledge), such as a password or PIN

2-	Things you have (possession), such as a badge or smartphone

3-	Things you are (inherence), such as a biometric like fingerprints or voice recognition


Examples of Multi-Factor Authentication include using a combination of these elements to authenticate:

Knowledge
-Answers to personal security questions
-Password
-OTP’s * (Can be both Knowledge and Possession - You know the OTP and you have to have something in  your Possession to get it like your phone)
Possession
OTPs generated by smartphone apps
OTPs sent via text or email
Access badges, USB devices, Smart Cards or fobs or security keys
Software tokens and certificates
Inherence
Fingerprints, facial recognition, voice, retina or iris scanning or other Biometrics
Behavioral analysis

OTP* - A one-time password (OTP) cq. one true pair/pairing is an automatically generated numeric or alphanumeric string of characters that authenticates a user for a single transaction or login session.           An OTP is more secure than a static password, especially a user-created password, which can be weak and/or reused across multiple accounts.

How does MFA improve Security?
As usernames and passwords have proven vulnerable to attacks, organizations looking to improve their security can turn to MFA to ensure a higher level of trust and allow verified users to access websites, applications and resources.
MFA adds layers of security by requiring users to provide multiple forms of identification. Think of MFA like a bank requiring you to provide ID, account information and a physical key in order to open a safety deposit box.


## 3.	What the principle of least privilege is and how it improves security.

![PoLP](../00_includes/SEC-03%20IAM/The-Principle-of-Least-Privilege-(PoLP).PNG)

What is the Principle of Least Privilege?
The Principle of Least Privilege (PoLP) is an IT security concept in which user access rights are restricted to a minimum. In fact, the user can only access the applications and resources that are essential to his work and for which he IS called upon.
A given user account should only have the access rights required to perform the tasks of its role - no more and no less.

How does the Principle of Least Privilege (PoLP)  improve Security?
The key benefit of the least privilege approach to security is that it minimizes the level of compromise in the event of a security breech. This means : The users who have permissions go on reducing.
Least privilege reduces the number of overprivileged users. Restricting the administrative right to only a few privileged user accounts instead of all end users minimizes the overall occurrence of privileged operations and therefore reduces the likelihood of high-risk errors.
For example, a user account created to retrieve records from a database does not require administrative privileges, while a programmer whose primary function is to update lines of legacy code does not require access to financial records.


## Sources

[What is Identity and Access Management (IAM)?](https://www.onelogin.com/learn/iam)

[Identity and Access Management (IAM)](https://www.ictportal.nl/ict-lexicon/identity-access-management-iam)

[YouTube Video: Identity and Access Management for Beginners](https://www.youtube.com/watch?v=fcSXiUsU5lE)