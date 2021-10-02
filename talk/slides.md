---
marp: true
title: Surface: A bridge to the Javascript community
description: Talk for ElixirConf 2021
footer: Surface — @davydog187
theme: uncover
paginate: true
_paginate: false
---

# Surface: A bridge to the Javascript community

---
# Who am I - Dave Lucia
- VP, Engineering at Simplebet :basketball: :baseball: :football:
- Elixirin' since 2016 :muscle:

---
# Coming to Elixir

<!--
* While many come to Elixir from Ruby, I came from Javascript 
* have a memory of what it was like living in the Node.js ecosystem
-->

---
# Javascript in the Browser - Early 2010s
* JQuery
* Backbone.js
* Angular

---
# Javascript in the Browser - Mid 2010s
* React / Vue
* Elm
* Svelte

<!-- Maybe even mention Bloomberg Brisket for fun -->

---
# BLV - Before Live View
* Server-rendered HTML :muscle:
* React & Vue.js 

<!--
Describe building apps before live view. Usually using sockets/channels + some Javascript framework.

Possibly React/Vue or even Elm
<!---->
---

# BLV - A lot of people still build apps this way
* Great for many usecases
* If you have a frontend heavy app, this may still be your goto route
---

# Announcment of LiveView
* Fundamentally changed the way that interactive web applications could be built
---

# Write once, use everywhere
---

# Challenges of building JS apps
---

# Managing state on both frontend and backend
* Redux
* Mobx
* Hooks
* Elm architecture
* ???

---
# Managing the toolchains

<!-- Insert meme about node_modules -->

---
# Testing two codebases
<!-- 
Now you have to test your Javascript code too to prevent regressions. Maybe you pull in Wallaby and do browser-based integration testing, but regardless, at a certain level of complexity, you're thinking about writing two fundamentally different classes of tests for your frotneds
-->
  
---
# LiveView cut out all of the crap
* Unlocked a new pathway for quickly building many classes of applications
* Changed the way that we write internal tools at Simplebet
* Throw some stuff in a Phoenix LiveView + PubSub, now you've got a Live, interfactive web Page
* Holy shit is it powerful

---
# At Simplebet, LiveView has changed the way we build our operational tools. :shh: it's our secret weapon

---
# I started craving something out of LiveView
* Somethign that I've seen before...
* What I experienced working within the Javascript community for so long

---
# A new project emerges

* In Spring of 2021, we had an ambitious, greenfield project
* I knew we could do it in LiveView, but LiveView was missing some of the things I really wanted

---
# What LiveView was missing
* Truly reusable components
* Static prop annotations
* Compile-time checks to enforce valid HTML

---
# Enter Surface
* Remember hearing about Surface, but never understood what value it was bringing over LiveView
* Clearly, I was missing a lot

---
# Surface enhances LiveView by taking a decade+ worth of learnings from the Javascript community

---
# Let's compare Surface to the latest and greatest Javascript frameworks

---
# Compile-time HTML validations
<!-- Compare JSX, and whatever Vue uses, maybe Svelte -->

---
# Template specific DSLs that is tailored to the domain

---
# Ok, but we just got HEEX!

---
# HEEX vs Surface templates
* heex only went halfway
* It's a great improvement over just string interpolation
* Introduces structured data into the templates
* Missing many of the fundamental improvments

---
# Surface++ - Conditional classes

---
# Surface++ - Slots

---
# Surface++ - Dynamic Components

---
# Surface++ - Declaritive props and data
* React now recommends Flow/Typescript to introduce types
* Before this they had a concept of `PropTypes` for annotating props
* Surface offers something in the middle

---
# Surface++ - Self-Documenting via Surface Catalogue

---
# Surface++ - Examples and Playground

---
# Surface++ - Community Component Libraries
* DaisyUI
* UIKit
* Bulma
* Bootstrap

---
# Surface++ - Investment in tooling
* `mix surface.format`
* `mix surface.convert`
---

# Surface++ - Bootstrapping a project
<!-- Show of Marlus's new work of using Sourceror to bootstrap
a Surface project
-->

---
# Surface - What lies ahead?
* Further enhancements to template language
  * Computed properties
  * TKTKTK ask Marlus - That thing from Adobe flex?
* Visual Regression Testing

---
# Why Surface is important
* Bringing back its best ideas back to LiveView
* Testing ground for new ideas
* Can make optimizations, tools, and langugage features that LiveView can't offer
---
# But it comes back to the community

---
# Let's usher in a new era of Elixir developers
* LiveView + Surface can attract Javascript developers who are looking for more

---
# What LiveView + Surface can offer Javascript developers
* Stability (in the API sense)
* Reliability
* Scale

---
# Thank you
