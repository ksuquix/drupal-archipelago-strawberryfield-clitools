# drupal-archipelago-strawberryfield-clitools
Some tools I've Made for CLI scripting of importing/manipulating Archipelago Digital Objects (and Collections) with strawberryfield manipulation

Required packages:
  jq
  php

Usage:  arch OBJ ACTION ....

OBJ:  do or dc (for digital_object or digital_object_collection)

ACTIONS:

list
* Lists all objects of type x (limit of 50, need to add pagination) in summary form

fetch UUID
* Fetches raw object

fetchstrawberry UUID
* extracts the strawberryfields data item

summarize UUID
* gets summary of a single object

search string
* Lists summary of all objects with title containing string

uploadfiles UUID file1 [file2 ...]
* Uploads files and adds into images/documents/models in strawberryfields

new title description tags memberof [file1 ...]
* Creates new object with title and description
* tags are mapped to subjects_local.  comma separated, make it one argument (can contain the whole argument in quotes)
* memberof is the sid of the object that is the parent of this one

