^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package moveit_ros_move_group
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.1.0 (2019-12-29)
------------------
* TfPublisher: fixup and add attached collsion objects (`#1792 <https://github.com/JafarAbdi/moveit/issues/1792>`_)
  * fixed transform timestamp
  * The move_group TfPublisher capability now also publishes attached collision objects and their subframes to the tf system
* move_group capability for publishing planning scene frames to the tf system (`#1761 <https://github.com/JafarAbdi/moveit/issues/1761>`_)
  Added a move_group capability, which publishes the frames of planning scene objects to the tf system.
* Merge `#1773 <https://github.com/JafarAbdi/moveit/issues/1773>`_: Fix compiler warnings
* fix unused parameter warnings
* move isEmpty test functions to moveit_core/utils (`#1627 <https://github.com/JafarAbdi/moveit/issues/1627>`_)
* Fix binary artifact install locations. (`#1575 <https://github.com/JafarAbdi/moveit/issues/1575>`_)
* Switch from include guards to pragma once (`#1615 <https://github.com/JafarAbdi/moveit/issues/1615>`_)
* Use CMAKE_CXX_STANDARD to enforce c++14 for portability (`#1607 <https://github.com/JafarAbdi/moveit/issues/1607>`_)
  * favor CMAKE_CXX_STANDARD to enforce c++14
  * update all cmake_minimum_required usage
* Remove ! from MoveIt name (`#1590 <https://github.com/JafarAbdi/moveit/issues/1590>`_)
* Cleanup move_group capabilities (`#1515 <https://github.com/JafarAbdi/moveit/issues/1515>`_)
  - use namespace definition to reduce verboseness of individual method signatures
  - use capability name for ROS console messages
* get_planning_scene_service: return full scene when nothing was requested (`#1424 <https://github.com/JafarAbdi/moveit/issues/1424>`_)
* Clang tidy fix `modernize-loop-convert` to entire code base (`#1419 <https://github.com/JafarAbdi/moveit/issues/1419>`_)
* separate source file for CartesianInterpolator (`#1149 <https://github.com/JafarAbdi/moveit/issues/1149>`_)
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
* Contributors: Dave Coleman, Jens P, JonasTietz, Jonathan Binney, Michael Görner, Mike Lautman, Robert Haschke, Sean Yen, Yu, Yan

1.0.1 (2019-03-08)
------------------
* [improve] Apply clang tidy fix to entire code base (Part 1) (`#1366 <https://github.com/ros-planning/moveit/issues/1366>`_)
* Contributors: Yu, Yan

1.0.0 (2019-02-24)
------------------
* [fix] catkin_lint issues (`#1341 <https://github.com/ros-planning/moveit/issues/1341>`_)
* [improve] Remove (redundant) random seeding and #attempts from RobotState::setFromIK() as the IK solver perform random seeding themselves. `#1288 <https://github.com/ros-planning/moveit/issues/1288>`_
* Contributors: Robert Haschke

0.10.8 (2018-12-24)
-------------------

0.10.7 (2018-12-13)
-------------------

0.10.6 (2018-12-09)
-------------------
* [fix] Fixed various memory leaks (`#1104 <https://github.com/ros-planning/moveit/issues/1104>`_)
* [maintenance] Replaced Eigen::Affine3d -> Eigen::Isometry3d (`#1096 <https://github.com/ros-planning/moveit/issues/1096>`_)
* [maintenance] Code Cleanup
  * `#1180 <https://github.com/ros-planning/moveit/issues/1180>`_
  * `#1196 <https://github.com/ros-planning/moveit/issues/1196>`_
* Contributors: Dave Coleman, Robert Haschke

0.10.2 (2018-10-24)
-------------------
* [fix] PlanningSceneMonitor lock `#1033 <https://github.com/ros-planning/moveit/issues/1033>`_: Fix `#868 <https://github.com/ros-planning/moveit/issues/868>`_ (`#1057 <https://github.com/ros-planning/moveit/issues/1057>`_)
* [maintenance] various compiler warnings (`#1038 <https://github.com/ros-planning/moveit/issues/1038>`_)
* [maintenance] add minimum required pluginlib version (`#927 <https://github.com/ros-planning/moveit/issues/927>`_)
* Contributors: Mikael Arguedas, Mohmmad Ayman, Robert Haschke, mike lautman

0.10.1 (2018-05-25)
-------------------
* Remove deprecated ExecuteTrajectoryServiceCapability (`#833 <https://github.com/ros-planning/moveit/issues/833>`_)
* migration from tf to tf2 API (`#830 <https://github.com/ros-planning/moveit/issues/830>`_)
* Add namespace capabilities to moveit_commander (`#835 <https://github.com/ros-planning/moveit/issues/835>`_)
* [fix] MoveAction capability can drop cancel request if it is sent shortly after goal is sent (`#756 <https://github.com/ros-planning/moveit/issues/756>`_)
* Contributors: Dave Coleman, Ian McMahon, Mikael Arguedas, Robert Haschke, Will Baker

0.9.11 (2017-12-25)
-------------------

0.9.10 (2017-12-09)
-------------------
* [fix] always return true in MoveGroupPlanService callback `#674 <https://github.com/ros-planning/moveit/pull/674>`_
* [improve] adding swp's to gitignore and removing redundant capabilites from capability_names.h (`#704 <https://github.com/ros-planning/moveit/issues/704>`_)
* Contributors: Mike Lautman, Shingo Kitagawa

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
* [fix] race conditions when updating PlanningScene (`#350 <https://github.com/ros-planning/moveit/issues/350>`_)
* [maintenance] clang-format upgraded to 3.8 (`#367 <https://github.com/ros-planning/moveit/issues/367>`_)
* Contributors: Dave Coleman, Robert Haschke

0.9.3 (2016-11-16)
------------------
* [maintenance] Updated package.xml maintainers and author emails `#330 <https://github.com/ros-planning/moveit/issues/330>`_
* Contributors: Dave Coleman, Ian McMahon

0.9.2 (2016-11-05)
------------------

0.6.6 (2016-06-08)
------------------
* added missing validity check
  iterator found with `configs.find()` needs to be validated before use...
* Removed trailing whitespace from entire repository
* moved planner params services into existing capability QueryPlannerInterfaces
* capability plugin MoveGroupPlannerParamsService to get/set planner params
* Fixed bug(?) in move_group::MoveGroupKinematicsService::computeIK link name selection.
* Contributors: Dave Coleman, Mihai Pomarlan, Robert Haschke

0.6.5 (2015-01-24)
------------------
* update maintainers
* Contributors: Michael Ferguson

0.6.4 (2014-12-20)
------------------

0.6.3 (2014-12-03)
------------------

0.6.2 (2014-10-31)
------------------
* Merge pull request `#522 <https://github.com/ros-planning/moveit_ros/issues/522>`_ from mikeferguson/indigo-devel
  add dependency on std_srvs (part of octomap clearing service)
* Contributors: Ioan A Sucan, Michael Ferguson

0.6.1 (2014-10-31)
------------------

0.6.0 (2014-10-27)
------------------
* Added move_group capability for clearing octomap.
* Contributors: Dave Hershberger, Sachin Chitta

0.5.19 (2014-06-23)
-------------------
* Address [cppcheck: duplicateIf] error.
  The same condition was being checked twice, and the same action was being taken.
* Contributors: Adolfo Rodriguez Tsouroukdissian

0.5.18 (2014-03-23)
-------------------

0.5.17 (2014-03-22)
-------------------
* update maintainer e-mail
* Contributors: Ioan Sucan

0.5.16 (2014-02-27)
-------------------
* empty state should be a diff state, otherwise attached objects are deleted
* Contributors: sachinc

0.5.14 (2014-02-06)
-------------------

0.5.13 (2014-02-06)
-------------------

0.5.12 (2014-01-03)
-------------------

0.5.11 (2014-01-03)
-------------------

0.5.10 (2013-12-08)
-------------------

0.5.9 (2013-12-03)
------------------
* Re-ordered movegroup's initialization, so capabilities start after monitors.
* correcting maintainer email
* Added planning feedback to gui, refactored states tab

0.5.8 (2013-10-11)
------------------

0.5.7 (2013-10-01)
------------------

0.5.6 (2013-09-26)
------------------

0.5.5 (2013-09-23)
------------------
* porting to new RobotState API
* more console output

0.5.4 (2013-08-14)
------------------

* make headers and author definitions aligned the same way; white space fixes
* Dependency for move_group_capabilities_base fixed.

0.5.2 (2013-07-15)
------------------

0.5.1 (2013-07-14)
------------------

0.5.0 (2013-07-12)
------------------
* white space fixes (tabs are now spaces)
* port to new base class for planning_interface (using planning contexts)

0.4.5 (2013-07-03)
------------------
* Fixed for moveit_msgs/JointLimits.h no such file or directory

0.4.4 (2013-06-26)
------------------
* fix `#259 <https://github.com/ros-planning/moveit_ros/issues/259>`_ and `#260 <https://github.com/ros-planning/moveit_ros/issues/260>`_.
