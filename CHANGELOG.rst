^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package moveit_ros_occupancy_map_monitor
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.1.0 (2019-12-29)
------------------
* Merge `#1773 <https://github.com/JafarAbdi/moveit/issues/1773>`_: Fix compiler warnings
* silent warnings outside MoveIt code base
* [windows] some more header inclusion and MSVC build error fixes. (`#1636 <https://github.com/JafarAbdi/moveit/issues/1636>`_)
  * Fix header inclusion for Windows build.
  * replace random() with c++11 <random> usage.
* Fix binary artifact install locations. (`#1575 <https://github.com/JafarAbdi/moveit/issues/1575>`_)
* Switch from include guards to pragma once (`#1615 <https://github.com/JafarAbdi/moveit/issues/1615>`_)
* Update occupancy grid when loaded from file (`#1594 <https://github.com/JafarAbdi/moveit/issues/1594>`_)
* Use CMAKE_CXX_STANDARD to enforce c++14 for portability (`#1607 <https://github.com/JafarAbdi/moveit/issues/1607>`_)
  * favor CMAKE_CXX_STANDARD to enforce c++14
  * update all cmake_minimum_required usage
* Remove ! from MoveIt name (`#1590 <https://github.com/JafarAbdi/moveit/issues/1590>`_)
* move occupancy_map_monitor into its own package (`#1533 <https://github.com/JafarAbdi/moveit/issues/1533>`_)
  Factor out occupancy_map_monitor into a new package moveit_ros_occupancy_map
  to break the dependency of ros_planning on ros_perception.
* Contributors: Dave Coleman, Jonathan Binney, Raphael Druon, Robert Haschke, Sean Yen, jschleicher
