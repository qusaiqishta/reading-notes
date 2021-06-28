# Caesar cipher

is one of the simplest and most widely known encryption techniques. It is a type of substitution cipher in which each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet. For example, with a left shift of 3, D would be replaced by A, E would become B, and so on. The method is named after Julius 
Caesar, who used it in his private correspondence.

## Cracking the cipher
Imagine that a very literate and savvy enemy intercepts one of Caesar's messages.

That enemy does not know that Caesar always uses a shift of 3, so he must attempt to "crack" the cipher without knowing the shift.
There are three main techniques he could use: frequency analysis, known plaintext, and brute force.

1- Frequency analysis

Human languages tend to use some letters more than others. For example, "E" is the most popular letter in the English language. We can analyze the frequency of the characters in the message and identify the most likely "E" and narrow down the possible shift amounts based on that.


2- Known plaintext

Another term for the original unencrypted message is plaintext. If the enemy already knew some part of the plaintext, it will be easier for them to crack the rest of the encrypted version.
For example, messages tend to start with similar beginnings. In WWII, encrypted German messages always started with a weather forecast, which ultimately made them easier for British mathematician Alan Turing to crack.


3- Brute force

There are only 25 possible shifts (not 26 — why not?). The enemy could take some time to try out each of them and find one that yielded a sensible message. They wouldn't even need to try the shifts on the entire message, just the first word or two.



## Encryption, decryption, and cracking
- Encryption: scrambling the data according to a secret key (in this case, the alphabet shift).

- Decryption: recovering the original data from scrambled data by using the secret key.

- Code cracking: uncovering the original data without knowing the secret, by using a variety of clever techniques.