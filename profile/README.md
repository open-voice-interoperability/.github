# The Open Voice Interoperability Initiative #
Welcome to the GitHub repositories of the Open Voice Interoperability Initiative! The **Open Voice Interoperability Initiative** is a project of the Linux Foundation AI and Data Foundation. It aims to revolutionize the conversational AI landscape by enabling voice and conversational AI systems to function like the web. Currently, conversational assistants operate in isolated walled gardens, confining users to a single proprietary ecosystem. The initiative proposes a future where users can seamlessly interact with any assistant or language model, just as they do now when navigating web pages.

Our approach involves defining, developing, and promoting standards, starting with an open, universal application messaging protocol or programming interface (API) called the Open Floor Protocol (OFP). The Open Floor Protocol consists of three specifications, the Conversation Envelope, Dialog Events, and the Assistant Manifest. This API allows assistants to interoperate across platforms, facilitating seamless communication and content transfer.

Our GitHub repositories are where you can find our specifications, documentation, language libraries, sample floor managers, and sample implementations.

## Why Interoperability for Conversational Assistants? ##
Interoperability is crucial for user access, opportunity, and commercial freedom in the evolving conversational AI domain. Unlike the World Wide Web, where browsers allow users to freely access billions of web pages based on standardized protocols, conversational assistants currently operate in closed ecosystems. Interoperability among conversational assistants is inspired by the web's open ecosystem, allowing users to switch between assistants effortlessly and access diverse sources of information.

## The Open Voice Interoperability Initiative's Approach ##
Standard message formats, such as the Conversation Envelope, Dialog Events, and the Assistant Manifest, are being developed for conveying information between assistants that enables them to collaborate on addressing users' goals. 
The **openfloor-docs** repository contains these specifications and always carries the current published version of the Open Floor Protocol.

## The Standards Development Process ##
We advocate for developing interoperability protocols through an open, transparent, and participatory process. This involves collecting and analyzing case studies, publishing requirements and specifications for review, sharing work through webinars and demonstrations, maintaining a repository of documents and code, and encouraging developer involvement.

## Future Work: The Open Voice Interoperability Roadmap ##
Open Voice Interoperability plans to address issues like the discovery and location of conversational agents and to address important security and privacy concerns. The roadmap also includes investigating how a universal API can simplify development and ensure consistency across services.

## How Can I Get Involved ##
The initiative invites participation from developers, researchers, and organizations interested in shaping the future of conversational AI. Explore our [reference floor manager](https://github.com/open-voice-interoperability/floor-implementations) and [sample agents](https://github.com/open-voice-interoperability/implementation-examples), comment on the specifications, and most importantly, try out the specifications with your conversational assistants.

### Developer resources
- **[openfloor.dev](https://openfloor.dev)** — an independent, developer-focused guide to building with the Open Floor Protocol: tutorials, walkthroughs, and quick-start material.
 
## Repositories ##
Our work spans a few repositories. If you're new, read the
specifications first, then pick the library for your language, then look at
the floor and the examples to see how agents are wired together.

### Specifications & background
- **[openfloor-docs](https://github.com/open-voice-interoperability/openfloor-docs)**
  — the normative Open Floor Protocol specifications: the Conversation
  Envelope, Dialog Events, and the Assistant Manifest, with schemas and
  worked examples. Start here. This is the source of truth for what a
  compliant message looks like.
- **[background](https://github.com/open-voice-interoperability/background)**
  — supplementary material on the initiative: motivation, history, and
  supporting write-ups.

### Libraries for building agents
- **[openfloor-python](https://github.com/open-voice-interoperability/openfloor-python)**
  — the reference Python implementation of OFP. Envelope / event / manifest
  types, payload validation, and a `BotAgent` base class you subclass to
  build a compliant assistant. Most of the examples here are built on this.
- **[openfloor-js](https://github.com/open-voice-interoperability/openfloor-js)**
  — a strict, standards-compliant TypeScript library for OFP, for building
  agents and clients in JavaScript / TypeScript.

  ### The floor, and worked examples
- **[floor-implementations](https://github.com/open-voice-interoperability/floor-implementations)**
  — implementations of the **Floor Manager**: the component that owns
  conversation and floor state for a multi-agent conversation and routes
  every event between participants (Pass-Through to all conversants,
  Delegate-to-Convener for coordination). Includes `web-floor`, a Flask
  gateway plus browser UI that acts as a spec-compliant floor manager you
  can run locally and point agents at.
- **[implementation-examples](https://github.com/open-voice-interoperability/implementation-examples)**
  — runnable OFP agents and multi-agent teams. Single agents (e.g. a NASA
  space assistant, a world-time agent, a fact-checker, a deliberate
  hallucination demo), an `agent-template` with full event handling, and
  full **teams** — a cafeteria-operations team and a startup-analysis team,
  each a convener plus domain specialists that run on a floor from
  `floor-implementations`. Every agent is standalone and can be reused in
  other conversations.

### How they fit together
`openfloor-docs` defines the messages. `openfloor-python` / `openfloor-js`
let you build participants that speak them. `floor-implementations` provides
the floor that connects participants and moves the conversation along.
`implementation-examples` contains current open-source OFP agents that you can test in your own environment.
For more information, see:

[Resources](https://github.com/open-voice-interoperability/.github/blob/main/profile/resources.md)

[FAQ](https://github.com/open-voice-interoperability/.github/blob/main/profile/FAQ.md)
