# Protected Left Warrant Search

This script was used to identify candidate locations for new protected-left turn signals in the City of Los Angeles based on safety warrant criteria specified in the [California Manual on Uniform Traffic Control Devices] (http://www.dot.ca.gov/trafficops/camutcd/). LADOT then submitted the top locations for funding through the [Metro ExpressLanes Net Toll Revenue Re-Investment Grant Program.] (https://www.metro.net/projects/expresslanes/projectsprograms/)

Please suggest improvements! I am by no means a professional pythoner.

### Requirements

- Python
- Geocoded collision data with the following fields:
  - Movement preceding the collision for each party
  - Direction of travel for each party
- Geocoded intersections
- This script uses the arcpy cursor functions within Arcmap, but you could reformat it to match the way your data is stored.
