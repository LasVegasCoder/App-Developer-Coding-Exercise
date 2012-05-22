Ticketfly App Developer Coding Exercise
===========================================

Ticketfly is looking for talented, pragmatic application developers who know how to  leverage modern web frameworks whenever possible and fill in the blanks when necessary. The following challenge is designed for you to demonstrate your ability to do just that. Please use the framework/language that you are most comfortable with - if you wish to use Grails, we recommend using 1.3.7 or 2.0.x.

### Some ground rules
At a minimum, this exercise should take 1.5 to 2 hours to complete. If you have more time to devote to it, that’s great. If you don’t have time to implement all the basic features, then find some way of conveying your thoughts on how you might do so. The bonus features are optional, but please give some thought on how you might implement one or two of them.

Given the tight timeline, we don’t expect perfection. This is an exercise in understanding what corners to cut, how to cut them and why.

### The challenge
Create a [very] basic event listing website for a music venue, “Fraser’s” . Each event must consist of at least: event name, headline and support artist(s), event date & time and ticket price. Users must be able to add, edit and remove listings. There should also be a read only view with a master list of all events and detail page for each event.

### Some constraints
We believe in giving our developers as much autonomy as possible, and this challenge is no exception. It is up to you to make decisions on the nitty gritty, but there are 3 basic rules:

* Event date/times can’t overlap
* An artist can’t appear at the same event more than once.
* The same artist can appear at different events

### Bonus Features
We’d be very impressed if you implement any of the the following. If you don’t, have a think about how you might implement a couple:
Choose a 3rd party API to integrate with. Some examples might be: Last.fm, Songkick, Echonest, Sonic Living or perhaps even Ticketfly’s API (see next page for some basic usage information).

* Implement an artist search feature.
* Add the ability for events to have an image.
* Implement some kind of security around the event creation and editing pages.
* Implement a RESTful API that exposes the event data contained in the application
* Write specification-based tests using a framework such as Cucumber or Spock

### Deliverables
Please zip up your source and email it to jobs@ticketfly.com.

Appendix - A quick guide to Ticketfly’s API
===========================================

All of Ticketfly’s event data is available through our API. The most commonly used feature of the API is the “upcoming events” action. 

### Example upcoming event API request:

http://www.ticketfly.com/api/events/upcoming.json?orgId=1&apiKey=LdcdJWkpj1nOl8SwTV0U

The orgId parameter represents the organization you wish to obtain data for. Org 1 is all public events in the USA, and is the org you should use for this exercise.

If you wish to use JSONP, you can add the callback parameter and pass the name of the javascrtipt function that will process the result of the API call:

http://www.ticketfly.com/api/events/upcoming.json?orgId=1&apiKey=LdcdJWkpj1nOl8SwTV0U&callback=myCallbackFunction

Other parameters you might find useful:

**maxResults**: The number of results to display per page  
**pageNum**: The page number to retrieve   
**q**: A text search query. This is used by the search box on ticketfly.com and understands quotes phrases and the use of AND , OR (case sensitive). It matches against the artist name, event name, promoter name and venue name & city. For example:

/api/events/upcoming.json?orgId=1&q=%22The+Lemonheads%22+San+Francisco

**artistName**: Retrieve events for this artist. This only searches against artist names and looks for an exact (but case-insensitive) match.

If you have any questions, please reach out to us.
