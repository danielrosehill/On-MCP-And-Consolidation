# On MCP And Consolidation

*Notes and a few resources*

(Point in time: Nov 9, 2025)

## Table of Contents

- [On MCP And Consolidation](#on-mcp-and-consolidation)
  - [Table of Contents](#table-of-contents)
  - [Notes](#notes)
- [The Problems With The MCP Status Quo](#the-problems-with-the-mcp-status-quo)
  - [Problem 1: It's Not Accessible (To Non-Developers)](#problem-1-its-not-accessible-to-non-developers)
    - [FYI: Not Everyone Loves The Idea](#fyi-not-everyone-loves-the-idea)
    - [Why MCP Needs To Be Ordinary Person Useable](#why-mcp-needs-to-be-ordinary-person-useable)
  - [MCP Is Also Hard For Tech Literate Users](#mcp-is-also-hard-for-tech-literate-users)
  - [Developers Don't Want Bundles Of MCP Servers](#developers-dont-want-bundles-of-mcp-servers)
- [MCP Consolidation As A Solution To Several Pain Points](#mcp-consolidation-as-a-solution-to-several-pain-points)
  - [Keywords](#keywords)
  - [Discovery Prompt](#discovery-prompt)
- [Project List](#project-list)
  - [MCP Gateways \& Routing](#mcp-gateways--routing)
  - [MCP Meta-Servers \& Aggregators](#mcp-meta-servers--aggregators)
  - [MCP Orchestration \& Management Platforms](#mcp-orchestration--management-platforms)

## Notes

I like to create Github repos to gather together resources (ie, "Awesome Lists" although I rarely actually use that precise format).

I create these mostly for my own reference. Sometimes, though, I revert to being a humble tech writer (for anyone who stumbles on my Github and wonders, that's my background): the resources are interesting and on my "to check out" list. But what's more interesting is where they fit in the picture.

It's in this vein that I jot down these thoughts. 

# The Problems With The MCP Status Quo

It's a bit of a stretch to describe the state of affairs today as a status quo given that the tech is highly nascent. But nevertheless I thought I would articulate what I see as the two main deficiencies with MCP right now and then share some resources for me, and anyone interested, to explore.

## Problem 1: It's Not Accessible (To Non-Developers)

MCP is fantastic. 

MCP is also - *wait, it's okay to use bad language on Github, right* - a sh*tshow. 

If you're here, and you use Github, then you very likely know what MCP is. 

Sometimes I use tech docs as launching pads for blogs and other content. So in that vein, I'll try to convey the essentials to those who are not in "tech":

I explain the value prop of MCP to my wife a bit like this: "you know how ChatGPT can *chat* with you? But how cool would it be if it could actually do *things* like .... book you a cinema ticket or write an email?"

My wife is an architect (the kind that makes nice buildings happen). 

So I also use local MCPs as pitches to underscore that MCP is actually a far-reaching concept that doesn't just involve providing AI assistants with the ability to interact with (remote) APIs, but also computers at their most fundamental level (the filesystem) and even, through vision, manage browsers: *"imagine if you could send that render out by chatting to an assistant on your desktop?"*

One level deeper (for more technical friends who haven't yet got stuck down the rabbit hole): *"API definitions are great but we need to organise them a little in a standardised fashion for AI agents to be able to use them well as otherwise they're just looking at a gigantic JSON schema. We're kind of chunking it and cherry-picking the functions we wish to make available. We define specific API actions as tools and give them a blueprint."*

### FYI: Not Everyone Loves The Idea

It's good to periodically spend time with normal people to remember that not everybody is instantly enraptured by the same things you find fascinating. 

In response to the ChatGPT email pitch I've heard responses like: "No thanks!". The underlying objective is sometimes security skepticism, sometimes AI fatigue, and sometimes ... folks just don't see the value.  

My observation: 

The ability of AI systems to *buy* things involves a much higher level of trust so we can even stratify receptiveness to agentic AI on this basis and see a good deal of variability:

Much as developers worry about agentic code tools screwing up code-bases (potentially costing them their jobs), non-developers worry about agents potentially going on a YOLO-style Amazon spending spree and bankrupting them.  

But if you see eye to eye on the potential utility of AI systems being able to *do*  things at some level, then folks like me are left with really crappy answers to the question of: *"so, how can I try out MCP?"*

Claude Desktop? Yes, but many folks are happy with ChatGPT (etc). Oh, you can add MCPs to ChatGPT? Sounds cool! But wait ... no, I'm not using "Developer Mode" and I really don't want to touch "code." 

### Why MCP Needs To Be Ordinary Person Useable

There are some inherent contradictions in agentic AI and MCP that rarely get much articulation.

Today, everyone and their grandmother is using AI. Developers are but a slice of the overall picture of AI use. To reach anything like its potential, MCP needs to be accessible. 

The AI agent landscape of today is remarkably backend-heavy. Far less attention goes into how to actually *use* the AI tools that achieve wonderful things through orchestration and, at its furthest reach, the exercise of some degree of autonomous decision-making. 

This is, I believe, a bad direction. In conventional marketing, businesses carefully gauge market demand and then try to fulfill it. For this reason, the ultimate beneficiaries of MCP - ordinary AI users - should not be dismissed or, worse, looked down upon, just because they are not "developers."

MCP's utility extends vastly beyond being nice tooling for agentic workflows. GUIs are a basic standard for what most people consider useable technology and non-developers do not want to wrestle with transport protocols and complicated authentication setups. MCPs have to be easily integrateable with well-maintained and functional AI frontends for most people to be willing to try them out. 

---

## MCP Is Also Hard For Tech Literate Users

Many folks on X proclaim triumphantly: "MCP is too hard for non-devs."

I will save my strident thoughts on the futility of ringfencing "devs" as a separate class of tech workers for another day, but the sentiment, I believe, also misses the mark.

Let's assume that - like me and most people I expect will read this, if any - you're tech-literate enough to be able to install local MCP servers, configure credentials in JSON, etc.

There is still a multiplicity of challenges:

- Poorly maintained MCP servers that do not work. The MCP might lag the API or it might just be stagnant. It's surprising to encounter some of these even among major vendors.
- Copycat MCPs: a popular service may have a wide variety of community MCPs. Besides confusion, this raises justifiable concerns among users about security.
- My pet peeve: the tendency of development tools - IDEs and components - to demand that the user provides a separate `mcp.json` just for this tool or component. This means that developers often waste valuable time creating the same configurations for various tools and that community driven tooling to support more efficient propagation of MCP arrays has had to develop.
- Splintering: volatility even among fairly fundamental concerns like the transport protocol being adopted further a general impression of MCP being too complicated and too chaotic. 

And even if you manage to get past the challenges we are still faced with a basic usability challenge:

MCPs - conceived of in large part as tools predominantly for developers - are "repo first." 

MCP tool definitions pose a context load (although Anthropic is proposing an interesting alternative mechanism). To mitigate against context flood from lengthy definitions, users are presently encouraged to cherry pick the MCPs they use for specific projects. 

This means that MCP is fragmented: if a user who also happens to be a developer is using a local AI assistant which has MCP, that developer doesn't want to have to turn various MCP connections on and off as they shift context between working in an IDE and saving a Netflix playlist. 

One solution (like that Claude Code uses) is to define various scopes of operation, such that users can define a few "always there" MCPs (user level) and project level servers where credentials might be shared. This makes sense but is still a cumbersome solution. 

## Developers Don't Want Bundles Of MCP Servers

MCP opens huge challenges around security and privacy. Locally run MCP servers are an option although they still transmit data to and from the cloud via API.

But local MCPs are environment-bound. Replicating these across computers is tedious. If the goal of MCP is to make AI more useful and fluid then this design frustrates the goal. My takes here are that the way forward lies, instead, in fewer but more carefully managed vendor MCPs that are accessed through cloud endpoints. 

---

# MCP Consolidation As A Solution To Several Pain Points

I created this repo because:

1) I like creating lists of resources for myself to check out
2) I also like writing

So this page is something of a hybrid of both. I organised it in this sequence because I thought the foregoing was important to delineate what I mean by MCP consolidation and share why I think it's both particularly important and - from an organisational standpoint - can be bundled even if the end technologies carry a few different names. 

Above, I mapped out a couple of fundamental challenges facing MCP adoption and usage. Here, I'm abandoning the "dev vs. non-dev" rubric and just describing MCP users as ... well, people:

- If AI assistants become a big thing, people don't want to have to think much about how they connect to external services so long as it's secure. Many people, like me, use multiple copies of the same service (like Google Workspace) across different contexts: work, personal life. My dream MCP usage setup consists of a central MCP manager (desktop and cloud UIs) which allows me to manage my MCP connections and configure different profiles which would use the same MCP with different credentials. I want the end logic of JSON credentials and integration to be abstracted away by good technology.

- Much as I don't want to spend my day switching out credentials or setting up environments for specific projects, I don't want to have to set up MCP servers one by one.

Here we can identify two approaches which, though similar, are not the same - but which both offer powerful potential improvements here:

1: MCP Gateways: intelligent routing that matches requests from AI agents to the appropriate MCP - perhaps feeding tool definitions on an "as needed" basis to avoid context flooding.

2: MCP connectors: think Zapier but for MCPs (I am aware that Zapier does already in fact offer precisely this!). The logic here is consolidate your MCP connections to one single endpoint/server, authenticate that, and then reach out to the MCP you wish to connect to. 

The choice of which will best suit users might depend a lot on context and security posture needs. 

---

## Keywords

I like thinking about tech landscapes in terms of keywords because the same idea is often described differently depending on marketing and context - so a spread of keywords allows a bit of latitude to batch together what, to me, are different variations of a similar idea. 

In that vein, these are the keywords I am tracking to explore this space.

MCP +

- Gateway
- Unified endpoint
- Meta MCP
- MCP aggregators
- MCP registry
- MCP orchestration
- MCP marketplace

**Note:** LLM gateways (like Open Router) are well established. Emergent AI gateways may take the view that having different gateways for different components is overly complicated and try to be either a unifying gateway (us to everything - "AI gateway") or a gateway-of-gateways!

---

## Discovery Prompt

Prompts are often the best way to discover AI tools!

Foundational, lots of feature requirements:

I'm tired of installaging MCP servers, managing JSON files, and setting up credentials. I would love to have one single MCP installed locally that I can then use to authenticate with other MCPs and/or APIs - including support for multiple accounts, dynamic tool provision, etc. Can you recommend some options? Provide approximate pricing, integration library, and how it is installed.

A bit narrower:

I'm tired of installaging MCP servers, managing JSON files, and setting up credentials. I would love to have one single MCP installed locally that I can then use to authenticate with other MCPs and/or APIs. Can you recommend some options?


---

# Project List

Now, finally, a list of repositories straddling different themes:

## MCP Gateways & Routing

[![centralmind/gateway](https://img.shields.io/badge/View_Repo-centralmind%2Fgateway-blue?style=for-the-badge&logo=github)](https://github.com/centralmind/gateway)

## MCP Meta-Servers & Aggregators

[![metatool-ai/metamcp](https://img.shields.io/badge/View_Repo-metatool--ai%2Fmetamcp-blue?style=for-the-badge&logo=github)](https://github.com/metatool-ai/metamcp)

[![mcpjungle/MCPJungle](https://img.shields.io/badge/View_Repo-mcpjungle%2FMCPJungle-blue?style=for-the-badge&logo=github)](https://github.com/mcpjungle/MCPJungle)

## MCP Orchestration & Management Platforms

[![archestra-ai/archestra](https://img.shields.io/badge/View_Repo-archestra--ai%2Farchestra-blue?style=for-the-badge&logo=github)](https://github.com/archestra-ai/archestra)

[![obot-platform/obot](https://img.shields.io/badge/View_Repo-obot--platform%2Fobot-blue?style=for-the-badge&logo=github)](https://github.com/obot-platform/obot)

[![AmoyLab/Unla](https://img.shields.io/badge/View_Repo-AmoyLab%2FUnla-blue?style=for-the-badge&logo=github)](https://github.com/AmoyLab/Unla)