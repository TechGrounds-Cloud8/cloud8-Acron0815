# Passwords


## Key terminology

- Hashing: 

Hasing is the process of converting a input of any given length into a fixed size string of text using a mathemetical function.


- Rainbow Table:

 A rainbow table is a precomputed compilation of plaintexts and matching ciphertexts (typically passwords and their matching hashes). Rainbow tables greatly speed up many types of password cracking attacks, often taking minutes to crack where other methods (such as dictionary, hybrid, and brute-force password cracking attempts) may take much longer.

 - Password manager: 
 
 A password manager is a program that helps you manage, remember and improve all your passwords. With a password manager you often only have to remember one password: that of the password manager. The average internet user has dozens of online accounts on all kinds of different websites. For all these accounts you need a username and password. To keep your accounts safe, each account must have a unique and strong password. That is why it is useful to use a password manager. This will help you create and remember all your unique strong passwords.

- Salting:

In 'salting', random data is added to a hash function. As if it gets 'salted', hence the term. The result of the encryption of this combination is saved.




## Exercise
### 1-Find out what hashing is and why it is preferred over symmetric encryption for storing passwords.

### 2-Find out how a Rainbow Table can be used to crack hashed passwords.

### 3-Below are two MD5 password hashes. One is a weak password, the other is a string of 16 randomly generated characters. Try to look up both hashes in a Rainbow Table.


### 03F6D7D1D9AAE7160C05F71CE485AD31

### 03D086C9B98F90D628F2D1BD84CFA6CA

### 4-Create a new user in Linux with the password 12345. Look up the hash in a Rainbow Table.

### 5-Despite the bad password, and the fact that Linux uses common hashing algorithms, you won’t get a match in the Rainbow Table. This is because the password is salted. To understand how salting works, find a peer who has the same password in /etc/shadow, and compare hashes.



## Sources

[What is a cryptographic "salt"?](https://crypto.stackexchange.com/questions/1776/what-is-a-cryptographic-salt)

[Hashing](https://www.techopedia.com/definition/14316/hashing-cybersecurity)

[What is Hashing? Hash Functions Explained Simply](https://www.youtube.com/watch?v=2BldESGZKB8)

[? Password-manager](https://www.zoho.com/vault/educational-content/what-is-a-password-manager.html#:~:text=A%20password%20manager%20is%20an,encrypted%20with%20one%20master%20password.)

[Rainbow-table](https://www.sciencedirect.com/topics/computer-science/rainbow-table)
