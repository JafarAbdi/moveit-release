^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package moveit_fake_controller_manager
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.1.0 (2019-12-29)
------------------
* Merge `#1781 <https://github.com/JafarAbdi/moveit/issues/1781>`_: Fix flaky moveit_cpp test
* Handle incomplete group states
  - issue a warning when building the robot model
  - use a RobotState initialized to joint defaults for fake controllers
* Merge `#1773 <https://github.com/JafarAbdi/moveit/issues/1773>`_: Fix compiler warnings
* fix unused parameter warnings
* Fix binary artifact install locations. (`#1575 <https://github.com/JafarAbdi/moveit/issues/1575>`_)
* Use CMAKE_CXX_STANDARD to enforce c++14 for portability (`#1607 <https://github.com/JafarAbdi/moveit/issues/1607>`_)
  * favor CMAKE_CXX_STANDARD to enforce c++14
  * update all cmake_minimum_required usage
* Remove ! from MoveIt name (`#1590 <https://github.com/JafarAbdi/moveit/issues/1590>`_)
* Clang tidy fix `modernize-loop-convert` to entire code base (`#1419 <https://github.com/JafarAbdi/moveit/issues/1419>`_)
* Apply clang tidy fix to entire code base (Part 2) (`#1394 <https://github.com/JafarAbdi/moveit/issues/1394>`_)
  * Conform class name to `CamelCase`
  * Conform member method name to `camelBack`
  * Exceptions to method name
  * Conform local variable name to `lower_case` part 1
  * Conform local variable name to `lower_case` part 2
  * Conform local variable name to `lower_case` part 3
  * Conform local variable name to `lower_case` part 4
  * Local static variable to `lower_case`
  * Local variable manual fix
  * Exceptions to local variable name
  * Conform static const variable name to `UPPER_CASE`
  * Conform global variable name to `UPPER_CASE`
  * Conform static const member variable to `UPPER_CASE`
  * clang-format
  * Travis: mandatory clang-tidy-check
  * Catch up most recent changes
  * Update .clang-tidy
  * fixup! Conform static const variable name to `UPPER_CASE`
* Contributors: Dave Coleman, Robert Haschke, Sean Yen, Yu, Yan

1.0.1 (2019-03-08)
------------------
* [improve] Apply clang tidy fix to entire code base (Part 1) (`#1366 <https://github.com/ros-planning/moveit/issues/1366>`_)
* Contributors: Robert Haschke, Yu, Yan

1.0.0 (2019-02-24)
------------------
* [fix] catkin_lint issues (`#1341 <https://github.com/ros-planning/moveit/issues/1341>`_)
* Contributors: Robert Haschke

0.10.8 (2018-12-24)
-------------------

0.10.7 (2018-12-13)
-------------------

0.10.6 (2018-12-09)
-------------------
* [maintenance] Code Cleanup (`#1196 <https://github.com/ros-planning/moveit/issues/1196>`_)
* Contributors: Robert Haschke

0.10.5 (2018-11-01)
-------------------

0.10.4 (2018-10-29)
-------------------

0.10.3 (2018-10-29)
-------------------

0.10.2 (2018-10-24)
-------------------
* [fix] latch initial pose published by fake_controller_manager (`#1092 <https://github.com/ros-planning/moveit/issues/1092>`_)
* [maintenance] add minimum required pluginlib version (`#927 <https://github.com/ros-planning/moveit/issues/927>`_)
* Contributors: Mikael Arguedas, Mike Lautman, Mohmmad Ayman, mike lautman

0.10.1 (2018-05-25)
-------------------
* switch to ROS_LOGGER from CONSOLE_BRIDGE (`#874 <https://github.com/ros-planning/moveit/issues/874>`_)
* Contributors: Mikael Arguedas, Xiaojian Ma

0.9.11 (2017-12-25)
-------------------

0.9.10 (2017-12-09)
-------------------

0.9.9 (2017-08-06)
------------------

0.9.8 (2017-06-21)
------------------

0.9.7 (2017-06-05)
------------------

0.9.6 (2017-04-12)
------------------

0.9.5 (2017-03-08)
------------------
* [fix][moveit_ros_warehouse] gcc6 build error `#423 <https://github.com/ros-planning/moveit/pull/423>`_ 
* [enhancement] Remove "catch (...)" instances, catch std::exception instead of std::runtime_error (`#445 <https://github.com/ros-planning/moveit/issues/445>`_)
* Contributors: Bence Magyar, Dave Coleman

0.9.4 (2017-02-06)
------------------
* [maintenance] clang-format upgraded to 3.8 (`#367 <https://github.com/ros-planning/moveit/issues/367>`_)
* Contributors: Dave Coleman

0.9.3 (2016-11-16)
------------------

0.5.7 (2016-01-30)
------------------

0.5.6 (2014-03-23)
------------------

0.5.5 (2013-09-30)
------------------

0.5.4 (2013-09-24)
------------------
* do no look for deps we do not need

0.5.3 (2013-09-23)
------------------
* initial version
