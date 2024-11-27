---
title: "org/issue/37: Tagging this repo"
date: 2024-04-21 01:16:24 +0000
author: dbluhm
categories: ["DIF"]
tags: ["org"]
permalink: /org/issue/37/
comments_file: DIF-org-issue-37_comments
excerpt: >
  The group discussed this on the 2024-11-19 telecon:
---
The concept of tagging this repo came up on the Aries WG call on Nov. 15, 2023. I wanted to continue that discussion here:

As prior art, consider this text from: https://github.com/hyperledger/aries-acapy-plugin-toolbox#aca-py-version-compatibility

> ## ACA-Py Version Compatibility
> 
> To avoid a confusing pseudo-lock-step release, this plugin is versioned independent of ACA-Py. Plugin releases will follow standard [semver](semver.org) but each release will also be tagged with a mapping to an ACA-Py version with the format `acapy-X.Y.Z-J` where `X.Y.Z` corresponds to the ACA-Py version supported and `J` is an incrementing number for each new plugin release that targets the same version of ACA-Py.
> 
> You should look for the most recent release tagged with the version of ACA-Py you are using (with the highest value for `J`).

This was a convention that the toolbox plugin adopted (back when we were actively working on it). I think tagging the whole repo will be challenging to do meaningfully; for the toolbox plugin, we needed to keep track changes of the plugin itself as well as the versions of ACA-Py it was compatible with. The plugins should be able to evolve and gain features and be able to version themselves to communicate when new features are added.