---
title: "Post_tutorial"
date: 2022-03-28T03:27:21-04:00
draft: false
---

## cs580-S2022-lab01

### Name
Michael Ceccarelli

### GitHub Account Name
mceccarelli

### Submission Date
9 March 2022

## Table of Contents

- [Introduction to Hashing](#introduction-to-hashing)
- [About](#about)
- [Features](#features)
- [Obtaining the Resource](#obtaining-the-resource)
- [Setup](#setup)
- [Execution](#execution)
- [Helpful Resources](#helpful-resources)

### Introduction to Hashing

	- Hashing algorithms are some of the most beautiful applications of mathematics in computer science.  The idea is simple: hashing is used for verification without explicit identification.  Every hash created by a hashing algorithm is always of the same length, and the same input will always produce the same output.  However, the key idea is that the inverse function doesn't exist, and trying to reverse the process and find the "actual" ID, password, or message is impossible from the hashing algorithm's output.  That's an unbelievable mathematical achievement, and I think it's truly incredible that these things exist.  I'm really excited to learn more and more about them as I go through this semester and into my senior comp, which is more and more likely to be about hashing algorithms every day.

### About

Describe the software resource and explain its relevance to your topic. Please include the link to the software resource.

	- The software resource I took a look at is a hash identifier.  Basically, what this means is that when you input a hash, the program tries to guess which hashing algorithm you used to to make it.  It won't guess what the actual message you inputted was originally, as that is supposed to be impossible, and it far too complicated to do with even the hashing algorithms that have been cryptographically broken.

	- I was really excited to discover this tool as a way to see exactly how an identification might be made.  Looking through the code is interesting, and it sparked a lot of other discoveries I made throughout GitHub about the same topic.  I have a list of other software tools I am going to take a look at here over the next couple days, that increase the complexity from the one I researched for this lab.  Some of them perform the same functionality, hash identification, while others actually go as far as to try to crack the original message by reversing the hash (something that should be impossible, making the hashing algorithm used unsafe).

	- https://github.com/AnimeshShaw/Hash-Algorithm-Identifier

---

### Features

Outline the main features of the software. Why is this software necessary for your work?

	- The software is necessary for my work because it was a great starting point for me to learn about hashing algorithms, and specifically how an identification algorithm operates.  There are a lot of these on the internet, but what I particularly love about this specific repository is that I can see all the code, and all the algorithms that the programmer used to make the best guess at what the hashing algorithm is that created the hash.

	- It is quite simple, as it's only functionality is to make a guess at what the hashing algorithm was, but it's still very important, as in order to "break" a hash (find the reverse algorithm and identify the original message), you need to identify the hash first.  That specific topic, being how they are broken, is really interesting to me, but before I get there, I need to start smaller.  Thus, I picked this tool to learn about because it can help me understand hashes in general, obviously the most fundamental step in my journey through learning about hashing algorithms.

	I include a code snippet of some of the methods that I've been studying to learn about how the hashes are detected.

	```
	def identify_hashes(input_hash):
    """
    Function to identify all the hashes and return the results as list.
    :rtype : list
    :param input_hash:
    """
    res = []
    for items in HASHES:
        if match(items[1], input_hash):
            res += [items[0]] if isinstance(items[0], str) else items[0]
    return res


def get_input(prompt):
    """
    Function Get input from the user maintaining the python compatibility with earlier and newer versions.
    :param prompt:
    :rtype : str
    :return: Returns the Hash string received from user.
    """
    if hexversion > 0x03000000:
        return input(prompt)
    else:
        return raw_input(prompt)
	```

---

### Obtaining the resource

Where do you find this software resource? Is it an open source project? an online tool? How do you install it? Are there any libraries that are also necessary to install?

	- I found this software resource on GitHub, after several searches related to cryptography, hashing algorithms, hash crackers, and hash identifiers.  I picked this one because of its simplicity (obviously the ideas aren't simple, but it's as simple as it's going to get for now) and it can serve as a good starting point for my learning.  All the code is located right on GitHub, so installation and setup was super easy.  I cloned the repository, and have been running it several times on my laptop to try to understand it more (and to test it out of course).  I didn't have to install any extra libraries to run it, though of course I did need to have Python, as that is the language it is written in.  The program runs right in the terminal window, and outputs it's guesses there after you paste in a hash.

	- The program works well, which is why I started studying it's source code, and has been starred by hundreds of users on GitHub.  To get some hashes to try it out with, I simply went on the internet -- there's tons of good resources there related to hash making and hash breaking, and I put some input text in, got a hash back, and pasted my hash in as input.  It was good at guessing which one I was using, and it usually comes up with a couple "top" guesses, then a bunch of other potential hashing algorithms underneath it.

---

### Setup

Include steps of all necessary steps to get the software to run (for example, installations). Include the commands to run if necessary.

	- This is mentioned in passing above, and it is very simple.  I cloned the repository using my SSH key, and I downloaded it into my 580 folder so I could experiment with it there.  The code is written in Python, so if I didn't have that, then I would have had to install it, but of course, I do, so that wasn't an issue.  There were no other installations that I did.  I entered the folder, and ran the program using `python HashIdentifier.py` without issues.  From there I was able to paste in my different hashes, which I obtained from using different hashing algorithms (as the software claims it can identify lots of different hashing algorithms), and got correct output each time.  It was really awesome to see, and I had so much fun using it.  I'm really excited to explore more, as there's tons of tools on GitHub where I can look at the code they are using and study off of it.  This assignment has given me a whole new perspective on hashing algorithms, and even though I only started a week ago, I really feel like my understanding is developing.

---

### Execution

How do you get the resource ready to use? Are there inputs to know? Please show a step-by-step guide (in a tutorial format) for readying the resource for your work. Include screenshots of successful execution and use of the software.

	- I'll give an example of what a user would do to test out the software using a SHA256 hash.  We will use an online resource to type in a message and generate out hash using the SHA256 algorithm.  There are tons and tons of these types of tools on the internet (yet another thing that I am super excited to look more into), and this is from one of those.

![SHA256 Screenshot](https://github.com/Allegheny-ComputerScience-580-S2022/lab01-mceccarelli/blob/main/writing/Screen%20Shot%202022-03-09%20at%2012.53.52%20PM.png)

	- Then, we run the hash identifier (using the same steps as above), and paste the output from the website into the hash identifier's input.  Its guesses are listed below, and as we can see, it guessed SHA256 as one of the most probable hashing algorithms that I used to generate that hash.

![HashIdentifier](https://github.com/Allegheny-ComputerScience-580-S2022/lab01-mceccarelli/blob/main/writing/Screen%20Shot%202022-03-09%20at%2012.51.57%20PM.png)
![HashIdentifierWithInput](https://github.com/Allegheny-ComputerScience-580-S2022/lab01-mceccarelli/blob/main/writing/Screen%20Shot%202022-03-09%20at%2012.52.19%20PM.png)

---

### Helpful resources

Include some of the relevant resources (links, articles, etc.) that you used to write in your tutorial.

	- I had the opportunity to look at many different tools on GitHub, all of which I will definitely be exploring at a later date.  They weren't appropriate for me to start with, as I chose this tool because it was not only fun but far less complicated (if there is such a thing) than the other ones I looked at.  I will link all of them below.

	- https://github.com/AnimeshShaw/Hash-Algorithm-Identifier
	- https://github.com/openwall/john
	- https://github.com/keroro824/HashingDeepLearning

	- I'll be trying all these out eventually, and they'll also be great learning resources, but they are definitely not places to get started, so they'll have to wait.

	- I also used several online hash algorithm tools, which made the hashes I used to test the program with.

	- https://passwordsgenerator.net/sha256-hash-generator/
	- https://www.md5hashgenerator.com
	- https://www.browserling.com/tools/sha2-hash

---

(Did you remember to add your name and GitHub account name and date to the top of this document?)
