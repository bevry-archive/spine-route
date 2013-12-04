
<!-- TITLE/ -->

# spine-route

<!-- /TITLE -->


<!-- BADGES/ -->

[![Build Status](http://img.shields.io/travis-ci/bevry/spine-route.png?branch=master)](http://travis-ci.org/bevry/spine-route "Check this project's build status on TravisCI")
[![NPM version](http://badge.fury.io/js/spine-route.png)](https://npmjs.org/package/spine-route "View this project on NPM")
[![Gittip donate button](http://img.shields.io/gittip/bevry.png)](https://www.gittip.com/bevry/ "Donate weekly to this project using Gittip")
[![Flattr donate button](http://img.shields.io/flattr/donate.png?color=yellow)](http://flattr.com/thing/344188/balupton-on-Flattr "Donate monthly to this project using Flattr")
[![PayPayl donate button](http://img.shields.io/paypal/donate.png?color=yellow)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=QB8GQPZAH84N6 "Donate once-off to this project using Paypal")

<!-- /BADGES -->


<!-- DESCRIPTION/ -->

The minimistic router from Spine, extracted microjs style.

<!-- /DESCRIPTION -->


<!-- INSTALL/ -->

## Install

### [Node](http://nodejs.org/), [Browserify](http://browserify.org/)
- Use: `require('spine-route')`
- Install: `npm install --save spine-route`

### [Ender](http://ender.jit.su/)
- Use: `require('spine-route')`
- Install: `ender add spine-route`

<!-- /INSTALL -->


## Usage

This is the [Routing](http://spinejs.com/docs/routing) component of the [Spine](http://spinejs.com/) MVC framework extracted into its own module, microjs style.

For complete documentation, and usage, see the [relevant spine documentation](http://spinejs.com/docs/routing).

``` coffeescript
# Define our Application
class App
	constructor: ->
		# Import the router
		Route = require('spine-route').Route

		# Bind routes to our application methods
		routes =
			'/': 'routeApp'
			'/site/:siteId/': 'routeApp'
			'/site/:siteId/:fileCollectionId': 'routeApp'
			'/site/:siteId/:fileCollectionId/*filePath': 'routeApp'
		for own key,value of routes
			Route.add(key, @[value].bind(@))

		# Start the routing
		Route.setup()

	routeApp: (opts) ->
		{siteId, fileCollectionId, filePath} = opts

# Create our application
app = new App()
```


<!-- HISTORY/ -->

## History
[Discover the change history by heading on over to the `History.md` file.](https://github.com/bevry/spine-route/blob/master/History.md#files)

<!-- /HISTORY -->


<!-- CONTRIBUTE/ -->

## Contribute

[Discover how you can contribute by heading on over to the `Contributing.md` file.](https://github.com/bevry/spine-route/blob/master/Contributing.md#files)

<!-- /CONTRIBUTE -->


<!-- BACKERS/ -->

## Backers

### Maintainers

These amazing people are maintaining this project:

- Benjamin Lupton <b@lupton.cc> (https://github.com/balupton)

### Sponsors

No sponsors yet! Will you be the first?

[![Gittip donate button](http://img.shields.io/gittip/bevry.png)](https://www.gittip.com/bevry/ "Donate weekly to this project using Gittip")
[![Flattr donate button](http://img.shields.io/flattr/donate.png?color=yellow)](http://flattr.com/thing/344188/balupton-on-Flattr "Donate monthly to this project using Flattr")
[![PayPayl donate button](http://img.shields.io/paypal/donate.png?color=yellow)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=QB8GQPZAH84N6 "Donate once-off to this project using Paypal")

### Contributors

These amazing people have contributed code to this project:

- Benjamin Lupton <b@lupton.cc> (https://github.com/balupton) - [view contributions](https://github.com/bevry/spine-route/commits?author=balupton)

[Become a contributor!](https://github.com/bevry/spine-route/blob/master/Contributing.md#files)

<!-- /BACKERS -->


<!-- LICENSE/ -->

## License

Licensed under the incredibly [permissive](http://en.wikipedia.org/wiki/Permissive_free_software_licence) [MIT license](http://creativecommons.org/licenses/MIT/)

Copyright &copy; 2013+ Bevry Pty Ltd <us@bevry.me> (http://bevry.me)

<!-- /LICENSE -->


This work is based off prior work by [Alex MacCaw](http://alexmaccaw.com/) and the [Spine](http://spinejs.com/) team, [view their license here](https://github.com/spine/spine/blob/master/LICENSE).