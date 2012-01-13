---
layout: post
author: Garrett Serack
twitter: fearthecowboy
title: What is the "Master Key" that is used to create the key-pair and PPID?
tags: ['developer', 'signing']
docid: "news:20070205"
---

James Manger asks a couple of pertinent questions, considering my last post on PPIDs:

> What is the "Master Key" that is used to create the key-pair and PPID? Could youexplain this process?

Whoa! You might as well ask what's in them sausages you just ate...

Seriously, the Master key is a posse' of bytes that we use to seed the entropy for creating the PPID and the private/public key-pairs.

The Master Key is generated by the CardSpace built-in STS when you create a personal card, and is stored with the rest of the data in the cardstore. It is the only peice of data in the card that the user doens't have control over.

I don't have the exact algorithm in my hands (I'm at the RSA Conference in San Francisco!), but I'll post it when I get back. If I recall correctly, it's kina along the same lines as GUID generation (takes a bunch of different data bits) and corrals them together to generate a stream of bytes.

I always like it when people ask questions about CardSpace's implementation, the cryptography behind it or really, any other security questions... It reminds me of somethin' my pappy told me... **"Always take a good look at what you're about to eat. It's not so important to know what it is, but it sure is crucial to know what it was"**. That kind of advice works really well for security, just as it did for those odd-tastin' sausages we barbeque'd up that night.