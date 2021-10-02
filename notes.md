# Notes

## What do you like about Surface?
- Surface moves runtime complexity to 


## Chat with Marlus

- Minimizes the dependencies vs JS
- DSL for writing components
    - Surface is in the middle of React vs Vue.js
    - React is extremely verbose compared to vue/svelte
    - JSX is built on top of JS, no syntactic sugar
    - eex tries to bring Elixir into the template language, which is complicated
    - Surface is best of both worlds because it gives the flexibility to extend the language independent of elixir, but the freerdom to explore and bring better ergonomics to the domain
    - heex can never do this because it has to be compatible with elixir because chris decided to not have the limited DSL
- Explore the syntactic sugar of Surface vs others
    - tagged for loops
    - tagged expressions `...` `=` `^` `~`
- Creating a language that is better for the domain
- Get excitement before ElixirConf
    - Create a suite of Tailwind components to get started
    - Generators for Surface
        - Instead of creating templates by using the phoenix generated files and changing the generated file
        - Use sourcerer to rewrite the generated files
            - Look at the `surface.convert` behavior which uses sourcerer for an example
    - `mix [surface.new](http://surface.new)` like create react app, single file that you can create a small surface project with

    [https://twitter.com/mcrumm/status/1431812684345798661?s=21](https://twitter.com/mcrumm/status/1431812684345798661?s=21)


## Brain dump
* LiveView
  * Changed the way I built web applications
  * Made it really easy to get a dynamci web-page up and running
* Javascript 
  * Building apps with React/Preact.js
    * Introduces a small syntax sugar to Javascript called "JSX" that desugars to a function call `create_element(blah)`
    * Spent a lot of time building the content management system of The Outline using React and Preact.js
    * A good majority of the time that I spent on building Javascript apps was syncing the data model between the front-end and the backend
    * Introducing layers like Mobx, Redux, or Hooks into your application adds a lot of complexity
    * Building out the websocket/http APIs for you frontend to communicate with is very time consuming 
      * GraphQL is proposed as a solution here but is also extremely time consuming to build, maintain, etc
  * Vue.js
    * Solves the render(state) -> html problem in a slightly different way using a DSL inside of markup rather than extending
    * Came up around the same time as React, also takes the approach of having a virtual dom and stateless rendering
  * Svelte.js comes from Rich Harris at the NYTimes
    * Was an experiment to see if much of the runtime complexity of the virtual dom could be offloaded to a compilation phase by building a compiler of sorts
    * Has introduced a lot of interesting ideas into the Javascript community around what is possible
* Coming back to LiveView
* Cool shit
  * The Surface Component Catalaogue is a killer feature. Storybook.js Anyone? implement style guides
  * Surface template DSL makes your life better not harder
    * "Why do I have to learn another language?" - Devon
      * We can optimize the output of the DSL
      * We can offer control flow that doesnt' exist in elixir but is good for template (for/else)
    * Component props and data
      * React has this with some little extra library, its called props something something
      * Defining default values and prop validation is powerful
      * You get compile and runtime warnings if you pass invalid props!
  * Investment in tooling
    * Surface convert for upgrading between Surface versions is insanely cool
    * Surface init for bootstrapping Surface inside a Phoenix project
      * This is could be a talk in and of itself
      * Uses Sourceror to parse the source code of your project, understands the semantics of your code, conditionally applies patches to your code
        * If it fails, it gives you helpful warning messages for why it was unable to apply the patch. How fucking cool is that?
    * Surface Catalaogue
  * Community Components
    * DaisyUI
    * UIKit
    * Bulma
    * bootstrap
* The connection between Surface and the Javascript community
  * Evolution of frontend frameworks of the last 10+ years
    * Reminiscing about the early days of the web where people would build webpages with funky javascript snippets on them
      * One that comes to my mind is the trailing text that would float around your cursor, like a text clock
    * JQuery/MooTools -> Backbone.js -> Angular / Emeber -> Vue.js / React.js -> Svelte.js
    * These frameworks spent a lot of time experimenting in various layers of the frontend stack
    * Applying abstractions over the years to solve different problems
    * Led to some convergent patterns like virtual dom or even compile time virtual domain
* Surface vs LiveView
  * Surface is pushing the ergonomics, tooling, and features of LiveView by learning from the decade+ years of experiments, hard-earned lessons, and convergence that the JavaScript community has already pushed through
    * Reusable Components!
    * HEex
    * Slots
    * Template specific DSL
    * Styleguide / Component catalogue
  * Surface's goal is to continue to iterate towards the best tooling from the JS commiunity
    * Future ideas
      * Visual Regression testing
      * Computed properties
      * Thing from Adobe Flex that Marlus mentioned
      * Component libraries for popular design frameworks, ala Tailwind via DaisyUI, etc
      * Continuing to enhance compile-time validations, checks, optimizations
  * The long-term success of Surface is important to provide optionality to the LiveView community, in the same way that React, Vue, ember, angular, etc provide optionality for developers 
  * Break out of the monoculture!
      

## Examples for Talk
It would be nice to have a working example for my talk that I can use to drive some of these points home

Random ideas
* Baby tracker that counts the number of bottles, diapers, formula, toys and keeps stats
* Sports thing that mimics sports betting in some way
  * Two teams are created, you get to place a bet, keeps track of your bets
* Build a twitter clone or something? Its ripping off of Chris's talk about LiveView, but maybe it provides some familiarity to the audience?
* Animals are always a good thing to fall back on
  * Maybe a food tracker for dogs and cats, provides a place where you need to make decisions based on the type of animal which may be helpful for illustrating template decisions
        
       
     
## The points I want to hit in this talk
* While many come to Elixir from Ruby, I came from Javascript and have a memory of what it was like living in the Node.js ecosystem
* LiveView has changed the way I think about building internal tools
  * We've had a lot of success with "Developer UI" tools that can be stood up quickly and just work :TM:
  * We can continue to build across Elixir and Phoenix versions without churn. Stability :muscle:
* LiveView has been a game-changer, but I've still felt myself missing something from those Javascript years
* While I don't miss primarily working in Javascript (cue the Node Modules black hole meme), I do miss the patterns from React for defining and composing components
  * But LiveView has components Dave!
  * And they're getting even better in Phoenix LiveView 1.6!
