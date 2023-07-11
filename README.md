# The Decentralized Web of Trust Reputation system

## Introduction

In the era of burgeoning digital interactions and information exchange, establishing trust in an online environment is more critical than ever. To address this need, we introduce our innovative Decentralized Web of Trust Reputation system. This system lays the groundwork for building a more trustworthy digital world, enabling entities to express trust, neutrality, or distrust towards others in a structured, transparent, and dynamic manner.

At its core, the system operates using the simple values of 1, 0, and -1 to indicate trust, neutrality, and distrust respectively. The primary actors in this system are 'Keys' and 'Items.' A 'Key' is akin to a person who can vouch for the credibility of another person or a piece of information, while an 'Item' is the information itself, like a document or a news article.

In our system, Keys can make trust claims towards other Keys or Items, effectively building a web of trust that's decentralized and ever-evolving. These trust claims create a network where the trustworthiness of any given Item can be verified against the accumulated opinions of Keys within their trust network.

The design of this trust network includes features to address common issues of trust in digital spaces. For instance, the system allows for trust claims to be updated or withdrawn, mirroring the fluid nature of trust in real life. It also limits the degrees of separation for trust claims to a maximum of three, ensuring trust isn't diluted by overextended connections. Moreover, when multiple trust claims are present, the system can intelligently resolve conflicts and prioritize closer connections, akin to placing more value on a friend's opinion than a friend-of-a-friend's.

Through this Decentralized Web of Trust Reputation system, we aim to enhance the credibility of online interactions, facilitating a more reliable exchange of information and fostering a digital environment where trust is robust, transparent, and adaptable.

In the following sections, we will delve into the detailed workings of this system, providing rules and examples to illustrate its functionality. Whether you are an end user, developer, or researcher, this guide aims to give you a comprehensive understanding of our unique trust system and its potential applications.

## The rules

1. **Issuing Trust**: In this system, an entity known as a 'Key' can assign a trust value to another Key or an Item. Think of it like a person (the Key) vouching for another person's character or a piece of information (the Item). 

2. **Trust Values**: The values that can be assigned are 1, 0, or -1. Assigning a '1' means the Key trusts the other Key or Item. A '0' signifies neutrality, and it's used to reset previous trust values. A '-1' means the Key doesn't trust the other Key or Item.

3. **Trust Updates**: A Key can issue multiple trust claims, but each new claim towards the same Key or Item overwrites the previous one. It's like updating your opinion about someone or something based on new information or experiences.

4. **Network of Trust**: All these trust claims form a graph structure, where the Keys and Items are the nodes, and the trust claims are the edges connecting them.

5. **Trusting Content**: If a Key trusts another Key, then any content or information vouched for by that trusted Key is also considered trustworthy.

6. **Degrees of Trust**: A Key can vouch for trustworthiness up to 3 degrees away. It's similar to a friend-of-a-friend situation: you trust your friend (1st degree), your friend trusts another friend (2nd degree), and that friend trusts another (3rd degree). Beyond this, the system won't consider any further degrees of trust.

7. **Checking Trust**: This layered system of trust lets a Key check the trustworthiness of information against the entire network of trust claims.

8. **Resolving Conflicting Trusts**: When a Key (at degree 2) has multiple trust or distrust claims from Keys at degree 1, the system adds them up. If the total is greater than 0, the Key or Item is considered trustworthy, and the path is followed. But if there's a distrust claim, that path isn't followed.

9. **Prioritizing Trust**: Trust claims from closer degrees have more weight. This reflects the idea that the opinion of a close friend is more valuable than that of a friend's friend.

Let's consider an example for further clarity. Imagine four friends: Alice, Bob, Charlie, and Dana. Alice trusts Bob (1st degree trust), Bob trusts Charlie (2nd degree trust for Alice), and Charlie trusts Dana (3rd degree trust for Alice). 

In this scenario, if Dana shares some information, Alice would consider it trustworthy because Dana falls within her 3-degree trust network. Now, let's say Bob changes his mind about Charlie and issues a distrust claim. Then, even though Charlie still trusts Dana, Alice would no longer trust Dana's information because her path to Dana (via Bob and Charlie) is broken by Bob's distrust claim.

This example illustrates how the system enables trust to be earned, distributed, and revised in a network, ensuring that only reliable information is accepted.
