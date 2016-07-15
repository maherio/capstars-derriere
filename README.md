# CapStars Derriere

[![Build Status](https://travis-ci.org/maherio/capstars-derriere.svg?branch=master)](https://travis-ci.org/maherio/capstars-derriere)

CapStars Derriere (get it? Because it's the backend) is a RESTful API which provides the complete data store for CapStars dynasty leagues, sports, players, etc.

Requirements:

Provide a RESTful API which returns the following data in JSON format

* A list of sports, as well as an individual sport
	* A sport consists of an identifier and a public name.
* A list of players for a given sport, as well as an individual player
	* A player consists of a first name, last name, position, height and weight attributes, and bio.


Notes:

* For now, I'm just stubbing out the player info b/c I'm not sure what I'll need to do to for a data store. Hopefully I can just ping an NFL or ESPN api, but I'm guessing that will be too costly for a side project and I'll have to either scrape (is that legal?) or maintain myself (ugh no). Either way, I want this to be flexible to change, so I want to abstract and encapsulate the data store as much as possible.
* I also wanted to try more hypermedia controls in the API, as I've never seen an API do that well. It'll be much more chatty this way, but there are ways around that and lots of tech and tools are better than ever at handling it.
* For now, I'm undecided whether or not I want authentication. On the one hand, this is a simple exercise that I don't want too complex to start. On the other, I do want to play more with Stormpath and think API auth is something that should be built in early.
