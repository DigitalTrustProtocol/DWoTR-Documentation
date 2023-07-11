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


## Trust is subjective

Trust, by its very nature, is subjective and heavily influenced by personal experiences, beliefs, and values. The same applies to our Decentralized Web of Trust Reputation system. It’s important to note that trust established through this system is inherently subjective, reflecting the unique perspectives and contexts of individual users, rather than claiming to offer an absolute or objective truth.

When a Key makes a trust claim, it's expressing its personal assessment, which can vary greatly from one Key to another based on their unique experiences and judgments. Similarly, when a Key evaluates the trustworthiness of an Item, the outcome is influenced by their position in the trust network and the trust claims of the Keys within their network. This allows for diverse views and interpretations, reflecting the complex nature of trust in real life.

This emphasis on subjectivity ensures that each user's experience with the system is personalized, allowing trust to be understood and established in a way that makes the most sense to them. By acknowledging that trust is a nuanced and context-driven concept, our system encourages users to critically evaluate the trust claims they encounter, promoting more informed decision-making and a more authentic online experience.

In this sense, the Decentralized Web of Trust Reputation system is not designed to dictate what is true or false universally. Instead, it provides a framework for users to express, explore, and evaluate trust within their own context, enhancing the richness and diversity of the digital trust landscape.

While the Decentralized Web of Trust Reputation system emphasizes the subjectivity of trust, it's important to distinguish this from the concept of universal truths. Universal truths are facts or principles that are objectively true in all contexts, irrespective of individual perspectives. For instance, gravity's effect on a falling object or the process of photosynthesis in plants are universal truths, unaffected by personal beliefs or trust.

In our system, subjectivity applies specifically to trust claims and relationships, reflecting the personal judgments and experiences of each Key. This does not mean that universal truths can be disputed through trust claims in this system. Facts remain facts, irrespective of whether an individual Key trusts or distrusts them.

Our system is designed to handle personal trust relationships and subjective judgments, not to mediate objective reality or universal truths. Trust claims should be understood as expressions of personal trust, rather than declarations of fact. As such, the system is not intended to replace rigorous fact-checking or scientific investigation, but to complement them by providing a framework for expressing and navigating personal trust in a digital environment.

## Trust is Omnipresent: Navigating Reputation in the Digital World

In the digital world, ratings and reputations are omnipresent. We trust e-commerce platforms' star ratings, we rely on credit scores from financial institutions, and we make decisions based on reviews on social media. These systems, usually operated by corporations and governments, have become an integral part of our digital lives. We accept them as an efficient means of evaluating products, services, and even people's creditworthiness.

However, when it comes to peer-to-peer reputation systems, where individuals rate and review each other, the reception can often be more complex and nuanced. The same mechanisms we accept from organizations can feel intrusive or uncomfortable when implemented on a personal level.

There are several reasons for this hesitation. 

1. **Privacy concerns**: Peer-to-peer reputation systems can feel like an invasion of privacy. The idea of being "rated" by our peers, with those judgments accessible to others, can feel like our personal lives are exposed in ways we can't control. Unlike dealing with corporations or governments, where there's often a level of separation, peer ratings are much more intimate and personal.

2. **Fear of misuse**: There's a concern that such systems could be misused for personal vendettas, leading to reputational damage. This is compounded by the fact that digital reputations can be difficult to repair.

3. **Bias and subjectivity**: People are inherently subjective. Their judgments can be influenced by personal bias, moods, or misunderstanding. In peer-to-peer systems, these personal biases can unduly influence someone's digital reputation.

4. **The complexity of human relations**: Human relationships are complex, multifaceted, and continuously evolving. Reducing this complexity to a single rating or score can feel reductive and unfair.

That said, while these challenges are real, they are not insurmountable. A well-designed peer-to-peer reputation system should address these concerns, providing clear guidelines, robust privacy safeguards, and mechanisms to handle misuse or dispute resolution. Furthermore, such systems should emphasize that they're tools for expressing personal trust, not objective truth, and are meant to complement, not replace, our existing ways of forming and managing personal relationships.

Overall, peer-to-peer reputation systems, like the Decentralized Web of Trust Reputation system, have the potential to empower individuals, allowing us to take control of our digital reputations and navigate the online world with greater confidence and security. They can democratize trust in the digital sphere, but it's vital that they are designed and used with care, respecting our needs for privacy, fairness, and control.
