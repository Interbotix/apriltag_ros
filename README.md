# apriltags2_ros

This is a Robot Operating System (ROS) wrapper of the [AprilTags 2 visual fiducial detector](https://april.eecs.umich.edu/software/apriltag.html). For details and tutorials, please see the [ROS wiki](http://wiki.ros.org/apriltags2_ros).

**Authors**: Danylo Malyuta  
**Maintainer**: Danylo Malyuta, danylo.malyuta@gmail.com  
**Affiliation**: NASA Jet Propulsion Laboratory, California Institute of Technology

# Contributing

Pull requests are welcome! Especially for the following areas:

- Publishing of the AprilTag 2 algorithm intermediate images over a ROS image topic (that AprilTag 2 [already generates](https://github.com/dmalyuta/apriltags2_ros/blob/master/apriltags2/src/apriltag.c#L1167-L1395) when `tag_debug==1`)
- Conversion of the [bundle calibration script](https://github.com/dmalyuta/apriltags2_ros/blob/master/apriltags2_ros/scripts/calibrate_bundle.m) from MATLAB to Python
- Replacement of AprilTag 2 core algorithm's usage of custom linear algebra and image processing functions with Boost and OpenCV

# Copyright

The source code in `apriltags2/` is wholly the work of the [APRIL Robotics Lab](https://april.eecs.umich.edu/software/apriltag.html) at The University of Michigan. This package simply rearranges the source code to be able to compile it with catkin.

The source code in `apriltags2_ros/` is original code that is the ROS wrapper itself, see the [LICENSE](https://github.com/dmalyuta/apriltags2_ros/blob/master/LICENSE). It is inspired by [apriltags_ros](https://github.com/RIVeR-Lab/apriltags_ros) and provides a superset of its functionalities.

If you use this code, please kindly cite:

```
@mastersthesis{malyuta:2017mt,
  author = {Danylo Malyuta},
  title = {{Guidance, Navigation, Control and Mission Logic for Quadrotor Full-cycle Autonomy}},
  language = {english},
  type = {Master thesis},
  school = {Jet Propulsion Laboratory},
  address = {4800 Oak Grove Drive, Pasadena, CA 91109, USA},
  month = dec,
  year = {2017}
}
@inproceedings{Wang2016,
  author = {Wang, John and Olson, Edwin},
  booktitle = {2016 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
  doi = {10.1109/IROS.2016.7759617},
  isbn = {978-1-5090-3762-9},
  month = {oct},
  pages = {4193--4198},
  publisher = {IEEE},
  title = {{AprilTag 2: Efficient and robust fiducial detection}},
  year = {2016}
}
```