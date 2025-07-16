### Checksum
* A value calculated from a data that is used to verify integrity pf tje data
* Typically used to detect errors in data that may have been introduced during transmission or storage
* The basic idea behind a checksum is to apply a mathematical algorithm to the data and generate a small fixed-size number (the checksum). When the data is later retrieved or transmitted, the same algorithm is applied again to check if the data matches the original checksum. If the checksums match, it means the data is likely intact. If they don't, it indicates that the data may have been corrupted or altered.
* Algorithms
    * MD5: Produces a 128 bit (16 byte) hash
    * SHA-1: Secure hashing algorithm. Produce a 160 bit (20 byte) hash
    * SHA-256: Produces a 256 bit (32 byte) hash
* Uses:
    * While downloading a file, we might be given a checksum at the beginning so we can verify if the file was downloaded properly
    * Network protocols (TCP, IDP) use checksum to verify if the data transferred across network is not corrupted
    

### Salting
* It involves adding a random string (the "salt") to the data before it's hashed
* This randomness ensures that even if two users have the same password, their hashes will be different. This is crucial for password security because it makes it much harder for attackers to use pre-computed tables (like rainbow tables) to crack passwords. 

### Hexadecimal
* Base 16 numerical system
* Since we have only 10 numeric digits, we use 6 letters as well to represent 16 symbols in hexadecimal systems
    * 0-9, A = 10, B = 11, C = 12, D = 13, E = 14, F = 15
* To represent 1111 of binary in hexadecimal, we will just need 1 symbol (F). Hence, to represent a number of 4 symbols, we just need 1 symbol. Hence, 32 bits can be represented in just 8 symbols in hexadecimal


### HMAC (Hash based Message Authentication Code)
* Hashing: A hash function takes an input and produces a fixed-size output (a hash or digest). Hash are usually one way
* MAC (Message Authentication Code): A mac is used to verify both the integrity (that the message hasn't been tampered with) and the authenticity (that the message came from a legitimate sender) of a message
* Keyed Hash: HMAC enhances a regular hash function by incorporating a secret key. Instead of just hashing the data, HMAC mixes the secret key with the data before hashing. This means that only someone who possesses the exact same secret key can re-create the correct hash for a given message
