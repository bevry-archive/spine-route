
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

- abernier (https://github.com/abernier) - [view contributions](https://github.com/bevry/spine-route/commits?author=abernier)
- adambiggs (https://github.com/adambiggs) - [view contributions](https://github.com/bevry/spine-route/commits?author=adambiggs)
- aeischeid (https://github.com/aeischeid) - [view contributions](https://github.com/bevry/spine-route/commits?author=aeischeid)
- amaierhofer (https://github.com/amaierhofer) - [view contributions](https://github.com/bevry/spine-route/commits?author=amaierhofer)
- cengebretson (https://github.com/cengebretson) - [view contributions](https://github.com/bevry/spine-route/commits?author=cengebretson)
- chetan51 (https://github.com/chetan51) - [view contributions](https://github.com/bevry/spine-route/commits?author=chetan51)
- csaunders (https://github.com/csaunders) - [view contributions](https://github.com/bevry/spine-route/commits?author=csaunders)
- cweezy (https://github.com/cweezy) - [view contributions](https://github.com/bevry/spine-route/commits?author=cweezy)
- dnalot (https://github.com/dnalot) - [view contributions](https://github.com/bevry/spine-route/commits?author=dnalot)
- eigenein (https://github.com/eigenein) - [view contributions](https://github.com/bevry/spine-route/commits?author=eigenein)
- ewoutkleinsmann (https://github.com/ewoutkleinsmann) - [view contributions](https://github.com/bevry/spine-route/commits?author=ewoutkleinsmann)
- faiizow (https://github.com/faiizow) - [view contributions](https://github.com/bevry/spine-route/commits?author=faiizow)
- gsamokovarov (https://github.com/gsamokovarov) - [view contributions](https://github.com/bevry/spine-route/commits?author=gsamokovarov)
- hecticjeff (https://github.com/hecticjeff) - [view contributions](https://github.com/bevry/spine-route/commits?author=hecticjeff)
- impressiver (https://github.com/impressiver) - [view contributions](https://github.com/bevry/spine-route/commits?author=impressiver)
- jackjennings (https://github.com/jackjennings) - [view contributions](https://github.com/bevry/spine-route/commits?author=jackjennings)
- jcarlson (https://github.com/jcarlson) - [view contributions](https://github.com/bevry/spine-route/commits?author=jcarlson)
- jeremyhaile (https://github.com/jeremyhaile) - [view contributions](https://github.com/bevry/spine-route/commits?author=jeremyhaile)
- joefiorini (https://github.com/joefiorini) - [view contributions](https://github.com/bevry/spine-route/commits?author=joefiorini)
- joelvh (https://github.com/joelvh) - [view contributions](https://github.com/bevry/spine-route/commits?author=joelvh)
- johanlunds (https://github.com/johanlunds) - [view contributions](https://github.com/bevry/spine-route/commits?author=johanlunds)
- jonstorer (https://github.com/jonstorer) - [view contributions](https://github.com/bevry/spine-route/commits?author=jonstorer)
- jtharris (https://github.com/jtharris) - [view contributions](https://github.com/bevry/spine-route/commits?author=jtharris)
- KevBurnsJr (https://github.com/KevBurnsJr) - [view contributions](https://github.com/bevry/spine-route/commits?author=KevBurnsJr)
- kossnocorp (https://github.com/kossnocorp) - [view contributions](https://github.com/bevry/spine-route/commits?author=kossnocorp)
- lorensr (https://github.com/lorensr) - [view contributions](https://github.com/bevry/spine-route/commits?author=lorensr)
- lyleunderwood (https://github.com/lyleunderwood) - [view contributions](https://github.com/bevry/spine-route/commits?author=lyleunderwood)
- maca (https://github.com/maca) - [view contributions](https://github.com/bevry/spine-route/commits?author=maca)
- maccman (https://github.com/maccman) - [view contributions](https://github.com/bevry/spine-route/commits?author=maccman)
- martydill (https://github.com/martydill) - [view contributions](https://github.com/bevry/spine-route/commits?author=martydill)
- mbleigh (https://github.com/mbleigh) - [view contributions](https://github.com/bevry/spine-route/commits?author=mbleigh)
- metaskills (https://github.com/metaskills) - [view contributions](https://github.com/bevry/spine-route/commits?author=metaskills)
- mitchlloyd (https://github.com/mitchlloyd) - [view contributions](https://github.com/bevry/spine-route/commits?author=mitchlloyd)
- nathanpalmer (https://github.com/nathanpalmer) - [view contributions](https://github.com/bevry/spine-route/commits?author=nathanpalmer)
- navitmccaffery (https://github.com/navitmccaffery) - [view contributions](https://github.com/bevry/spine-route/commits?author=navitmccaffery)
- noTxt (https://github.com/noTxt) - [view contributions](https://github.com/bevry/spine-route/commits?author=noTxt)
- nrw (https://github.com/nrw) - [view contributions](https://github.com/bevry/spine-route/commits?author=nrw)
- paulyoung (https://github.com/paulyoung) - [view contributions](https://github.com/bevry/spine-route/commits?author=paulyoung)
- pitr (https://github.com/pitr) - [view contributions](https://github.com/bevry/spine-route/commits?author=pitr)
- pyykkis (https://github.com/pyykkis) - [view contributions](https://github.com/bevry/spine-route/commits?author=pyykkis)
- rlaneve (https://github.com/rlaneve) - [view contributions](https://github.com/bevry/spine-route/commits?author=rlaneve)
- rodrigorm (https://github.com/rodrigorm) - [view contributions](https://github.com/bevry/spine-route/commits?author=rodrigorm)
- scottburton11 (https://github.com/scottburton11) - [view contributions](https://github.com/bevry/spine-route/commits?author=scottburton11)
- shiftb (https://github.com/shiftb) - [view contributions](https://github.com/bevry/spine-route/commits?author=shiftb)
- sishen (https://github.com/sishen) - [view contributions](https://github.com/bevry/spine-route/commits?author=sishen)
- sjoerdmulder (https://github.com/sjoerdmulder) - [view contributions](https://github.com/bevry/spine-route/commits?author=sjoerdmulder)
- SlexAxton (https://github.com/SlexAxton) - [view contributions](https://github.com/bevry/spine-route/commits?author=SlexAxton)
- snichme (https://github.com/snichme) - [view contributions](https://github.com/bevry/spine-route/commits?author=snichme)
- SpeCT (https://github.com/SpeCT) - [view contributions](https://github.com/bevry/spine-route/commits?author=SpeCT)
- suprMax (https://github.com/suprMax) - [view contributions](https://github.com/bevry/spine-route/commits?author=suprMax)
- teamtreehouse (https://github.com/teamtreehouse) - [view contributions](https://github.com/bevry/spine-route/commits?author=teamtreehouse)
- timoxley (https://github.com/timoxley) - [view contributions](https://github.com/bevry/spine-route/commits?author=timoxley)
- umate (https://github.com/umate) - [view contributions](https://github.com/bevry/spine-route/commits?author=umate)
- vkill (https://github.com/vkill) - [view contributions](https://github.com/bevry/spine-route/commits?author=vkill)
- vojto (https://github.com/vojto) - [view contributions](https://github.com/bevry/spine-route/commits?author=vojto)
- yaakaito (https://github.com/yaakaito) - [view contributions](https://github.com/bevry/spine-route/commits?author=yaakaito)

[Become a contributor!](https://github.com/bevry/spine-route/blob/master/Contributing.md#files)

<!-- /BACKERS -->


<!-- LICENSE/ -->

## License

Licensed under the incredibly [permissive](http://en.wikipedia.org/wiki/Permissive_free_software_licence) [MIT license](http://creativecommons.org/licenses/MIT/)

Copyright &copy; 2013+ Bevry Pty Ltd <us@bevry.me> (http://bevry.me)

<!-- /LICENSE -->


This work is based off prior work by [Alex MacCaw](http://alexmaccaw.com/) and the [Spine](http://spinejs.com/) team, [view their license here](https://github.com/spine/spine/blob/master/LICENSE).