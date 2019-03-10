# claim.it

> _claim.it_ is a project developped during 2019 ETHParis hackathon. Check it on [DevPost](https://devpost.com/software/claim-it).

![identity board](https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/000/777/083/datas/gallery.jpg)

## In the beginning..

.. were identity and claim smart contracts.
ERC 725 and 735 had been receiving a whole lot of hype for several months, and the first robust implementations were finally starting to show up.
But DApps taking advantage of their promising features were not there yet. In fact, neither were dev tools that would make it easier for the community to take over these new standards and make the most out of them.

At this point, the missing part was an **easy-to-deploy dev tool to monitor and interact with standardized claim systems**, showing an interface so friendly that it could even be integrated right away in final products.

## _claim.it_ is..

* **super simple** : it runs with any Ethereum blockchain. Just specify the address of a _claim registry_, run `docker-compose up` and that's it ! A webapp is deployed showing you **live** all new claims from users to users in a nice intuitive way. Integration with your favorite browser wallet is supported out of the box and you can use it to create, transfer, update, delete and experiment with new claims in the blink of an eye.
* **exhaustive** : all the claims you want to watch are there, in front of you, with all attached information updating live as new events occur.
* **built to last** : designed on emerging standards, the tool should smoothly adapt to identity and claim smart contract standards evolution.
* **versatile** : you can use _claim.it_ as a dev tool to quickly experiment with claims. But everything is in place for you to just take the live stream of claims and integrate it to your own app for instance. The sky's the limit !

## But _claim.it_ really is..

### An effort in standardization

ERC 725 and 734 for identities, 735 for claims, 780 for claim registries. Studying in depth these new standards made it clear that some issues could already be solved regarding open discussions on these ERCs.

What would be the reason for multiple claim registries to compete ? Should a key manager contract always be separated from proxy ? etc.

We are quite proud of this time of reflection which happened to play a major role in the complete project, and we hope that our conclusions may be food for thought in the community.

### A complete API

The RESTful API, coded in _Go_ around the [Gin Gonic](https://github.com/gin-gonic/gin) framework, backed by a _MongoDB_ database, answers to clients' calls and reacts to on-chain events. It contextualizes and brings intelligence to on-chain claims.

### A smooth interface

The _React_ webapp stays up-to-date live with _push_ notifications and keeps the interface clean with features like full integration of the [ENS](https://ens.domains/) resolver.
It fully integrates with your favorite browser wallet to help you not only get access to enriched claims but also interact with them.

And if  you are interested by _data availability_, the webapp may always be out there if you choose to deploy it with [Arweave](https://www.arweave.org/) as we did for our demo !



## And _claim.it_ will be..

.. a monitoring system for encrypted and traceable claims.

*How is that ?* claims store on-chain the issuer and recipient's addresses, most of the time together with an IPFS URI. Everything seems public and clear under these assumptions.

But what if:
1. the claim stored on IPFS is encrypted
2. identity smart contracts like ERC 725 show to the world your public key
3. proxy-reencryption is used to deliver, in a trustless manner, private claims to new recipients while tracing claim holders

That is the best we can hope for _claim.it_. Maybe you could be a part of it ?

[GitHub - Blockchainpartner/claim.it](https://github.com/Blockchainpartner/claim.it)