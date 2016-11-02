# Quantifying the Estimated Safety Benefits of Engineering Changes

This script was used to estimate the safety benefit from engineering changes, specificly a road diet, which transforms a roadway that with two vehicle travel lanes in each direction into a roadway with one vehicle travel lane in each direction and a center turn lane.



Please suggest improvements! I am by no means a professional pythoner.

### Requirements

- Python
- Geocoded collision data with the following fields:
  - Movement preceding the collision for each party
  - Direction of travel for each party
- A geocoded network that includes [segments] (http://geohub.lacity.org/datasets/d3cd48afaacd4913b923fd98c6591276_36) and [intersections] (http://geohub.lacity.org/datasets/0372aa1fb42a4e29adb9caadcfb210bb_9).
- This script uses the arcpy cursor functions within Arcmap, but you could reformat it to match the way your data is stored.

### Input

- SWITRS-formatted collision data including the following tables:
  - [Collision Table] (http://geohub.lacity.org/datasets/bed43aa2945a47b18ae888246712ccb1_0)
  - [Party Table] (http://geohub.lacity.org/datasets/8cfe25a12dca4826b6a311470c76f1ea_1)
- CSV table listing the corridor ID, centerline segment IDs, and travel directions of the segment (example below)

     | Corridor ID   | BOE Segment ID| Dir   |
     | ------------- |---------------| ------|
     | 1             | right-aligned | $1600 |
     | 1             | centered      |   $12 |
     | 1             | are neat      |    $1 |
