# Passwords


## Key terminology

- ### Hashing: 

Hasing is the process of converting a input of any given length into a fixed size string of text using a mathemetical function.


- ### Rainbow Table:

-What is a rainbow table?

A rainbow table is a precomputed compilation of plaintexts and matching ciphertexts (typically passwords and their matching hashes). Rainbow tables greatly speed up many types of password cracking attacks, often taking minutes to crack where other methods (such as dictionary, hybrid, and brute-force password cracking attempts) may take much longer.

The rainbow table is a database used to gain authentication by cracking the password hash. It is a pre-computed dictionary of plaintext passwords and their corresponding hash values ​​that can be used to find out which plaintext password produces a particular hash. Since more than one piece of text can produce the same hash, it's not important to know what the original password really was as long as it produces the same hash.





 
 - ### Password manager: 
 
 A password manager is a program that helps you manage, remember and improve all your passwords. With a password manager you often only have to remember one password: that of the password manager. The average internet user has dozens of online accounts on all kinds of different websites. For all these accounts you need a username and password. To keep your accounts safe, each account must have a unique and strong password. That is why it is useful to use a password manager. This will help you create and remember all your unique strong passwords.

- ### Salting:

In 'salting', random data is added to a hash function. As if it gets 'salted', hence the term. The result of the encryption of this combination is saved.




# Exercise

## 1-Find out what hashing is and why it is preferred over symmetric encryption for storing passwords.

Hashing is a cryptographic process that can be used to validate the authenticity and integrity of various types of data. Hash functions are mainly used in authentication systems - here they offer the advantage that no passwords have to be stored in plain text format. If hash functions are used incorrectly, serious data leaks can result. It's only worse if hashing is not used at all.

The passwords in a computer system are not stored directly as plain text, but hashed using encryption. A hash function is a 1-way function, which means it cannot be decrypted. Whenever a user enters a password, it is hashed and compared to the hash already stored. If the values ​​match, the user is authenticated.

-Hash function vs. encryption

Unlike encryption, which can be reversed (two-way street), hashing is a one-way street. The output of a hash function is a set of different characters with a fixed length - the hash value.

Hash values ​​do not necessarily have to be kept secret, since they cannot be converted back to their original state. An important point here: Each data set that is subjected to a hash function produces a unique hash value. If two different inputs have the same hash value, there is a "collision". Depending on how complicated it is to track them down using arithmetic operations, a hash function can be classified as ineffective from a security perspective.

If passwords are to be stored in databases, hashing is almost always preferable to encryption: In the event of a compromise, the attackers cannot get their hands on passwords in plain text format. "Encryption should only be used when there is a need to recover the original password," recommends the Open Web Application Security Project (OWASP) on its website.


## 2-Find out how a Rainbow Table can be used to crack hashed passwords.

-How does the Rainbow Table Attack work?

A rainbow table works very quickly and effectively by performing cryptanalysis. Contrasted with brute force attacks, where the hash function calculates each given string, calculates its hash value and then compares it to the one in the computer at each step. A rainbow table attack eliminates this need by already computing hashes of the large set of available strings. 

-Pros and Cons of Rainbow Table Attack

Advantages:

Unlike brute forcing, running the hash function is not the issue here (since everything is precomputed). Since all values ​​are already calculated, this simplifies to a simple lookup and comparison operation in the table.
The exact password string does not need to be known. If the hash matches, it doesn't matter if the string isn't the password itself. It is authenticated.


Disadvantages:

A large amount of memory is required for memory tables.
Since all values ​​are already calculated, this simplifies to a simple lookup and comparison operation in the table.

### 3-Below are two MD5 password hashes. One is a weak password, the other is a string of 16 randomly generated characters. Try to look up both hashes in a Rainbow Table.


### 03F6D7D1D9AAE7160C05F71CE485AD31

![Password1Crack](../00_includes/SEC-07%20Passwords/Password-1-Crack.PNG)

### 03D086C9B98F90D628F2D1BD84CFA6CA

![Password2Crack](../00_includes/SEC-07%20Passwords/Password-2-Crack.PNG)

- This MD5 Password is salted and not recognized in the table

### 4-Create a new user in Linux with the password 12345. Look up the hash in a Rainbow Table.

![Create a new user in Linux](../00_includes/SEC-07%20Passwords/Create-a-new-user-in-Linux.PNG)

GorillaAcron Hash:


![Look up the hash](../00_includes/SEC-07%20Passwords/Look-up-the-hash.PNG)


### 5-Despite the bad password, and the fact that Linux uses common hashing algorithms, you won’t get a match in the Rainbow Table. This is because the password is salted. To understand how salting works, find a peer who has the same password in /etc/shadow, and compare hashes.

My Peer's

![My Peers](../00_includes/SEC-07%20Passwords/My-Peers.PNG)


Compare hashes (with Aurèl)

![Compare hashes](../00_includes/SEC-07%20Passwords/Compare-hashes.PNG)



## Sources

[CrackStation](https://crackstation.net/)

[What is a cryptographic "salt"?](https://crypto.stackexchange.com/questions/1776/what-is-a-cryptographic-salt)

[Hashing](https://www.techopedia.com/definition/14316/hashing-cybersecurity)

[What is Hashing? Hash Functions Explained Simply](https://www.youtube.com/watch?v=2BldESGZKB8)

[Password Hashing, Salts, Peppers | Explained!](https://www.youtube.com/watch?v=--tnZMuoK3E)

[? Password-manager](https://www.zoho.com/vault/educational-content/what-is-a-password-manager.html#:~:text=A%20password%20manager%20is%20an,encrypted%20with%20one%20master%20password.)

[Rainbow-table](https://www.sciencedirect.com/topics/computer-science/rainbow-table)
