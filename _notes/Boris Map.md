I made a map called "Boris Starred" using [[Facilmap]] and changed the read-only link to <https://facilmap.org/boris>.

It has a Starred layer, and a [[FoodWiki]] layer.

I'd need to break those into two different maps if I wanted to give different people collaborative access to it.

The embedded map includes the location hash so it's centered around Vancouver.

## Updates

January 13th, 2024
* I used [Google Takeout](https://takeout.google.com) to export all of my Saved Places
* It's an almost 1MB GeoJSON file which is 20K lines long
* There were ~200 or so which had a location / GMaps query string, but said "no location information available" and the coordinates set to 0,0; I manually went through and deleted all those entries
* Importing into [[Facilmap]] timed out with the full file
* I manually split it into ~3500 line files, and imported them all
* It does import! I have all my Starred (and I assume Want To Go, and Closed, and a bunch of public and private lists, which aren't labeled in the export) on the map
* But! They're all labeled as "Point", rather than including the name of the thing I have starred

## Map

<iframe style="height: 500px; width: 100%; border: none;" src="https://facilmap.org/boris#11/49.2658/-122.9741/Mpnk"></iframe>

Default of this map is centered on the Vancouver area.
## To Do

- [x] Export Google Stars and Import ([Import](https://docs.facilmap.org/users/import/) GPX, KML or GeoJSON files.)
- [ ] Explore transforming Google Maps GeoJSON to Facilmap compatible (with names, etc)