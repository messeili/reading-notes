# Reading30: Hash Tables

#### Hashing

Basically, a hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.

Creating a Hash A hash table traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a possible suggestion:

Add or multiply all the ASCII values together. Multiply it by a prime number such as 599. Use modulo to get the remainder of the result, when divided by the total size of the array. Insert into the array at that index. Example:

```
Key = "Cat" Value = "Josie"

67 + 97 + 116 = 280

280 \* 599 = 69648

69648 % 1024 = 16

Key gets placed in index of 16.
```
