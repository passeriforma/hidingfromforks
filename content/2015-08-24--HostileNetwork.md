Title: The Network is Hostile
Date: 2015-08-24
Category: Computing
Tags: computing, security, NSA, metadata, awks

2013 was a pretty integral year from a cybersecurity perspective, with the release of large quantities of files from the NSA which confirmed that the American government was actively spying on {insert name/country here} This included gems such as tapping the fiber connection supporting the UN, as well as many others.

Since then, there have been a series of further leaks and revelations on this topic, and a lot of arguing about whether this is actually news from people in tech [0]. As with all these things, the answer is a combination of yes and no, though I suspect that a majority of people are starting to suffer from revelation fatigue (I know I am).

But this article isn’t about the latest revelation that, in fact, the NSA is further into our networks than we ever thought before. Rather, this is about what the leaks have taught us, from beginning to end, and (perhaps more importantly), what these revelations mean for how we should be thinking and acting on the internet. 

**The network is hostile.**

The first rule of internet security is that there is no internet security. This assumption is based on the design of the internet, where unknown third parties are responsible for handling and routing your data. No matter whether you’re using Tor or a VPN or any “safe” router you like, there is no way to ensure your packets will be routed as you want them, and absolutely no way to ensure that they won’t be looked at. 

With the way things are, it's easy to think that this is a new problem. However, nothing could be further from the truth. As far back as ARPANET it was known that connecting from A to B meant passing through a variety of untrusted machines. At that time, the only thing protecting your data was a gentlemen’s agreement not to look. Somehow, we haven't progressed much from this stage since.

From the reaction to the leaks, we can see that even though it was “obvious” that anyone could be spying on our data, we were only aware of it intelectually. Even knowing that the worst was possible, we still chose to believe that leased lines from reputable providers would make us safe. If nothing else, these recent leaks have thoroughly refuted this assumption.

**We don't encrypt enough.**

A surprising lesson has been that over 20 years since development of SSL encryption, we still send enormous amounts of valuable data as plaintext. 

Even in 2014, things like Yahoo Mail were routinely routed in cleartext (good job guys) [1]. This doesn't just make it vulnerable to people like the NSA, but also to everyone - everyone - on your local network. And it gets better; even if you managed to get all your data sent encrypted across the wider network, companies would transmit the same, unencrypted, data naively through inter-datacenter connections. And guess who was sitting on those lines (hint: it was the NSA) [2].


[Look, they’ve even included smileys to show how happy they are at the poor effort!](https://upload.wikimedia.org/wikipedia/commons/f/f2/NSA_Muscular_Google_Cloud.jpg "Well, you tried")

Its easy to think that were doing much better now than we were in 2013, and perhaps in some ways we are. But as long as were sending and tolerating unencrypted packets, we have a long way to go.

**Its the metadata, stupid.**

But even if we miraculously manage to achieve 100% encryption, we still haven't solved the whole problem. Session metadata in today’s protocols leaks enormous amounts of data, and we have no way to defend against it. 

Some examples of metadata: protocol type, port number, routing information, session duration, source and destination address and communication bandwidth. Unsurprisingly, traffic analysis remains a particular problem as this can leak vast amounts of information about a user’s browsing habits.

None of this is news to us in Australia, after our metadata laws of yesteryear. The problem is that there’s so little we can do about it. Networks like Tor protect the identity of connection endpoints, but with huge cost in bandwidth and latency, plus they only offer limited protection when faced with a motivated global adversary [3]. IP tunnels only pass the problem to a different set of trusted components, and these too can be subverted.

**Take it all**

An eye opening fact of the intelligence leaks has been the sheer volume of data that agencies have been willing to collect. Famously exemplified with the US data collection policies, its more worrying cousin is “full take” devices like TEMPORA [4], which sits atop the backbone of the internet and reads it all.

If we just look at the collection of this data, rather than how its accessed, it looks like the limiting factors are purely technical. i.e. data collection is a function of processing power, bandwidth and storage. Does that sound reassuring? Because it shouldn't.

This is because while human communication bandwidth is increasing, storage and processing power is increasing faster. With some basic filtration (lists of keywords, anyone?) and no encryption, this form of data collection is increasingly headed towards being the norm rather than the exception. 

**We’ve seen the future, and it’s as bad as we thought**

Even if you’re not inclined to see the NSA as the bad guy (and I know some people who don't), theyre hardly the only agency able to subvert a global network. Ive already mentioned the UK, but other nations such as China and Russia (apologies for bringing up Cold War boogeymen) are also laying cable, and are thus increasingly able to lay their own backdoors within them. Its important to realise that someday traffic will be flowing through networks controlled by governments that are not your friends and want to see you come to harm. And with the current state of our networks, you're giving them the power to do just that.

If you're concerned about the future, then the answer is to finally, truly believe our propaganda about network trust. We need to learn to build systems today that can survive in such a hostile environment. Failing that, we need to adjust to a very different world.

[0] https://news.ycombinator.com/item?id=10066014 

[1] https://grahamcluley.com/2013/10/yahoo-ssl-https/ 

[2] http://tinyurl.com/ofcfkj8 

[3] http://www.spiegel.de/media/media-35541.pdf 

[4] https://en.wikipedia.org/wiki/Tempora 

