# Getting started with the Web #

## Background ##

Producing websites is a simple matter, all you need is a computer with Server software and some files the server can send people. In the background is the network, quitely doing your bidding quite quickly these days. To understand web design, you must first understand your medium: the internet.

The internet, over simplifying greatly, is a network of computers. In fact, a network of networks of computers with a series of common languages more officiously known as Protocols. You actually know at least one of them but we'll go through the most important ones.

1. HTTP
Hypertext Transfer Protocol is the most front-facing web language; you see it everywhere.

    ex: http://www.twitter.com

What you have here is an HTTP call to a Domain Name. What's behind the scenes is a verb: GET, POST, PUT, you get the picture. These verbs tell the server "I want THIS file" or "Here's some data" or "Change my contact information." Typing that into a browser asks the computer that stores Twitter for a file, namely the twitter home page. It (usually) complies and now you're there. The process by which that occurs is TCP/IP.

2. IP
Okay, I don't really want to get into that yet. First let's talk about the DNS or Domain Name System. That's just a huge list of Domain Names (like www.twitter.com) that point to (here it comes) an IP address (Internet Protocol address, why it isn't IPA we'll never know) that allows you to locate the server where all those tweets and such live. In reality, Twitter is likely hosted on serveral servers to load-balance all the traffic. This is going to be a recurring theme; distributing resources is going to be a big part of how to actually have a production-grade website.

3. TCP
Lurking in the shows is TCP, Transmission Control Protocol. It is one of a couple different protocols that handle "low-level" stuff. Basically, we have a ton of data packets and only so many wires to send them on. All of these packets can clog the wire if they are not sent efficiently so it is a way to handle that problem so that your Twitter page comes back with all those lovely tweets and they are "pristine," that is, not messed up by sending them through a physical medium subject to pesky things like noise. You don't really need to know much about TCP other than that it can make a connection a bit slower by enforcing data integrity, our "pristine" tweets, the Twitter logo, etc..

Let's go over how these things work together.

The Request-Response Cycle

This is the core of how the web functions. You send a GET, POST, etc. request (HTTP), from now on we'll call this the Client side, to a domain name that is mapped to an IP address which then travels down the wire and ends up at the machine whose Server software knows how to read and RESPOND to the request which is what comes back to you. What comes back is a file with a header (you don't usually see that) that tells your browser what happened on it's end like "Cool, here's your file," "thanks for the yummy data" or "I DON'T KNOW WHAT YOU ARE TALKING ABOUT!" in the form of a status code. You probably have seen a 404 before - it means "Couldn't find that here," cryptically, "Resource does not exist." The request-response cycle is how your hunger for tweets gets satisfied: you, the client, ask or request delicious tweets and the server responds with tasty, poorly written morsels. We'll always have to keep the request-response cycle in mind but don't fret, your tools will get angry and tell you if you aren't respecting the protocols.