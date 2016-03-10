# My tech stack
This is my personal (opinionated) tech stack

Sometimes I get asked what technology stack I'm using for what and if I heard of technology X. This little readme shows what technologies I prefer and why.

## Server/Backend
*Language:* JavaScript  
*Platform:* Node.js  
*Package management:* NPM  

*Frameworks:*
* Hapi.js
* Expressjs

I like to create micro services if possible and have a Hapi.js-powered proxy that binds them all together. Usually, I go with Hapi.js when deciding to create Node.js-powered backends as it reduces the amount of boilerplate I need to write and I like the configuration-heavy approach.

## Web/Frontend
*Language:* JavaScript  
*Package management:* NPM  

*Toolchain:*
* Webpack
* Babel

I usually tend to use the `stage-1` or `stage-0` preset when using Babel depending on the feature set I need to use for protoyping. For projects I know should be production-ready soon or to be used as a base in a team environment, I only use the `es2015` preset with specific plugins, like `class-properties`, `export-extensions` and object rest spread.
Webpack I found to be a great bundler for web apps, it takes care of all my assets (not just my JavaScript) and it provides very detailed configuration and optimization options. I gradually start from a simple setup and then move on to using code splitting and similar feature when I need them.
For libraries I usually go with Rollup as I want my libraries to be as small as possible and I don't mind all of my JS files being in the same scope in the resulting file.

*Frameworks:*
* ReactJS ([My opinion on ReactJS](https://medium.com/front-end-hacking/my-probably-entirely-subjective-reactjs-impressions-430eca0b9255#.mam94de78))

## Mobile
*Language:* JavaScript  
*Package management:* NPM  

*Frameworks:*
* React Native

I am a big fan of React Native and have used it for apps that are currently in the App Store. React Native for me has all the advantages of JavaScript in a mobile platform:
- Interfaces with native controls
- Declarative UI (The React part of React Native)
- Multiple threads

## Databases
- RethinkDB
- CouchDB

RethinkDB is my database of choice, because it's fully JSON-compliant, has a modern admin interface, a JavaScript playground on the admin interface, powerful queries and real-time support being built-in (and it doesn't feel like a hack). My second choice is CouchDB, mostly because I worked with it for almost three years, but it falls short compared to RethinkDB in terms of querying and real-time support.

## Games
That depends on the platform I'm targeting. But additionally to the technologies mentioned so far, these technologies may also be under consideration:
- Unity3D (C#)
- Haxe + OpenFL
- One of my own many game engines

The decision depends on the requirements of the game. For 3D and heavily physics based games I tend to go with Unity3D.

## JavaScript
Since JavaScript is a big part of this list, I'd like to go deeper with some of the beliefs.

*Modularity:* I'm a big believer in keeping everything as modular as possible
*Control flow:* Promises (ES6 promise)
*AJAX:* fetch (with or without polyfill)
*Task runner:* NPM scripts most of the time, I have used Grunt extensively in the past. When the scripts tend to go out of control, I turn back to Grunt for a specific project.

### Linting & Testing
#### Linting
* ESLint with AirBnB preset

I feel the AirBnB preset is the closest to my personal preference and while I don't agree on some minor points in their guideline, I think it's a very good base for linting (especially for React projects).

#### Testing
If I need tests on the server-side, I go with AVA, as it allows me to write tests in ES2015 and has a clearer and more concise API than my other go-to test framework Mocha.

* Mocha (Test runner)
* Chai (Assertion library)
* Karma (For client-side tests I always go with Karma. I have lived through setting up automated client testing with JavaScript and I happily choose Karma, even though it may sometimes be unpredictable if specific runners or plugins don't work well with one another. Debugging Karma configurations is something I struggle with.)

### Communication
* Slack
* Github Issues

I prefer asynchronous communication. Github issues is where I formulate my ideas for discussion and create task issues out of those. I like to do "umbrella" tasks which group certain issues for a specific milestone, release or task group.

### Development workflow
* Github Flow
* ZenHub

I have used Trello before and I found it to be way too liberal. With Trello I felt there was the need for someone to organize the boards and enforce certain standards on how the boards should be used. Where Trello worked really well for me was couple of days or single-week projects.

### Local development workflow
* Vagrant



### Deployment workflow
* Docker

I am still in the phase of figuring things out with Docker, so as much as I want to go deep into the technology, I'm currently only dipping my toes into that.

For most apps I build, I use a separate deployment branch with contains the deployable and can be run out-of-the-box on the target server. This branch will be build on a CI

### Continous integration
* Travis CI
* Jenkins
* CircleCI

For open-source projects, I always use Travis CI. For closed-source projects, I base the decision of Jenkins vs. CircleCI on the need of a self-hosted solution, costs and the effort I need to put in into the configuration of Jenkins.

### Hosting platform
* AWS
* DigitalOcean
* Github Pages

When I need a complete server where I may need to tinker around or have complete control, I go for DigitalOcean or AWS with a preference for AWS. It took me some time to get into AWS, but nowadays I feel confident to configure load balancers, servers and domains in AWS for smaller to mid-sized projects. For static sites, I typically use Github pages, especially when the repository is already on Github. I want to take a look at surge.sh, but haven't had a chance to do so yet.


### Stuff I'm keeping my eye on
* Gitlab + Gitlab CI (I have used Gitlab at a company before and I found it most pleasant to work with, but I can't see myself switching to Gitlab just yet. Github is just too convenient at the moment. I'm really interested to see how the CI integration will progress and the Mattermost integration may be promising)
* Tutum.co
* `async`-`await`: I haven't had a chance to use it in a production environment yet, but I really want to
