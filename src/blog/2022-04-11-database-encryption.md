---
title: Alwala Community Development Network
description: Storing a sensitive data in plain text format could turn into a
  nightmare if the access to your database has been compromised. To minimize
  losses in such an cases MySQL provides functions for encrypt and hash of data.
author: Abigail
date: 2023-02-08T13:52:47.492Z
tags:
  - post
  - featured
image: /assets/blog/article-1.jpg
imageAlt: Image reused
---
STORING A SENSITIVE DATA
Storing a sensitive data in plain text format could turn into a nightmare if the access to your database has been compromised. To minimize losses in such an cases MySQL provides functions for encrypt and hash of data.
Insert Values:
mysql> INSERT INTO `users` (`email`, `pswd`) VALUES ('user3@example.com', PASSWORD('pass123'));

AES - these functions use the official AES algorithm (also known as "Rijndael") that provides encoding with a 128-bit key. 
To encrypt a password use the AES_ENCRYPT(str,key_str) function:
mysql> INSERT INTO `users` (`email`, `pswd`) VALUES ('user6@example.com', AES_ENCRYPT('pass123', 'secret'));

INSERT into user (first_name, address) VALUES (AES_ENCRYPT('Obama', 'usa2010'),AES_ENCRYPT('Obama', 'usa2010'));

To decrypt a password previously encypted with the AES algorithm use the AES_DECRYPT(crypt_str,key_str) function:

SELECT AES_DECRYPT(first_name, 'usa2010'), AES_DECRYPT(address, 'usa2010') from user;

mysql> SELECT AES_DECRYPT(`pswd`, 'secret') AS `pswd` FROM `users` WHERE `email` = 'user6@example.com';

mysql> INSERT INTO custcards VALUES (AES_ENCRYPT('cardnumber',SHA2

('cvv',512)));

Insert new User

INSERT INTO `user` (`Username`, `Pass`) VALUES ('bob.jhonny', MD5('mypassword'));
SELECT * FROM `user` WHERE username='bob.jhonny' AND pass=MD5('mypassword');

Conclusion
The AES standard provides the best defense in on sensitive data . The AES_ENCRYPT and AES_DECRYPT functions are the best choices to store a sensitive data (e.g. passwords, credit card numbers, etc.).