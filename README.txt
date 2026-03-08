Chaining Hash Table in C++ for CSE 310 Project (Data Structures and Algorithms)

Features:
- Implements a modified Secure Hash Algorithm 1 to ensure high entropy key distribution.
- Used a linked list chaining strategy to handle multiple keys per hash bucket.
- Built in methods to calculate the standard deviation of the slot lengths to measure distribution efficiency.
- Utilizes 32 bit word processing, circular left shifts, and SHA-1 logical functions.

Interface:
- load(string key): Hashes the input string and inserts it into the appropriate slot in O(1) average time.
- hash_function(string key): Processes the string through 80 iterations of the SHA-1 algorithm to produce a bucket index.
- get_std_dev(): Returns a double representing the standard deviation of the current element distribution.

Getter and Utility Methods:
- get_k_count(): Returns the total number of buckets in the hash table.
- print_list(int index): Displays all keys stored in a specific bucket.
- print_std_dev(): Formats and prints the standard deviation to 4 decimals places.

Internal Components: 
Node Struct: A simple linked list element containing a string key and Node *next pointer.
SHA-1 Helpers: Includes make_block, get_K, get_S, and get_f for low level cryptographic operations.

NOTE: 
- At the time of this README, common methods outside of the assignment's requirements are not implemented.
- SHA 1 reference: https://nvlpubs.nist.gov/nistpubs/Legacy/FIPS/fipspub180-1.pdf
