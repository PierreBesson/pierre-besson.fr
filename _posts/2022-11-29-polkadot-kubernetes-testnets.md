---
layout: post
title: Deploying Polkadot and Parachain Testnets on Kubernetes
date: '2022-11-29 12:00:00 +0100'
tags: 'polkadot,testnet,kubernetes'
categories: articles
---

I gave this talk at [Sub0 2022](https://sub0.polkadot.network/) in Lisbon.

# Video

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/Iicj4Lfa-nU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Summary of the talk

The goal of this talk is to showcase how Parity leverages Kubernetes to operate multi-chains testnets. We will take this opportunity to introduce our suite of recently open sourced tools including our helm charts collection which helps with deploying nodes and useful services (telemetry, faucet, etc.) as well as the testnet-manager which provides a UI and API to facilitate the setup of validators/collators and automate the onboarding of parachains onto testnets.

# Links

### Github repos

Polkadot kubernetes testnet example deployment:
- [PierreBesson/polkadot-kubernetes-testnet-example](https://github.com/PierreBesson/polkadot-kubernetes-testnet-example)


Repositories maintained by the Parity Devops teams
- [paritytech/ansible-galaxy](https://github.com/paritytech/ansible-galaxy)
- [paritytech/helm-charts](https://github.com/paritytech/helm-charts)
- [paritytech/testnet-manager](https://github.com/paritytech/testnet-manager)

### Slides

- [Slides](/files/sub0-2022.pdf)
