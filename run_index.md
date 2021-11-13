Run index
=========

`run_20211031`
--------------

* Subset of times from `traj2.csv` (see `trajectory.csv`)
* All bodies fully illuminated
* **Incorrect camera quaternions**: Quaternions matched SurRender, where camera frame has y pointing down, but simulation code uses a camera frame with y pointing up.

`run_20211102`
--------------

* t=86400 from `traj2.csv` (should match SurRender case1c) (see `traj-case1c.csv`)
* Illumination from Sun (point source)
* Full stereographic disks outlined in orange
* Corrected camera quaternions (simulation still uses different camera frame from SurRender)
* Added `omega_cam` field (V2)
* Added images with gridlines (with and without illumination) (V2)
* **Compared to SurRender case1c, body positions seem off by approximately 1 frame, even though timestamps of frames match**

`test_20211102`
---------------

* Spacecraft body frame = world frame, no rotation
* Spheres of radius 1 at (0, -4, 4), (0, 0, 4), and (0, 0, 4), visible by cameras B, C, and A respectively
* Middle sphere serves as illuminator
* _Observation:_ When side sphere was used as illuminator, middle sphere rendered larger than ideal stereographic radius when only illumination mask was used (and not angular distance from center mask)
