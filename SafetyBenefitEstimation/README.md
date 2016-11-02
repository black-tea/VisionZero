# Quantifying the Estimated Safety Benefits of Engineering Changes

This script was used to estimate the safety benefit from engineering changes, specificly a road diet, which transforms a roadway that with two vehicle travel lanes in each direction into a roadway with one vehicle travel lane in each direction and a center turn lane.

identify candidate locations for new protected-left turn signals in the City of Los Angeles based on safety warrant criteria specified in the [California Manual on Uniform Traffic Control Devices] (http://www.dot.ca.gov/trafficops/camutcd/). LADOT then submitted the top locations for funding through the [Metro ExpressLanes Net Toll Revenue Re-Investment Grant Program.] (https://www.metro.net/projects/expresslanes/projectsprograms/)

Please suggest improvements! I am by no means a professional pythoner.

### Requirements

- Python
- Geocoded collision data with the following fields:
  - Movement preceding the collision for each party
  - Direction of travel for each party
- A geocoded network that includes [segments] (http://geohub.lacity.org/datasets/d3cd48afaacd4913b923fd98c6591276_36) and [intersections] (http://geohub.lacity.org/datasets/0372aa1fb42a4e29adb9caadcfb210bb_9).
- This script uses the arcpy cursor functions within Arcmap, but you could reformat it to match the way your data is stored.
