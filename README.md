# CapStars Derriere

[![Build Status](https://travis-ci.org/maherio/capstars-derriere.svg?branch=master)](https://travis-ci.org/maherio/capstars-derriere)

CapStars Derriere is the RESTful API backend which provides the complete data store for CapStars dynasty leagues, sports, players, etc.

Requirements:

Provide a RESTful API which returns the following data in JSON format

* Sport resource and collection (GET)
	* A sport consists of at least a public name.
* Position resource and collection (GET)
	* A position belongs to a Sport and consists of a name and abbreviation.
* Player resource and collection (GET)
	* A player has a Position and consists of at least a first name, and last name.
* League resource and collection (GET, PUT/POST, DELETE)
	* A league belongs to a Sport, has a commissioner (User) and consists of a name.
* League Settings collection (GET, PUT/POST)
	* Settings that belong to a League, and will include things like roster position, scoring settings, password, salary cap, etc.
* Roster resource and collection (GET, PUT/POST, DELETE)
	* A roster belongs to a League and an owner (User), has Players and DraftPicks, and consists of a name, salary (total of signed players), penalty (total of cut players), etc.
* Contract resource and collection (GET, PUT/POST, DELETE)
	* A contract belongs to a Roster, has a Player, and consists of start date, end date, release date, and an amount for each year.
* Stat resource and collection
	* A stat belongs to a Player and consists of a metric, a value, and a date.

Current Functionality:
* None. Just getting a fresh lumen app up and running.

Notes:

* For now, I'm just stubbing out the player info b/c I'm not sure what I'll need to do to for a data store. Hopefully I can just ping an NFL or ESPN api, but I'm guessing that will be too costly for a side project and I'll have to either scrape (is that legal?) or maintain myself (ugh no). Either way, I want this to be flexible to change, so I want to abstract and encapsulate the data store as much as possible.
* I also wanted to try more hypermedia controls in the API, as I've never seen an API do that well. It'll be much more chatty this way, but there are ways around that and lots of tech and tools are better than ever at handling it.
* For now, I'm undecided whether or not I want authentication. On the one hand, this is a simple exercise that I don't want too complex to start. On the other, I do want to play more with Stormpath and think API auth is something that should be built in early.
