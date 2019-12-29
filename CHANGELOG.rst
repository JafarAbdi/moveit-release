^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package moveit_kinematics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.1.0 (2019-12-29)
------------------
* Merge `#1773 <https://github.com/JafarAbdi/moveit/issues/1773>`_: Fix compiler warnings
* fix -Woverloaded-virtual warnings
  Due to a different order of arguments, there was an extra layer of function forwarding for searchPositionIK.
* fix unused parameter warnings
* delete IKCache copy constructor (`#1750 <https://github.com/JafarAbdi/moveit/issues/1750>`_)
  It never existed, because the class contains a mutex object (not copyable).
  clang complained about this discrepancy.
* optional prefix for link names in ikfast plugin (`#1599 <https://github.com/JafarAbdi/moveit/issues/1599>`_)
  If you pass a `link_prefix` parameter in your `kinematics.yaml`, this string is prepended to the base and tip links. It allows multi-robot setups (e.g. dual-arm) and still instantiate the same solver for both manipulators.
* Fix binary artifact install locations. (`#1575 <https://github.com/JafarAbdi/moveit/issues/1575>`_)
* Switch from include guards to pragma once (`#1615 <https://github.com/JafarAbdi/moveit/issues/1615>`_)
* Use CMAKE_CXX_STANDARD to enforce c++14 for portability (`#1607 <https://github.com/JafarAbdi/moveit/issues/1607>`_)
  * favor CMAKE_CXX_STANDARD to enforce c++14
  * update all cmake_minimum_required usage
* Remove ! from MoveIt name (`#1590 <https://github.com/JafarAbdi/moveit/issues/1590>`_)
* Relax dependencies of moveit_kinematics (`#1529 <https://github.com/JafarAbdi/moveit/issues/1529>`_)
  * relax dependencies of moveit_kinematics
  * renamed measure_ik_call_cost to benchmark_ik
* KDL IK solver: fix handling of mimic joints (`#1490 <https://github.com/JafarAbdi/moveit/issues/1490>`_)
  - correctly count mimic joints
  - don't resize extra_joint_weights vector
  Fixes an issue introduced in 5bedb7a31db8ab4ac7e474de762e5dfc42ad4d13.
* ikfast: fix ROS apt-key in OpenRAVE docker image (`#1503 <https://github.com/JafarAbdi/moveit/issues/1503>`_)
* Fix ikfast plugin-generator script (`#1492 <https://github.com/JafarAbdi/moveit/issues/1492>`_)
* IKFast: increase verbosity of generated script (`#1434 <https://github.com/JafarAbdi/moveit/issues/1434>`_)
* IKFastPlugin: fix initialization of RobotState (`#1449 <https://github.com/JafarAbdi/moveit/issues/1449>`_)
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
* Contributors: Christian Henkel, Dave Coleman, Immanuel Martini, Jonathan Binney, Michael Görner, Robert Haschke, Sean Yen, Yu, Yan, jschleicher

1.0.1 (2019-03-08)
------------------
* [improve] Apply clang tidy fix to entire code base (Part 1) (`#1366 <https://github.com/ros-planning/moveit/issues/1366>`_)
* Contributors: Robert Haschke, Yu, Yan

1.0.0 (2019-02-24)
------------------
* [fix] catkin_lint issues (`#1341 <https://github.com/ros-planning/moveit/issues/1341>`_)
* [capability] Adapt ikfast plugin to new KinematicsBase API. `#1320 <https://github.com/ros-planning/moveit/issues/1320>`_
* [improve] cleanup LMA kinematics solver `#1318 <https://github.com/ros-planning/moveit/issues/1318>`_
* [improve] KDL IK solver improvements (`#1321 <https://github.com/ros-planning/moveit/issues/1321>`_)
* [improve] Kinematics tests, kdl cleanup `#1272 <https://github.com/ros-planning/moveit/issues/1272>`_, `#1294 <https://github.com/ros-planning/moveit/issues/1294>`_
* Contributors: Dave Coleman, Jorge Nicho, Mike Lautman, Robert Haschke

0.10.8 (2018-12-24)
-------------------

0.10.7 (2018-12-13)
-------------------

0.10.6 (2018-12-09)
-------------------
* [enhancement] Pass RobotModel to IK, avoiding multiple loading (`#1166 <https://github.com/ros-planning/moveit/issues/1166>`_)
  See `MIGRATION notes <https://github.com/ros-planning/moveit/blob/melodic-devel/MIGRATION.md>`_ for API changes in IK plugins,
  kdl, srv, or cached_ik for examples.
* [maintenance] Replaced Eigen::Affine3d -> Eigen::Isometry3d (`#1096 <https://github.com/ros-planning/moveit/issues/1096>`_)
* [maintenance] Use C++14 (`#1146 <https://github.com/ros-planning/moveit/issues/1146>`_)
* Contributors: Alex Moriarty, Michael Görner, Robert Haschke

0.10.5 (2018-11-01)
-------------------

0.10.4 (2018-10-29)
-------------------

0.10.3 (2018-10-29)
-------------------

0.10.2 (2018-10-24)
-------------------
* [capability] add IKP_Translation{X,Y,Z}AxisAngle4D to the cpp template, see https://github.com/ros-planning/moveit/issues/548#issuecomment-316298918
* [maintenance] various compiler warnings (`#1038 <https://github.com/ros-planning/moveit/issues/1038>`_)
* Contributors: Kei Okada, Mikael Arguedas, Mohmmad Ayman, Robert Haschke, mike lautman, v4hn

0.10.1 (2018-05-25)
-------------------
* migration from tf to tf2 API (`#830 <https://github.com/ros-planning/moveit/issues/830>`_)
* switch to ROS_LOGGER from CONSOLE_BRIDGE (`#874 <https://github.com/ros-planning/moveit/issues/874>`_)
* fixes to ikfast kinematics plugin (`#808 <https://github.com/ros-planning/moveit/issues/808>`_)
* Cached ik kinematics plugin (`#612 <https://github.com/ros-planning/moveit/issues/612>`_)
  add caching wrapper for IK solvers
* Contributors: Ian McMahon, Mark Moll, Mikael Arguedas, Robert Haschke, Xiaojian Ma

0.9.11 (2017-12-25)
-------------------
* Merge pull request `#714 <https://github.com/ros-planning/moveit/issues/714>`_ from henhenhen/kinetic-devel_lookup-param
  Use lookupParam() in kinematics plugins
* Replace param() with lookupParam() in srv_kinematics_plugin
* Replace param() with lookupParam() in lma_kinematics_plugin
* Replace param() with lookupParam() in kdl_kinematics_plugin
* Replace param() with lookupParam() in ikfast_kinematics_plugin
* Remove redundant parameter query
* Contributors: Henning Kayser, Isaac I.Y. Saito

0.9.10 (2017-12-09)
-------------------
* [fix][kinetic onward] Fix create_ikfast_moveit_plugin to comply with format 2 of the package.xml. Remove collada_urdf dependency `#666 <https://github.com/ros-planning/moveit/pull/666>`_
* [fix] create_ikfast_moveit_plugin: fixed directory variable for templates that were moved to ikfast_kinematics_plugin `#620 <https://github.com/ros-planning/moveit/issues/620>`_
* [improve] IKFastTemplate: Expand solutions to full joint range in searchPositionIK `#598 <https://github.com/ros-planning/moveit/issues/598>`_
* [improve] IKFastTemplate: searchPositionIK now returns collision-free solution which is nearest to seed state. (`#585 <https://github.com/ros-planning/moveit/issues/585>`_)
* Contributors: Dennis Hartmann, G.A. vd. Hoorn, Michael Görner, fsuarez6

0.9.9 (2017-08-06)
------------------
* [improve] Modify ikfast_template for getPositionIK single solution results (`#537 <https://github.com/ros-planning/moveit/issues/537>`_)
* Contributors: nsnitish

0.9.8 (2017-06-21)
------------------
* [build] ikfast_kinematics_plugin: Write XML files as UTF-8 (`#514 <https://github.com/ros-planning/moveit/issues/514>`_)
* [build] adjust cmake_minimum_required for add_compile_options (`#521 <https://github.com/ros-planning/moveit/issues/521>`_)
* [build] ikfast_kinematics_plugin: Add c++11 compile option. This is required for Kinetic.
* Contributors: Martin Guenther, Michael Goerner

0.9.7 (2017-06-05)
------------------
* [fix][Kinetic+] ikfast_kinematics_plugin: Add c++11 compile option `#515 <https://github.com/ros-planning/moveit/pull/515>`_
* [fix][Indigo] moveit_kinematics Eigen3 dependency (`#470 <https://github.com/ros-planning/moveit/issues/470>`_)
* Contributors: Martin Guenther, YuehChuan

0.9.6 (2017-04-12)
------------------

0.9.5 (2017-03-08)
------------------
* [fix][moveit_ros_warehouse] gcc6 build error `#423 <https://github.com/ros-planning/moveit/pull/423>`_ 
* Contributors: Dave Coleman

0.9.4 (2017-02-06)
------------------
* [maintenance] clang-format upgraded to 3.8 (`#367 <https://github.com/ros-planning/moveit/issues/367>`_)
* Contributors: Dave Coleman

0.9.3 (2016-11-16)
------------------
* [fix] Replace unused service dependency with msg dep (`#361 <https://github.com/ros-planning/moveit/issues/361>`_)
* [maintenance] Updated package.xml maintainers and author emails `#330 <https://github.com/ros-planning/moveit/issues/330>`_
* Contributors: Dave Coleman, Ian McMahon

0.9.2 (2016-11-05)
------------------
* [Maintenance] Auto format codebase using clang-format (`#284 <https://github.com/ros-planning/moveit/issues/284>`_)
* Contributors: Dave Coleman

0.9.0 (2016-10-19)
------------------
* Add dependency on new moveit_kinematics package
* Move moveit_ikfast into moveit_kinematics
* Moved kinematics plugins to new pkg moveit_kinematics
* Contributors: Dave Coleman

0.8.3 (2016-08-21)
------------------
