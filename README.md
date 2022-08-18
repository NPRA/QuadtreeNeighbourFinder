# QuadtreeNeighbourFinder
Program to find neighbouring tiles in a quadtree.

## Quadtree.java
Generates a quadtree-tile from a lat/lon at a given zoom level.

## QuadTreeHelper.java
Finds neighbour tiles to the given quadtree tile.
You can either find a specific neighbour (see below) or get all 8 neighbour tiles around the given tile.

||||
|:---:|:---:|:---:|
|(LU) left-up|(U) up|(RU) right-up|
|left|given tile|right|
|(LD) left-down|(D) down|(RD) right-down|

            getNeighbour(QuadTreeHelper.LU, centerQT),
            getNeighbour(QuadTreeHelper.U, centerQT),
            getNeighbour(QuadTreeHelper.RU, centerQT),
            getNeighbour(QuadTreeHelper.L, centerQT),
            centerQT,
            getNeighbour(QuadTreeHelper.R, centerQT),
            getNeighbour(QuadTreeHelper.LD, centerQT),
            getNeighbour(QuadTreeHelper.D, centerQT),
            getNeighbour(QuadTreeHelper.RD, centerQT),

## Visualize Tiles
To help visualize tiles, this little helper program can be used: <https://github.com/NPRA/quadtree-helper>  
Either run the gist (link in the readme) in your browser, or deploy it yourself.

## TODO
- Add tile generator for a given polygon.
- Add an algorithm to generate a minimal set of tiles to fill a polygon.
