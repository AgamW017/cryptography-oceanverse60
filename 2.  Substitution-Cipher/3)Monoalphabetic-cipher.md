# Monoalphabetic Cipher
Letter in the plaintext is replaced with a fixed letter from the alphabet. The substitution is one-to-one, meaning that each letter in the plaintext is always substituted with the same letter in the ciphertext.

Example: A substitution rule might map "A" to "Q," "B" to "W," and so on. "HELLO" might become "QEBBI."

# Code
```py
def substitution_encrypt(string,key):
    alphabets = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z'] # indexing the alphabets
    string = list(i for i in string.lower() if i in alphabets) # removes spaces and other characters
    for i in range(0,len(string)):
        string[i]=key[alphabets.index(string[i])] # replacing alphabets using given key
    string = ''.join(string)
    return string

print(substitution_encrypt("sampletext","qwertyuiopasdfghjklzxcvbnm"))
```

# Problems
Man! Who will specify 26 character long key... (that's not the actual problem)

Even though it has 26! possibilies this time (a great jump from 25 indeed) but still its guessable using various methods (we are going to discuss)

# Learning
As time passes humans tend to be smarter than their privious generations, it can be seen through methods of encryptions too, as time goes by, new and smarter methods emerge...

Let's see one more cool way of old age encryption before trying to (very smartly ;) ) guess the message.