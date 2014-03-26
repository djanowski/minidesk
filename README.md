minidesk
========

Minidesk will be a minimal help desk / ticketing system mounted on top of other services like GitHub and Google Apps.

For now, this is just a design and goals document. Feel free to discuss in the [issues section](https://github.com/djanowski/minidesk/issues).

Goals
-----

Minidesk should:

1. Be open-source.
2. Be easy to use by support agents and content editors.
3. Be relatively simple to set up by a programmer.
4. Leverage other services as much as possible: GitHub, Google Apps, AWS, etc.
5. Serve startups and small companies that hate to pay $59 per team member.

Features
--------

For the help desk:

* Email integration: tickets are conversations with clients. One or multiple support email addresses for incoming issues.
* Ticket owners: tickets can be delegated to other team members.
* Ticket status: it should, at least, differentiate between pending (no reply yet), in progress and closed (archived?).
* Canned responses: quickly insert predefined snippets of text with answers to common problems.
* Knowledge base integration: find and insert links to relevant parts of the knowledge base.

2. Knowledge base

* CMS: a static content site with sections and articles.
* Full text search.
* Multi-language support: each article can have translated variants.
   
Possible integrations
---------------------

We want to be as lean as possible and reuse as many services as possible.

* **Google Apps**: Could provide authentication.
* **Gmail**: Could Gmail (or the Google Apps flavor) be used for managing tickets? Would tags be enough for proritization and delegation of tickets?
* **GitHub**: Your knowledge base could be an open source repository, similar to [redis-doc](https://github.com/antirez/redis-doc). Then some artifact could build your site into static HTML and push the result into your `gh-pages` branch. That way we could have a help site hosted on GitHub, with its optional custom domains. Full text search on the site could be done client-side with something like [lunr.js](http://lunrjs.com/).
