# Why you should use bcrypt
* Plain text passwords: a plain text password makes use of only letters. Should a hacker gain access to passwords such as these, they can easily pose as a user on your system. Often, plain text passwords are replicated across other logins as well, as users don’t want to have to remember multiple passwords for different sites or applications
* One way hash: With a one-way hash password, a server does not store plain text passwords to authenticate a user. Here, a password has a hashing algorithm applied to it to make it more secure. While in theory, this is a far better password solution, hackers have found ways around this system as the algorithm used is not exactly a one-way option at all
* ‘Salting’ the password: One could consider ‘salting’ a password before it is hashed. What does this mean? Well, a ‘salt’ adds a very long string of bytes to the password. So even though a hacker might gain access to one-way hashed passwords, they should not be able to guess the ‘salt’ string
* Random ‘salt’ for each user: As an alternative, a random ‘salt’ string could be added for each user, created on the generation of the user account. This will increase encryption significantly as hackers will have to try to find a password for a single user at a time
* The BCrypt Solution: BCrypt is based on the Blowfish block cipher cryptomatic algorithm and takes the form of an adaptive hash function
* Using a Key Factor, BCrypt is able to adjust the cost of hashing. With Key Factor changes, the hash output can be influenced. In this way, BCrypt remains extremely resistant to hacks, especially a type of password cracking called rainbow table.
* If you have sensitive data or information that you need to be protected, ensuring it is secured correctly is vital. As we have seen, there are many ways to secure this information through various password methods, but only BCrypt offers a truly robust solution.

# Understanding bcrypt
* industry-grade and battle-tested bcrypt algorithm to securely hash and salt passwords. bcrypt allows building a password security platform that can evolve alongside hardware technology to guard against the threats that the future may bring, such as attackers having the computing power to crack passwords twice as fast. Let's learn about the design and specifications that make bcrypt a cryptographic security standard
* bcrypt was designed by Niels Provos and David Mazières based on the Blowfish cipher: b for Blowfish and crypt for the name of the hashing function used by the UNIX password system.
* crypt is a great example of failure to adapt to technology changes. According to USENIX, in 1976, crypt could hash fewer than 4 passwords per second. Since attackers need to find the pre-image of a hash in order to invert it, this made the UNIX Team feel very comfortable about the strength of crypt
* a fast computer with optimized software and hardware was capable of hashing 200,000 passwords per second using that function
* Blowfish cipher is a fast block cipher except when changing keys, the parameters that establish the functional output of a cryptographic algorithm: each new key requires the pre-processing equivalent to encrypting about 4 kilobytes of text, which is considered very slow compared to other block ciphers. This slow key changing is beneficial to password hashing methods such as bcrypt since the extra computational demand helps protect against dictionary and brute force attacks by slowing down the attack
* Another benefit of bcrypt is that it requires a salt by default. It uses a 128-bit salt and encrypts a 192-bit magic value as noted in the USENIX documentation
* A function called EksBlowfishSetup is setup using the desired cost, the salt, and the password to initialize the state of eksblowfish. Then, bcrypt spends a lot of time running an expensive key schedule which consists of performing a key derivation where we derive a set of subkeys from a primary key. Here, the password is used as the primary key. In case that the user selected a bad or short password, we stretch that password/key into a longer password/key. The aforementioned practice is also known as key stretching
* The magic value is the 192-bit value OrpheanBeholderScryDoubt. This value is encrypted 64 times using eksblowfish in ECB mode with the state from the previous phase. The output of this phase is the cost and the 128-bit salt value concatenated with the result of the encryption loop.
* The result of bcrypt achieves the three core properties of a secure password function as defined by its designers:

* It's preimage resistant.
* The salt space is large enough to mitigate precomputation attacks, such as rainbow tables.
* It has an adaptable cost.
* OWASP recommendations:

* Perform UX research to find what are acceptable user wait times for registration and authentication.
* If the accepted wait time is 1 second, tune the cost of bcrypt for it to run in 1 second on your hardware.
* Analyze with your security team if the computation time is enough to mitigate and slow down attacks.

# Where to store JWT
* When you're building a Next.js application, authentication might be needed in the following cases:
* When accessing a page
* When accessing an API route
* When your application calls an API hosted outside of your Next.js application on behalf of the user
* All of the work happens on the frontend:
* The user is redirected to Auth0.
* When the user is successfully signed in, they will be redirected back to the application.
* The client-side will complete the code exchange with Auth0 and retrieve the user's id_token and access_token which will be stored in memory.
* Using browser local storage can be a viable alternative to mechanisms that require retrieving the access token from an iframe and to cookie-based authentication across domains when these are not possible due to browser restrictions
* cluded from a source outside your domain to the minimum needed (such as links to jQuery, Bootstrap, Google Analytics etc.) Reducing third-party JS code reduces the possibility of an XSS vulnerability. Performing Subresource Integrity (SRI) checking in third-party scripts (where possible) to verify that the resources fetched are delivered without unexpected manipulation is also more secure.