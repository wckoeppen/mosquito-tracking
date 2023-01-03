# mosquito-tracking
## Experimental Setup
The experimental setup has a camera set up near the floor, tilted slightly upwards, aimed into a controlled (netted) chamber. The experiment chamber is a 3D volume that is roughly a [4-sided square frustrum](https://en.wikipedia.org/wiki/Frustum), the front being a glass plate through wich the camera looks. The sides and back of the chamber are bounded by netting, which are set up so that, according to the perspective view through the camera, looks approximately square. Meanwhile, there is an inner chamber, also netted off in which a subject can reside. The inner chamber is in the middle back of the experimental chamber.

A human is typically (but not always) in the inner chamber. The experiment begins when insects are released from a vial into the chamber.

## Data Format
These data are exported from the pfmd.net dataset as CSVs. The data includes the following fields:
- `id`: A unique ID that associates what the program has determined is a individual. This may be a true continous track of an individual, or it may be a new id given to an existing individual that became untracked for some reason.
- `datetime`: The recorded datetime of the location. Points are generally recorded every hundreth of a second. A "long" track might be something like 10 seconds (1000 recorded points) long.

In terms of data geometry:
- `x_cm`: the left to right distance.
- `y_cm`: the up-down distance.
- `z_cm`: the depth in the field of view, i.e., the distance from the camera.

There are also some ancillary fields:
- `size_mm2`: this is the measured size according to the camera and software. It can vary somewhat, but overall seems to be able to guage the size of the insect population inside the net.
- `speed_mps`: the current speed of the tracked individual
- `acceleration_mps2`: the acceleration from the last point
- `distance_cm`: distance of this individual flown along the track