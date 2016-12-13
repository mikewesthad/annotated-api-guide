# Annotated List of Web APIs

This is an annotated list of Web APIs that are great for learning and experimenting in JavaScript. The APIs are broken down into three categories:

<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:1 -->

1. [APIs that are completely public](#apis-that-are-completely-public)
2. [APIs that require an API key but do not private credentials](#apis-that-require-an-api-key-but-do-not-private-credentials)
3. [APIs that require server-side programming for authorization](#apis-that-require-server-side-programming-for-authorization)

<!-- /TOC -->

This list is a collection of APIs I've used along with many pulled from afeld's [gist](https://gist.github.com/afeld/4952991). This is a work-in-progress. To do:

-   Make a note about which APIs use HTTP and which use HTTPS
-   Add a section on proxying HTTPS
-   Add a section on CORS proxys like <http://cors-anywhere.herokuapp.com/> or <http://crossorigin.me/>
-   Add some sample code for how to get JSON and JSONP
-   Finish integrating other mega-lists of APIs and annotating them

## APIs that are completely public

No API key is necessary or there is a public API key that is freely available. These are great for quick testing and learning about APIs.

-   [Giphy](https://github.com/Giphy/GiphyAPI)
    -   Access to GIFs from Giphy
    -   Requires a key, but there is a public key available for experimentation & development
    -   Returns JSON
-   [Hipsterjesus](http://hipsterjesus.com/)
    -   Hipster ipsum generator
    -   Returns JSON
-   [The Open Movie Database](http://www.omdbapi.com/)
    -   Get info about movies and TV shows including rotten tomatoes rating and plot summary
    -   Returns JSON
-   [jService](http://jservice.io/)
    -   Collection of trivia questions aired on Jeopardy
    -   Returns JSON
-   [Pokéapi](http://pokeapi.co/)
    -   Pokedex API
    -   Daily rate limit of 300 requests per resource per IP address
    -   Returns JSON
-   [Discogs API](https://www.discogs.com/developers/#)
    -   Get info about artists, releases, labels, etc.
    -   240 requests per minute per IP address without authorization
    -   Some resources (like the search endpoint) require a [authentication](https://www.discogs.com/developers/#page:authentication). You can sign up and use a user token as an easy way to access those resources (e.g. adding `&token=YOURTOKEN` to the URL).
    -   Returns JSON
-   [The Cat API](http://thecatapi.com/) (more complete access with API key)
    -   Free access to `/api/images/get` endpoint without an API key
    -   Does not support JSON/JSONP yet, but can return an HTML image tag
-   [COLOURlovers](http://www.colourlovers.com/api)
    -   Get colors/palettes
    -   Default format is xml, so add `format=json` for data in JSON format
    -   Requires JSONP with a key of `jsonCallback`
-   [Robothash](https://robohash.org/) (pass in anything after the URL to get a robot image)
    -   Turn a URL into a robot image
    -   Returns an image, so create an `img` with src pointing to the URL
-   [Dronestre.am](http://dronestre.am/)
    -   Database of US drone strikes
    -   Requires JSONP
-   [TVMaze API](http://www.tvmaze.com/api)
-   [US Earthquakes](http://earthquake.usgs.gov/fdsnws/event/1/)
-   [International Space Station (ISS) Location](http://open-notify.org/Open-Notify-API/)
-   [Sunrise sunset times](http://sunrise-sunset.org/api)
-   [Fuck Off As A Service (FOAAS)](https://www.foaas.com/)
-   [Netflix Roulette](http://netflixroulette.net/api/)
-   [NFLArrest API](http://nflarrest.com/api/)

## APIs that require an API key but do not private credentials

These APIs require you to register to get an API key, which then you use in your API requests. None of these APIs require server-side techniques to get access.

These are great for experimenting and learning, but if you are creating a final product (art installation, web app, etc.), you probably don't want your API key to be easily accessible in a public website. If someone reads your source code, they could get your API key and use up your allotted API calls.

-   [Flickr](http://www.flickr.com/services/api/) (images)
-   Google
    -   [Google Knowledge Graph](https://developers.google.com/knowledge-graph/) (information)
    -   [Google Maps](https://developers.google.com/maps/documentation/javascript/tutorial)
    -   [Google Plus](https://developers.google.com/+/api/) (people)
    -   [Youtube](https://developers.google.com/youtube/)
-   [Bing Maps](http://msdn.microsoft.com/en-us/library/dd877180.aspx)
-   [Facebook Graph API](https://developers.facebook.com/docs/reference/api/) ([JS SDK](https://developers.facebook.com/docs/reference/javascript/) allows auth via client-side)
-   [Foursquare](https://developer.foursquare.com) (location)
-   [Etsy](http://www.etsy.com/developers/documentation/getting_started/jsonp) (shopping)
-   [GitHub](http://developer.github.com/) (code)
-   [Gravatar](http://en.gravatar.com/site/implement/)
-   [Lob](https://www.lob.com/docs#verify) (mailing address verification)
-   [Mapbox](https://www.mapbox.com/developers/) (maps)
-   Mapzen [plugins](https://mapzen.com/projects/) and [data](https://mapzen.com/data/) (maps)
-   [Markit On Demand](http://dev.markitondemand.com/MODApis/) (stocks)
-   [Meetup](http://www.meetup.com/meetup_api/)
-   [Metropolitan Museum of Art](http://scrapi.org/)
-   [OpenStreetMap](http://wiki.openstreetmap.org/wiki/Develop) (maps)
-   [OpenTok](http://www.tokbox.com/opentok/api/features) (videochat)
-   [Pearson](http://developer.pearson.com/apis) (publications)
-   [Reddit](http://www.reddit.com/dev/api)
-   [SoundCloud](http://developers.soundcloud.com/) (music/audio)
-   [SpaceAPI](http://spaceapi.net/) (hackerspace directory)
-   [Spotify](https://developer.spotify.com/) (music)
-   [Stripe](https://stripe.com/docs/stripe.js) (payment)
-   [Transitland](https://transit.land/how-it-works/) (public transit)
-   [Tumblr](http://www.tumblr.com/docs/en/api/v2)
-   [Twilio Client](http://www.twilio.com/client) (audio/video)
-   [Vimeo Simple API](http://developer.vimeo.com/apis/simple) (video)
-   Wikipedia, via [DBpedia](http://dbpedia.org/About) or [MediaWiki](http://www.mediawiki.org/wiki/API) (information)
-   [Wolfram Alpha](http://products.wolframalpha.com/api/) (information, math, etc.)

## APIs that require server-side programming for authorization

-   [Instagram](http://instagram.com/developer/) (images)
-   [Twitter](https://dev.twitter.com/docs)

# References

-   <https://github.com/toddmotto/public-apis>
-   <https://en.wikipedia.org/wiki/List_of_open_APIs>
-   <https://gist.github.com/afeld/4952991>
-   <https://github.com/jdorfman/awesome-json-datasets>
-   <https://github.com/caesar0301/awesome-public-datasets>
