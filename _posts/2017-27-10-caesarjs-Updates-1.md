---
layout: post
title: caesar.js project update #1 : First Steps
---

# caesar.js project update #1 : First Steps
27th October 2017

## Introduction

This is the first update on the my project - caesar.js. This blog post will provide a brief summary of current progress, the decision regarding the naming of the libary and information on the first cipher - the caesar cipher including its name, a brief history, how it works and how I want to implement it in caesar.js.

## Update Summary

Since I uploaded the initial project plan, I have taken a few solid steps towards acheiving the project goal. 

The project plan references the fact that this project will have to main elements to build. 

- The Front End View to work with the ciphers
- The JavaScript library to do the logic -  encrypting/decrypting etc.

In short, I have now created the simplest of UI's to essentially test the library as it is in use. I have also begun the library, implementing the first cipher. 

## Choosing A Name

I am using the working name 'caesar.js' this is due to the first cipher that was implemented in the library - the caesar Cipher. The caesar cipher is named after Julius Caesar who is the first recorded person to use this most simple form of encryption. **Simple is a theme I would like to maintain through out the project.**

## The Caesar Cipher

### Cipher Summary:

The Caesar Cipher is one of the most popular ciphers known through out the world and examples of it in use can be found through out the history books. The Cipher is named after Julius Caesar, the infamous Roman Politician who helped form the Roman Empire.

The cipher earn't it's name as Julius was the first recorded user, although it is highly likely that it was used by other users way before Caesar.

## Cipher Method:

The purpose of any cipher is to hide the meaning of the original text (referred to as the plain text) by converting this into an unreadable text (referred to as cipher text) using a certain key. This key contains all the information required to convert the plain text to cipher text but perhaps more importantly the owner of the key can then convert the cipher back to plain text again when the text needs to be read.

The Caesar cipher essentially shifts all the letters along a certain number of places. So if the key was 3, all letters in the alphabet would be shifted 3 letters along. 

Here is the plain text alphabet:

Plain Text |  Plain Text Numeric Value | Plain Text Alphabet (cont.) | Plain Text Numeric Value (cont.)|
------------ | -------------|-------------|-------------|
a | 1 |n|14
b | 2|o|15
c| 3|p|16
d| 4|q|17
e| 5|r|18
f| 6|s|19
g| 7|t|20
h| 8|u|21
i| 9|v|22
j| 10|w|23
k| 11|x|24
l| 12|y|25
m| 13|z|26

If the key value is 3 when you encrypting the plain text all letters will become the corresponding letter 3 places down. i.e. *a* becomes *d*, *d* becomes *g*, *g* becomes *j*  etc.

Here is the plain text alphabet along side the cipher alphabet with a shift of 3:

Plain Alphabet |  Cipher Alphabet val | Plain Text Alphabet (cont.) | Cipher Text Alphabet Value (cont.)|
------------ | -------------|-------------|-------------|
a | d |n|q
b | e|o|r
c| f|p|s
d| g|q|t
e| h|r|u
f| i|s|v
g| j|t|w
h| k|u|x
i| l|v|y
j| m|w|z
k| n|x|a
l| o|y|b
m| p | z |c

It should be clear from above the above table that the alphabet in this case should be treated similar to modular arithmetic or clock and once you have reached the end of the alphabet, you continue back to start. For example, *Z* shifted 1 place would become *A*

### Example:

Take a look at the example below where the word hello is encrypted with a shift of 3.

Caesar Cipher (Shift 3)|
-----------------------|
Plain Text Letters:|h|e|l|l|o
Cipher Text Letters:|k|h|o|o|r

## Implementing in Caesar.js Libary

In order to successfully implement a basic version of this classic cipher in the caesar.js library the following use cases must be passed:
- The user should be able to call a function and pass two values - the plaintext to be encrypted and the shift value. This should return the encrypted string of text. The function should by default maintain case, symbols and spaces.
- The user should be able to call a different function and pass two values - the cipher text to be encrypted and the key. This should return the plain text.



