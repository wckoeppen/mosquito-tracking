# mosquito-tracking

These data are exported from the pfmd.net dataset as CSVs. The data includes the following fields:

- `id`: A unique ID that associates what the program has determined is a single track. This may be a true continous track, or it may be a single organism that has gone out of the field of view and back in, etc.
- `datetime`: The recorded datetime of the location. Points are generally recorded every hundreth of a second. A "long" track might be something like 20 seconds long.

- `x_cm`: the left to right distance.
- `y_cm`: the up-down distance.
- `z_cm`: the depth in the field of view, i.e., the distance from the camera.

There are also some ancillary fields:

- `size_mm2`: is this used to group points?
- `speed_mps`: the current speed
- `acceleration_mps2`: the acceleration from the last point
- `distance_cm`: distance flown along the track