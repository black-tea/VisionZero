# Quantifying the Estimated Safety Benefits of Engineering Changes

This script was used to estimate the safety benefit from engineering changes, specificly a road diet, which transforms a roadway that with two vehicle travel lanes in each direction into a roadway with one vehicle travel lane in each direction and a center turn lane.



Please suggest improvements! I am by no means a professional pythoner.

### General Requirements

- Python
- Geocoded collision data with the following fields:
  - Movement preceding the collision for each party
  - Direction of travel for each party
- A geocoded network that includes [segments] (http://geohub.lacity.org/datasets/d3cd48afaacd4913b923fd98c6591276_36) and [intersections] (http://geohub.lacity.org/datasets/0372aa1fb42a4e29adb9caadcfb210bb_9).
- This script uses the arcpy cursor functions within Arcmap, but you could reformat it to match the way your data is stored.

### Script Input

- SWITRS-formatted collision data including the following tables:
  - [Collision Table] (http://geohub.lacity.org/datasets/bed43aa2945a47b18ae888246712ccb1_0)
  - [Party Table] (http://geohub.lacity.org/datasets/8cfe25a12dca4826b6a311470c76f1ea_1)
- CSV table listing the corridor ID(s), centerline segment IDs, and travel directions of the segment (example below)

<dl>
<dt>hello</dt>
  
| Corridor ID   | BOE Segment ID| Dir   |
| ------------- |---------------| ------|
| 1             | 2098          | E,W   |
| 1             | 4643          | E,W   |
| 1             | 5325          | E,W   |
| 1             | 7135          | E,W   |
| 1             | 12095         | E,W   |
  

</dl>
- another CSV table listing the corridor ID(s) and centerline intersection IDs (example below)

| Corridor ID   | BOE Intersection ID|
| ------------- |--------------------|
| 1             | 96407              |
| 1             | 99928              |
| 1             | 110461             |
| 1             | 117460             |
| 1             | 117487             |

<center>

| Tables   |      Are      |  Cool |
|----------|:-------------:|------:|
| col 1 is |  left-aligned | $1600 |
| col 2 is |    centered   |   $12 |
| col 3 is | right-aligned |    $1 |

</center>
