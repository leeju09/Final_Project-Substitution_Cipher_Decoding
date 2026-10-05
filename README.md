# Substitution Cipher Decoder

A python project that decodes an English message encrypted with a **substitution cipher** using character frequency analysis, pattern recognition, and iterative mapping - no word list required.

---

## Overview

A **substitution cipher** replaces each letter in a plaintext message with another letter according to a fixed mapping. While the letters change, structural features of the original English remain visible:

- Word length and spacing
- Repeated words and letter patterns
- Letter frequency distribution
- Common one-, two-, and three-letter word patterns

This project exploits those clues to reverse-engineer the encryption key and recover the original plaintext.

---

## Objective
Decode the following encoded message without relying on a dictionary or word list:

encoded_msg = "jyn fg jggtwj djtfcn stf sjyn edcyjnc ia zy stes fjqtye z wzdn owcff gstf gsq sjyn edcyjnc gsjg mtgs tg gszi xjqcfg owzm gstyc cycxtcf gz gtyq otgf ty gsq xcdhq jyn gsc wzdn ntn edty jyn aczawc ntn lcjfg iazy gsc wjxof jyn fwzgsf jyn hjda jyn jyhszktcf jyn zdjyeigjyf jyn odcjvljfg hcdcjwf jyn lditg ojgf jyn gsc wzdn fajvc fjqtye ltdfg fsjwg gszi gjvc zig gsc szwq aty gscy fsjwg gszi hziyg gz gsdcc yz xzdc yz wcff gsdcc fsjwg oc gsc yixocd gszi fsjwg hziyg jyn gsc yixocd zl gsc hziygtye fsjwg oc gsdcc lzid fsjwg gszi yzg hziyg yctgscd hziyg gszi gmz cphcagtye gsjg gszi gscy adzhccn gz gsdcc ltkc tf dtesg zig zyhc gsc yixocd gsdcc octye gsc gstdn yixocd oc dcjhscn gscy wzoocfg gszi gsq szwq sjyn edcyjnc zl jygtzhs gzmjdnf gszi lzc msz octye yjiesgq ty xq ftesg fsjww fyill tg"

The goal is to determine the full mapping between encoded characters and plaintext characters, then produce a readable English message.

---

## Approach

The decoding process is **iterative**:

1. **Count frequency** - Analyse both letter and word frequency in the encoded text.
2.  **Form initial hypotheses** - The most common 3-letter words in English are 'the' and 'and'; map those first.
3.  **Apply the mapping** - Decode the message with the current partial mapping.
4.  **Inspect the partial output** - Look for recognizable words and patterns.
5.  **Refine the mapping** - Add or correct mappings based on context.
6.  **Repeat** - Continue until the entire message is reabable.

Manual updates to the mapping dictionary are made whenever analysis strongly suggests a specific letter correspondence.

---

Final decoded Message:

The decoded text is the famous "Holy hand Grenade of Antioch" speech from Monty Python and the Holy Grail:
and st attila raised his hand grenade up on high saying o lord bless this thy hand grenade that with it thou mayest blow thine enemies to tiny bits in thy mercy and the lord did grin and people did feast upon the lambs and sloths and carp and anchovies and orangutans and breakfast cereals and fruit bats and the lord spake saying first shalt thou take out the holy pin then shalt thou count to three no more no less three shalt be the number thou shalt count and the number of the counting shalt be three four shalt thou not count neither count thou two epcepting that thou then proceed to three five is right out once the number three being the third number be reached then lobbest thou thy holy hand grenade of antioch towards thou foe who being naughty in my sight shall snuff it.

---
# What I learned
1. **Frequency analysis is powerful** - Even a simple letter/word count can unlock a substitution cipher.
2. **Context compound** - Every correctly mapped letter makes the next guess easier.
3. **Iteration beats perfection** - You don't need the full key upfront; build it gradually.
4. **Structural clues matter** - Word length, repeated patterns, and position in a sentence are all signals.

---
 North Hennepin Community College
 Fall Semester 2026
 Course: CSCI 2011-51 Programming in Python
 Author:  Julia Lee GitHub: @leeju09
 
