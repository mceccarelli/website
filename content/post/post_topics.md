---
title: "Post_topics"
date: 2022-03-28T03:30:58-04:00
draft: false
---

## Assignment 2
### Topic Exploration For a Senior Thesis Proposal

#### Name
Michael Ceccarelli

#### GitHub Account Name
mceccarelli

#### Submission Date
3 March 2022


#### Questions

##### 1.

What research area of interest are you exploring this week?

I explored the field of security through the lens of algorithms, specifically hashing algorithms.

Hashing algorithms have been on my radar for years now, I just haven't gotten around to actually diving into them.  They are truly beautiful, and from my limited previous knowledge, utilize a lot of the same number theoretic properties that cryptosystems I do understand, such as RSA, rely on.

I truly can't wait to explore, I know I'm going to really enjoy it!


---
##### 2.

What keywords did you use to find relevant articles at online search engines?

I found it a bit difficult to start, as all the papers that came up throughout my first few searches were all very advanced, and I needed something that helped me get my feet wet in hashing algorithms before I started looking at an analysis paper comparing them, for example.

Some keywords I used were hashing, hash, algorithms, cryptography, encryption, and SHA.


---
##### 3.

In more detail, please describe one of the most exciting articles which is highly _relevant_ to your own research area.

 - Please describe this article in a few sentences to give an overall understanding of this work. For this article state:

The article begins by introducing exactly what hashing algorithms are and how they can be used (exactly what I needed).  Then, it moved into more advanced topics, comparing the Secure Hash Algorithms, Message Digest, and Whirlpool algorithms.  It was a really good read for me, since it slowly brought things on, rather than assuming I had a lot of previous knowledge about the subject.  Also, it kept things interesting, eventually diving into more complex topics, certainly more so than where it started.


 - What is the goal and motivation of the work?

The goal of the article is to describe the most popular hashing algorithms, describing how they work, without ever going too technical or mathematical.  It was an extremely informative article to read, and it certainly inspired me to investigate hashing algorithms more.


 - Discuss the research question(s) behind the work (what did they study, what problem did they seek to solve)?

The researchers took a look at multiple hashing algorithms, discussing a bit of their history and how they are related to one another.  The author's aren't trying to find flaws in the security of the hashes, they are describing how they work and some of the history behind each one (and each iteration/generation/version of the same algorithm).


 - What did the authors accomplished in this work?

The authors managed to give the reader a very clear beginning to hashing algorithms, inspiring the audience to investigate more and further their learning.  They cover a variety of hashes, explaining a bit about how each one works, without ever getting too technical as to turn off the reader into further pursuing the topic.  It was an excellent read for me, someone who is very interested in hashes but hasn't had any place to start in the past, serving as a motivator and a foundation for further study.


 - What future directions of their work are possible?

There is a clear direction for more work, specifically taking off the training wheels and diving deeper into the theory that drives hashing algorithms.  There is certainly a good basis for the logic and ideology that goes into the hashes, but I know there's a lot more room for the authors to get more technical with each one.


- Please include the article’s references. Note, these references can be found by clicking on the “cite” link in Google Scholar.

Here are the article's references.

[1] R.C. Merkle, "One Way Hash Functions and DES", in CRYPTO, 1989, pp.428-446.
[2] Kleppmann, Martin (2 April 2017). Designing Data-Intensive Applications: The Big Ideas Behind Reliable,
Scalable, and Maintainable Systems (1 ed.). O'Reilly Media. p. 203. ISBN 978-1449373320.
[3] Goodin, Dan (2016-05-04). "Microsoft to retire support for SHA1 certificates in the next 4 months". Ars
Technica. Retrieved 2019-05-29.
[4] "Google will drop SHA-1 encryption from Chrome by January 1, 2017". VentureBeat. 2015-12-18. Retrieved 2019-05-29.
[5] "The end of SHA-1 on the Public Web". Mozilla Security Blog. Retrieved 2019-05-29.
[6] "Announcing Request for Candidate Algorithm Nominations for a New Cryptographic Hash Algorithm (SHA-3) Family [U.S. Federal Register Vol. 72 No. 212)]" (PDF). November 2, 2007. Archived (PDF)
from the original on March 31, 2011. Retrieved July 18, 2017.
[7] https://en.wikipedia.org/wiki/File:SHA-1.svg
[8] https://en.wikipedia.org/wiki/File:SHA-2.svg
[9] https://en.bitcoin wiki.or g/wiki/SHA -3


---
##### 4.

What type of relevant software resources (libraries, data, algorithms, open-source tools, online tools, etc.) did you find? Why are these resources relevant to your work?

There were so many different directions to take, and the article helped push me in the right area.  It mentions NIST, a government agency which standardizes cryptography.  They are responsible for recommending the safest and most secure algorithms, citing the fact that cryptography is far too complex for most businesses to worry about.

In reality, there are tons and tons of software tools relevant to security, even specifically hashes, that I can investigate in the future.  Lots of hash crackers, hash identifiers, explanations of hash algorithms themselves, etc, there's truly so much to explore.  Also, what's nice is there seems to be lots of open source work, so it's all accessible and easy to learn from.


---
##### 5.

In more detail describe one of the software resources that you found. For this software resource state:

Inspired by a tool we used in 403 called "John the Ripper", I did some digging on GitHub to get started.  I investigated a hash identifier someone made in Python, and it was really fun!


 - The goal and motivation of the software?

The goal is to be able to identify hash algorithms by entering a hash and getting the most probable algorithms used to create said hash.


 - What is the application and relevance of the software to your topic?

The application seems to be more for a fun challenge, but obviously identifying hashes (specifically an algorithm that was used) can be a big part of cyber security, both on offense and defense.


 - What does the software do (or what is it supposed to do)?

The software takes an input, which is some hash, and tries to guess which hashing algorithm was used to create it.  It gives what it believes to be the most probable algorithms, as it is not guaranteed to be exactly correct.


- What is needed to use the software? Please try to download software or code to execute it to be able to fully answer this question.

I cloned it the way I always do, then ran it using `python (tool name).py`.  There are tons of hash-algorithm-learning resources on the internet (that I used in 403 from before), so finding hashes to test wasn't hard.


- Who are the users of the software?

Anybody who is trying to find out what algorithm created a hash, or someone just having fun investigating hash algorithms (like myself).


---

(Did you remember to add your name and GitHub account name and date to the top of this document?)
