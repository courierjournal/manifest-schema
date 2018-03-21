# Manifest schema
Documentation for the `cj-manifest.json` file that goes in to all Courier Journal off-platform interactive content.


## Purpose
The manifest file lies at the root of every major interactive project that's off-platform. It's used to describe the contents of the interactive and to assist in generating a landing page. 

The `cj-manifest.json` file should *ideally* be generated by the interactive build template which is driven by a configuration file. But can be generated manually according to the schema below if needed.


## Schema
The file is a single JSON object
* __title__ : The title of the interactive (usually whats also placed in the `<title>` tag).
* __description__ : Description of interactive. Usually what's also used as the social description.
* __url__ : Full path of the interactive.
* __thumbnail__ : A thumbnail of the interactive. Can also be the social share card.
* __intitialPublish__ : When the project was originally first published. Format is unix timestamp.
* __lastPublish__ : This was the last time the interactive was updated. Format is unix timestamp.
* __series__ : If the interactive is part of a series, use a unique string here to indentify it.
* __authors__ : Array of authors.
* __keywords__ : Array of keywords that describe the interactive.
* __priority__ : Boolean that describes whether this is a primary project. Ideally you set true to large projects that are popular and in high use.
* __exclude__ : Boolean that allows you to exclude it from being ingested into the landing page.
* __category__ : String that descibes a category for this interactive.


## Example
```
{
  "title": "See the locations of Kentucky’s Civil War monuments, memorials and statues",
  "description": "We’ve mapped the locations of every Confederate and Union monument, memorial and statue known to exist in the state of Kentucky.",
  "url": "https://projects.courier-journal.com/kentucky-civil-war-confederate-union-monuments-memorials-statues",
  "thumbnail": "preview_th.jpg",
  "initialPublish": 1521659711,
  "lastPublish": 1521659793,
  "series": "",
  "authors": [{"name": "Jesse Hazel", "title": "Newsroom Developer"}],
  "keywords": ["Civil War Monuments", "Confederate Statues", "History"],
  "priority": false,
  "exclude": false,
  "category": "Maps"
}
```
