## What it does?
Geohash is a public domain of encoding coordinates. An example of a geohash is the coordinate pair 28.6132,77.2291 being converted into a geohash of ttnfv2u.

Geohash length sizes and corresponding precision levels examples:
- A Geohash of length 1 represents a large area, such as a continent.
- A Geohash of length 2 represents a smaller area, such as a country.
- A Geohash of length 3 represents a region or large city.
- A Geohash of length 4 represents a smaller city or town.
- Geohashes of length 5 or higher represent progressively smaller areas, down to street level and even specific locations.

## How it works?
* Geohashes use Base-32 alphabet encoding (characters can be 0 to 9 and A to Z, excl "A", "I", "L" and "O”)
*  Imagine the world is divided into a grid with 32 cells.
* The first character in a geohash identifies the initial location as one of the 32 cells
* This cell will also contain 32 cells, and each one of these will contain 32 cells (and so on repeatedly).![[Pasted image 20250108183559.jpg]]
Simple way to store location in a DB

# Quadtrees
https://jimkang.com/quadtreevis/

so confusing lols