# Motivation

Reacted is a fully [isomorphic JS][airbnb-isomorphic] framework built on top of React, Flux and Webpack that aims to be productive, performant, robust and flexible. 

### Productive
 - No more server-side templates to have sever-side generated Html: just [React][react] components that render both on the server and the client.
 - No more hard to reason / debug evented codebase: uses [Flux][flux-video] unidirectional data flow to make your app predictible.
 - Stop rewriting the wheels over and over: just easily compose your own or [open source][react-component-com] React components thanks to their tight and well-defined Api.
 - [Super fast][webpack-build-performance] [hot reload][webpack-reload] of your entire stack, including your [React components][react-reload], your [css and more][webpack-loaders].

### Fast
 - Instantaneous page render feel: [Html is initially rendered][webpack-server-side] on the server with just the [necessary inlined css][webpack-style-collector]. Shared assets are then fetched asynchronously in the background. Subsequent pages load data, JS and css as needed.
 - Fast DOM manipulation: [React's virtual DOM][react-virtual-dom] minimize slow and costly DOM manipulation
 - Out-of-the-box [assets optimizations][webpack-optimization]: compilation, concatenation, minification, module splitting, caching, remove code behind feature flag etc...
 - SPDY support: the Reactd server offers [Spdy resources hint and push][igvita-spdy]. It fallbacks to [head flushing][first-byte-flush] to trigger asset fetching as soon as possible

### Robust
 - [CommonJS][node-module] module dependency makes your code run on Node and in [a browser][webpack-commonjs]. Your code is more explicit and easier to isolate for testing 
 - Testing React with [Jest][jest] is easy thanks to [auto-mocking][jest-automock] and fast (no PhantomJS): don't let your front-end grow out of control.
 - Out-of-the box [code linting][webpack-jshint]: JS should never make it to production without being linted
 - [Easy Integration][flow-loader] [with flow][flowtype] so you can make your JS safer when you start feeling the pain of untyped JS


### Flexible
 - Completely Back end agnostic: the Reactd [Express server][express-com] is responsible for building and serving your assets and generating your Html page so your API can focus on serving data, not assets.
 - Build step produces an assets directory and a manifest file so you can easily deploy and reference your assets in your backend.
 - The Reactd server is Docker containerized so you can run, build and deploy anywhere


# Todo

Explain architecture and how it fits in current stack
List problems that need to be solved to a fully isomorphic app
For each problem, write about the different solutions 


# License

Copyright (c) 2014 Julien Nakache

MIT (http://www.opensource.org/licenses/mit-license.php)

[airbnb-isomorphic]:http://nerds.airbnb.com/isomorphic-javascript-future-web-apps/
[react]:http://facebook.github.io/react/
[flux]:https://facebook.github.io/flux/
[flux-video]:https://www.youtube.com/watch?v=nYkdrAPrdcw&list=PLb0IAmt7-GS188xDYE-u1ShQmFFGbrk0v#t=621
[webpack-reload]:http://webpack.github.io/docs/hot-module-replacement.html
[webpack-build-performance]:http://webpack.github.io/docs/build-performance.html
[react-reload]:http://gaearon.github.io/react-hot-loader/2014/07/23/integrating-jsx-live-reload-into-your-react-workflow/
[webpack-loaders]:http://webpack.github.io/docs/list-of-loaders.html
[react-virtual-dom]:http://facebook.github.io/react/docs/working-with-the-browser.html#the-virtual-dom
[webpack-style-collector]:https://github.com/webpack/react-webpack-server-side-example/blob/master/server/style-collector.js
[webpack-server-side]:https://github.com/webpack/react-webpack-server-side-example
[webpack-optimization]:http://webpack.github.io/docs/optimization.html
[igvita-spdy]:https://www.igvita.com/2013/06/12/innovating-with-http-2.0-server-push/
[first-byte-flush]:https://plus.google.com/+IlyaGrigorik/posts/GTWYbYWP6xP
[react-component-com]:http://react-components.com/
[node-module]:http://nodejs.org/api/modules.html
[webpack-commonjs]:http://webpack.github.io/docs/commonjs.html
[jest]:https://facebook.github.io/jest/
[jest-automock]:https://facebook.github.io/jest/docs/automatic-mocking.html#content
[webpack-jshint]:https://github.com/webpack/jshint-loader
[flowtype]:http://flowtype.org/
[flow-loader]:https://github.com/facebook/flow/issues/5
[express-com]:http://expressjs.com/