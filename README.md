# Zen.Hexagons

Hexagon routines for use in for software that uses hexagon grids.
Can be used for pointy-topped or flat-topped hexes and offset, axial or cube coordinate systems.

Uses ideas from Amit Patel's brilliant http://www.redblobgames.com/grids/hexagons/.

Nuget package download: https://www.nuget.org/packages/Zen.Hexagons/1.0.4

# Example
To use:

    var hexLibrary = new Zen.Hexagons.HexLibrary(HexType.FlatTopped, OffsetCoordinatesType.Odd, 64.0f);
    
    var hexCube = hexLibrary.OffsetCoordinatesToCube(new HexOffsetCoordinates(2, 2));
    var hexAxial = hexLibrary.OffsetCoordinatesToAxial(new HexOffsetCoordinates(2, 2));
    
    var neighbors = hexLibrary.GetAllNeighbors(new HexOffsetCoordinates(1, 1));
    var neighborNW = hexLibrary.GetNeighbor(new HexOffsetCoordinates(1, 1), Direction.NorthWest);
    
    var ring1 = hexLibrary.GetSingleRing(new HexOffsetCoordinates(1, 1), 1);
    var ring2 = hexLibrary.GetSingleRing(new HexOffsetCoordinates(2, 2), 2);
    
    var ring3 = hexLibrary.GetSpiralRing(new HexOffsetCoordinates(2, 2), 2);
    
# Developer
Written by Greg Moller (greg.moller@gmail.com)

# License
Licensed under the MIT License. See the LICENCE file for more information.
