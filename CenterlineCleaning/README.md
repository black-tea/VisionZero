# Centerline and Intersection Data Cleaning

The Bureau of Street Engineering currently provides the most comprehensive street network for the City of Los Angeles. This street centerline file, and the intersection nodes generated from it, serve as the foundation for the City's data-driven approach to eliminating traffic deaths by 2025. The Department of Transporation used this python script (and manual checking) to make sure the data was well prepared for analysis.

Please suggest improvements! I am by no means a professional pythoner.

### Requirements

- Python
- [Centerline File] (http://geohub.lacity.org/datasets/d3cd48afaacd4913b923fd98c6591276_36)
- Node/Intersection File
- This script uses the cursor functions within ArcPy, but you could reformat it to match the way your data is stored.

### Preparation

1. First assign all collisions the unique ID of the nearest intersection. The end result should be an additional field in the collisions table that has the unique ID for the related intersection. This script gives more detail on our process at LADOT.
2. For the intersection data, subset out those that are not signalized.
3. For the collision data, filter for collisions involving left or u-turns. Also, remove those involving alcohol.
4. This project was focused only on our most recent year of available data (2013) so we removed those before that year. If you would like to do a multi-year search, see the [Signalized Safety Warrant Project] (https://github.com/black-tea/VisionZero/tree/master/NewSignals) for a method to aggregate by year and rank by most recent year that warrant criteria was met.

### Process Diagram

![Left Turn Warrant Process Diagram](https://github.com/black-tea/VisionZero/blob/master/ProtectedLeft/HSIP_CityWide_LeftTurn.png)