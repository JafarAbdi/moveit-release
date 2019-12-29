^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package moveit_chomp_optimizer_adapter
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.1.0 (2019-12-29)
------------------
* Merge `#1773 <https://github.com/JafarAbdi/moveit/issues/1773>`_: Fix compiler warnings
* fix unused parameter warnings
* Fix binary artifact install locations. (`#1575 <https://github.com/JafarAbdi/moveit/issues/1575>`_)
* Use CMAKE_CXX_STANDARD to enforce c++14 for portability (`#1607 <https://github.com/JafarAbdi/moveit/issues/1607>`_)
  * favor CMAKE_CXX_STANDARD to enforce c++14
  * update all cmake_minimum_required usage
* Remove ! from MoveIt name (`#1590 <https://github.com/JafarAbdi/moveit/issues/1590>`_)
* Allow ROS namespaces for planning request adapters (`#1530 <https://github.com/JafarAbdi/moveit/issues/1530>`_)
  To allow instantiation of different planning pipeline configurations from different ROS parameter namespaces, pass a NodeHandle to a new initialize() function of PlanningRequestAdapters.
* Merge `#1525 <https://github.com/JafarAbdi/moveit/issues/1525>`_: Fix Chomp planning adapter
* Fix ChompTrajectory initialization from trajectory
* change API of ChompPlanner::solve() to not use message
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
* Contributors: Dave Coleman, Henning Kayser, Robert Haschke, Sean Yen, Yu, Yan

1.0.1 (2019-03-08)
------------------
* [fix] segfault in chomp adapter (`#1377 <https://github.com/ros-planning/moveit/issues/1377>`_)
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
* [maintenance] Moved CHOMP optimizer into own package (`#1251 <https://github.com/ros-planning/moveit/issues/1251>`_)
* rename default_planner_request_adapters/CHOMPOptimizerAdapter -> chomp/OptimizerAdapter
* Contributors: Robert Haschke
