Title: "Intuitive" Protocols
Date: 2015-04-12
Category: Computing
Tags: computing, networks, intuitive, humour

Upon dwelling upon the core of the internet, and the fact that its nothing more than a very large, very distributed system, I always begin to feel a gentle, yet unshakable, sense of sadness creep over me; kind of like when you first realise that the world is not a fair place and that kitten on the box may never reach its treat, or that Keanu Reeves will almost certainly make more money than you over arbitrary time scales. 

The internet is such a core utility in our lives, but an eternally confusing one. Whenever people try to “explain” the core protocols and connections that make up distributed, weblike, systems, they always lean towards “intuitive”, “approachable” arguments. Interestingly, no matter how they spin it, these kinds of intuitive arguments are not intuitive. A successful intuitive explanation must invoke experiences that I have had in real life, and I have never had a real-life experience that has resembled any form of common distributed or internet protocol. For example, let’s suppose that I am having a nice conversation with a friend. If that conversation was similar to HTTP, it would go something like:


EMILY: Alex, I would like [today’s XKCD](http://xkcd.com/).

ALEX: OK here it is. 

EMILY: Alex, I would like [last week’s comic](http://xkcd.com/737/).

ALEX: Yeah, its here. 

EMILY: Alex, I want the comic with Knuth being a ninja.

ALEX: … Give me a moment to find it.

EMILY: Let me tell you again that I want the XKCD comic with Knuth being a ninja.

ALEX: …

[Hours pass]

EMILY: Alex, do you have the XKCD comic with [the ghost and the eternal passage of time](http://www.xkcd.com/1393/)?

ALEX: 404 FILE NOT FOUND. GO AWAY.


And that, children, is how you lose friends forever. 

But maybe something less concrete, more conceptual, is necessary for the real intuitive explanation experience. Gossip protocols are ostensibly modeled off, you guessed it, gossip, so sound as if they can be easily explained. So let’s pretend that I’m at a party and am meeting someone for the first time:


EMILY: I announce that my name is Emily.

OZ: *to Beth* I verify that she announced that her name is Emily.

ANDY: *to Beth* I verify that she announced that her name is Emil.

BETH: *to Oz* I verify that she announced that her name is Emil.

OZ: *to Beth* I verify that she announced that her name is Emily!

BETH: I VERIFY THAT SHE ANNOUNCES THAT HER NAME IS EMIL!

ANDY: I VERIFY THAT SHE ANNOUNCES THAT HER NAME IS EMIL!

OZ: I ANNOUNCE THAT YOUR NAME IS EMIL.

EMILY: I announce that my name is Emily!

OZ: *to Andy* She announces that her name is Emily.

ANDY: *to Beth* She announces that her name is Emily.

BETH: *to Oz* She announces that her name is Emily.

EMILY: Who are you?

OZ, BETH, ANDY: … YOU ANNOUNCE THAT YOUR NAME IS EMILY.

EMILY: I ANNOUNCE THAT YOU ARE BORING.

OZ: I ANNOUNCE THAT YOU ARE BORING.

EMILY: I announce that I am leaving.
 

Have I mentioned that I don't like gossip parties? Last but not least, we have the old “favourite” known as Byzantine Fault Tolerance. The name itself should give it away as being an unintuitive idea, as neither you, nor I, nor the NSA, are Byzantine Generals, and the attack at dawn is a ruse anyway so we can get a few hours peace before lunch. So, lets all suppose I am in the basement, and want to go to lunch with a few friends. This is what the experience would look like if it resembled a BFT protocol:


EMILY: I announce my desire to go to lunch. 

BETH: I verify that I heard that you want to go to lunch. 

ANDY: I also verify that I heard that you want to go to lunch. 

CHRIS: YOU DO NOT WANT TO GO TO LUNCH. 

EMILY: OH NO. LET ME TELL YOU AGAIN THAT I WANT TO GO TO LUNCH. 

CHRIS: YOU DO NOT WANT TO GO TO LUNCH.

BETH: CHRIS IS FAULTY.

CHRIS: CHRIS IS NOT FAULTY.

ANDY: I VERIFY THAT BETH SAYS THAT CHRIS IS FAULTY.

BETH: I VERIFY MY VERIFICATION OF MY CLAIM THAT ANDY CLAIMS THAT I KNOW CHRIS.

EMILY: I AM SO HUNGRY.

CHRIS: YOU ARE NOT HUNGRY.

ANDY: I DECLARE CHRIS TO BE FAULTY.

CHRIS: I DECLARE ANDY TO BE FAULTY.

EMILY: I DECLARE EMILY TO BE SLIPPING INTO A DIABETIC COMA.

ANDY: I have already left for lunch.


Ultimately, we need to stop obsessing over distributed systems and how they do or don't talk to each other. I don't blame people for being interested in this hideously complex, excruciatingly irrational field, in the same limited sense that I do not blame drug addicts for wanting to acquire and then consume cocaine. The desire to make computers communicate, and then make that communication fast and reliable is a powerful one, growing with the internet in size and scale. However, unfortunately, this addiction, if left unchecked, will inescapably lead to madness and/or reports containing no less than 453 pages of diagrams (with appendices, containing the proofs), and these reports will STILL be incoherent to the educated expert. 

![](http://yourdon.com/strucanalysis/wiki/images/c/c1/Figure920.jpg "As you can see, we removed the labels for simplicity")

Even if we break the will of the machines with formal proofs, and restrictive protocols, and cryptography, we will never be able to put ourselves inside the computer. And as such, we will be left helpless and crying as the internet explodes and the computers decide that gossip was overrated after all.

