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

I like to create micro services if possible

## Web/Frontend
*Language:* JavaScript  
*Package management:* NPM  

*Toolchain:*
* Webpack
* Babel

I usually tend to use the `stage-1` or `stage-0` preset when using Babel depending on the feature set I need to use.

*Frameworks:*
* ReactJS (My opinion on ReactJS)

## Mobile
*Language:* JavaScript  
*Package management:* NPM  

*Frameworks:*
* React Native

I am a big fan of React Native and have used it for apps that are currently in the App Store.

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
*Task runner:* NPM scripts most of the time, I have used Grunt extensively in the past. When the scripts go out of control, I turn back to Grunt.

### Linting & Testing
#### Linting
* ESLint with AirBnB preset

#### Testing
* Mocha (Test runner)
* Chai (Assertion library)
* Karma

### Communication
* Slack
* Github Issues

I prefer asynchronous communication. Github issues is where I formulate my ideas for discussion and create task issues out of those.

### Development workflow
* Github Flow
* ZenHub

I have used Trello before and I found it to be too liberal.

### Local development workflow
* Vagrant



### Deployment workflow
* Docker

I am still in the phase of figuring things out with Docker, so as much as I want to go deep into the technology, I currently dipped my toes into that.

### Continous integration
* Travis CI
* Jenkins
* CircleCI

For open-source projects, I always use Travis CI. For closed-source projects, I base the decision of Jenkins vs. CircleCI on the need of a self-hosted solution, costs and the effort I need to put in into the configuration of Jenkins.

### Hosting platform
* DigitalOcean
* Heroku
* Github Pages

When I need a complete server where I may need to tinker around or have complete control, I go for DigitalOcean.  When I have something small or a prototype, I might use Heroku instead as it's super simple for deployments. For static sites, I typically use Github pages, especially when the repository is already on Github. I want to take a look at surge.sh, but haven't had a chance to do so yet.


### Stuff I'm keeping my eye on
* Gitlab + Gitlab CI (I have used Gitlab at a company before and I found it most pleasant to work with, but I can't see myself switching to Gitlab just yet. Github is just too convenient at the moment. I'm really interested to see how the CI integration will progress and the Mattermost integration may be promising)
* Tutum.co
* Ava (This looks like a very promising test runner to me. There are a few things that stop me from using it on a regular base: Babel 6 support, Browser support, Karma support)
* `async`-`await`: I haven't had a chance to use it in a production environment yet, but I do want to
