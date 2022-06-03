---
layout: post
read_time: true
show_date: true
title: "My First NFT Collection in Polygon Mainnet"
date: 2022-04-20
img: posts/20220420/mandos.png
tags: [creativity, NFT, IPFS, generative art]
category: opinion
author: Luis Ignacio Callero
description: "NFT project with Generative Art and IPFS"
---
Recently I created a video describing what is, and what are the benefits of generative art in the NFT creation scope.

<iframe width="560" height="315" src="https://www.youtube.com/embed/DK-SshPEBRA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Generative art has allowed me to generate thousand of images that were finally converted into NFT. 

But let us start from the beginning:

### Graphic Design
This stage was not a simple task. My team mate [Juan Meregone](https://www.linkedin.com/in/juanmeregone) was the one in charged of carefully designing the different layers with Inkscape and Photoshop editors. He then exported those layers and group them in folders with descriptive names to allow me to understand the position they should be inserted in the final image.

### Generative Art
Once he had all the layers set up, I would use some nice code from [hashlips](https://github.com/HashLips/hashlips_art_engine) and with a few setting updates, it was ready to be used for our project. Thanks hashlips for sharing this great generating tool!!
A thousand different images were generated including some that are rare which means that a specific layer is unique or probably not as frecuently used by other images.

### Decentralized Images
If we are planning to create NFTs which is part of a decentralized world, we need a good counterpart to store the images.
So, once all the unique images were successfully generated, I used the great benefits of decentralized hostings of IPFS (Inter Planetary File System) to upload and store my images. I uploaded all of them as a folder and IPFS in return provided a CID (Container Identifier). This CID is now part of my path to access my images in the IPFS.
I would then generate a json file for each one of the images with the script provided in hashlips project. This json file contains some information as: id, image location, description, etc.
All json files will also be uploaded to IPFS and a new CID for that folder is provided in return.

<tweet>Pinata Cloud is a great tool to easily get access to IPFS since it also includes the "pin" option, ideal for NFTs since it allows for the images to remain "for ever" accessible</tweet> 

### Minting NFTs
Using the ERC721 contract template from [OpenZeppelin](https://docs.openzeppelin.com/contracts/4.x/erc721#:~:text=ERC721%20is%20a%20standard%20for,across%20a%20number%20of%20contracts.) I was able to deploy the NFTs initially on the Polygon testnet (Mumbai) and finally on the Polygon Mainnet.

### Final Product in Open Sea
You can access our [NFT Collection](https://opensea.io/collection/mandos-this-is-the-way) to check out how it looks in OpenSea NFT marketplace.


![Generative Art Image](./assets/img/posts/20220420/mando_large.png)
<small>[This mandalorian](https://opensea.io/assets/matic/0xc3b2d1fe02bc15182d676e59e3d3f5fe4ff41ac1/6) is the product of a generative art</small>

I really believe this was a great learning experience. Also was my first implementation to a Production Blockchain, since all of my previous projects were deployed in testnets.

<small>For a more detailed description of this deployment please visit the [NFT Repository](https://github.com/luigicallero/NFT_Mandalorians)</small>