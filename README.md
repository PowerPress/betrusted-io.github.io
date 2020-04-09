Betrusted is a protected place for your private matters. It's built
from the ground up to be checked by anyone, but sealed only by you.
Betrusted is more than just a secure CPU -- it is a system complete
with screen and keyboard, because privacy begins and ends with the
user.

<video width="100%" controls autoplay muted><source src="https://raw.githubusercontent.com/betrusted-io/betrusted-io.github.io/master/assets/media/betrusted_intro_450p.mp4" type="video/mp4"></video>
[1080p version](https://bunniefoo.com/betrusted/media/betrusted_intro_1080p.mp4)

## The Birds, the Bees, and the Private Keys

A hacked phone or laptop means all of your passwords, private keys,
authenticator tokens and other secrets are potentially compromised. To
guard against this, systems are starting to incorporate physically
distinct
"[enclaves](https://developer.apple.com/documentation/security/certificate_key_and_trust_services/keys/storing_keys_in_the_secure_enclave)"
(aka [secure
elements](https://www.ledger.fr/2018/12/03/a-closer-look-into-ledger-security-the-secure-element/)
or [TPMs](https://en.wikipedia.org/wiki/Trusted_Platform_Module)). An
enclave is like having a safe in your house: even if the lock on the
front door is broken, the thief still can't access the contents of the
safe.

Today's enclaves protect only certain cryptographic secrets, such as
private keys. These enclaves lack human-friendly I/O and must delegate
the task of rendering and recording information to a less secure
host.

This leads to an important nuance: protecting private keys is not the
same thing as protecting your private bits. A remotely-controlled
keyboard logger can still record your passwords as you type them; a
screen grabber can still read your messages, photos, and authenticator
tokens as easily as you can.

Betrusted solves this problem by incorporating easily auditable
Human-Computer Interaction (HCI) elements to the security enclave.
Betrusted ensures that human-readable secrets are never stored,
displayed, or transmitted beyond the confines of the betrusted device:
betrusted is a security enclave with human-friendly I/O.

## HCI-driven security model

[HCI](https://en.wikipedia.org/wiki/Human%E2%80%93computer_interaction)
stands for Human-Computer Interaction. It's about making computers
usable.

Adding human I/O to an enclave means tackling the diversity of human
language without compromising security. Thus a key challenge for
betrusted is striking a balance between best security practices and a
native-language HCI: more features means more attack surfaces, while
too few features renders the device too difficult to use.

Therefore, correctly scoping the HCI aspect is critical. Betrusted's
HCI scope includes text and voice messaging support.

* The [HCI rationale](/hci-rationale/) page explores the core HCI
requirements.
* The [betrusted architecture](/betrusted-architecture/) page covers
how HCI and security requirements come together into a single device.

## Building betrusted

Trust starts with transparency. Food is labelled with their
ingredients, and subject to routine tests for quality and
contamination. This keeps us safe from foodborne illnesses. As long as
technology remains a black box, we should not be surprised that bad
actors can hide viruses in our devices.

Betrusted aims to build a full technology stack, including silicon,
device, OS, and UX, that is open for inspection and verification by
anyone: experts, governments, and users are free to audit, critique,
confirm and improve its ability to keep secrets. You, the user, get to
pick which version or provider for betrusted you trust the most. Thus,
the only secrets in betrusted are the ones you choose to seal in it.

The depth of this tech stack represents a significant engineering
effort, spanning multiple disciplines across the techology
spectrum. We welcome the contributions of all free/libre software developers:
please visit [our github repo](https://github.com/betrusted-io/).

The project is currently at the early hardware prototype stage. The
current plan divides the project into three phases: a developer-only
alpha; an early-adopter beta; and finally, a consumer-ready product.

Learn more about the [betrusted development plan](/dev-plan/).

## Betrusted device concept

**Betrusted is not a phone**: it is a secure enclave with auditable
input and output surfaces. Betrusted relies on sharing your existing
connectivity -- such as your phone or cable modem -- to access the
Internet. Say you're on the road and you want to securely message a
friend. You would tether betrusted to your phone's wifi, so that the
phone is just an untrusted relay for encrypted messages coming too and
from betrusted. The only place the decrypted messages will ever appear
is on the trusted screen of a betrusted device.

The first generation of betrusted will incorporate a WiFi
interface. Read more about how [betrusted handles
networking](/betrusted-architecture/#network-interface) to understand
how your betrusted can be extended to handle your favorite network
interface.

As a secondary device, betrusted aims to occupy a minimal footprint.
The typical usage scenario integrates betrusted into the protective
case of your existing mobile phone. This usage scenario requires
betrusted to be physically as thin as practical. This "thin as
practical" criteria influences virtually all of the design decisions
around the device hardware.

betrusted is also designed with a special low-power consumption
"memory LCD" screen that can display information all day without
draining its battery. This always-on feature allows betrusted to serve
as a kind of notepad for your life's private details. For example,
saving bitmap images of your airplane boarding passes on betrusted
allows you to board an airplane without having to turn on your phone.

Below are some concepts to give an idea of what the betrusted device
might eventually look like.

### First-Generation Alpha Hardware

The alpha hardware is implemented using a FPGA containing a RISC-V
soft core. The primary goal of this phase is to solidify the specs of
the eventual betrusted system through development and testing on a
looks-like, works-like prototype.

![](assets/images/betrusted-quarter2.jpg)

Above is a photo of an early alpha hardware unit. A superset of
proposed features are represented in this prototype to facilitate HCI
experimentation.

Read more about the [alpha hardware FPGA](/betrusted-architecture/#developer-fpga-system).

# More Info

Please visit the [betrusted
wiki](https://github.com/betrusted-io/betrusted-wiki/wiki) for more
technical information. The main [betrusted github
repository](https://github.com/betrusted-io) will also begin to fill
in as more technical details come online.

## Morsels you may be interested in

* [Avalanche Noise Source](/avalanche-noise) design notes

## Who is behind betrusted?

The betrusted-io github repository's people page [lists the
developers](https://github.com/orgs/betrusted-io/people) that have [elected to reveal their
participation
publicly](https://help.github.com/en/articles/publicizing-or-hiding-organization-membership).

The administrative contact for the betrusted.io project is [Andrew
'bunnie' Huang](https://en.wikipedia.org/wiki/Andrew_Huang_(hacker))
([@bunniestudios](https://twitter.com/bunniestudios)/[blog](https://bunniestudios.com)).

<center><img src="https://nlnet.nl/logo/banner.png" width="20%"> <img src="https://nlnet.nl/image/logos/NGI0_tag.png" width="20%"></center>

The Betrusted team is funded in part through the [NGI0 PET
Fund](https://nlnet.nl/PET), a fund established by NLnet with
financial support from the European Commission's [Next Generation
Internet](https://ngi.eu/) programme, under the aegis of DG
Communications Networks, Content and Technology under grant agreement
No 825310.

### Navigation

* **Betrusted**
  * [HCI Rationale](/hci-rationale)
  * [Betrusted Architecture](/betrusted-architecture)
  * [Development Plan](/dev-plan)
  * [Avalanche Noise Source Design](/avalanche-noise)
