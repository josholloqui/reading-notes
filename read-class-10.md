# User Modeling
* Modern web applications need to model sensitive information about their users. When a users provides an applications with sensitive information, they are trusting that it will not be leaked are misused
* users password, should be encrypted using a hashing algorithm before it is ever stored. this prevents anyone (including developers with database permissions) from ever getting access to their password
* User models that have sensitive data that should NEVER be sent to client applications. If your application requires that users be able to read each others personal information, create a second Profile model to hold that data and strictly limit access to the Profile model. Safely using a second model will ensure that no users will accidentally (or maliciously) get access to sensitive information

# Cryptography
* Cryptography is the science which studies methods for encoding messages so that they can be read only by a person who knows the secret information required for decoding, called the key; it includes cryptanalysis, the science of decoding encrypted messages without possessing the proper key, and has several other branches

# Hash Algorithms
* A Cryptographic Hash Algorithm takes a piece of data and produces a hash that is deliberately difficult to reverse. If identical data is passed into the algorithm the same hash will always be produced. Hash algorithms are often used for checking the integrity of data.
* a hash password can be stored when the user signs up. When the user needs to login, they can resend their password and the server can hash the login password using the same hash algorithm
* server compares hash passwords

# Cypher Algorithms
* A Cryptographic Cypher Algorithm takes a piece of data and a key and produces encrypted data. Later the encrypted data can be reversed into the original data by decrypting it using the same key.
* User tokens can be created by associated a random unique string (tokenSeed) with a user account and, in turn, encrypting the tokenSeed with a secret key that only the server knows. We can then send the encrypted token to a client application. When the client makes a future request they send back the token. The server can reverse the token into the tokenSeed by decrypting it with the secret key

# Basic Authorization
* Basic Authorization is a common method used to send a username and password in an HTTP request. The username and password are joined with a ‘:’ then “base64 encoded” and placed after the string ‘Basic ‘. The resulting string is set to the value of an Authorization header.
* A Server can decode the Basic Authorization header to retrieve the username and password. 
