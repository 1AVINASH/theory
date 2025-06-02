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
