^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package moveit_jog_arm
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Forthcoming
-----------
* Fix versioning
* moveit_jog_arm: Get transforms from RobotState instead of TF (`#1803 <https://github.com/JafarAbdi/moveit/issues/1803>`_)
* jog_arm: add a C++ API (`#1763 <https://github.com/JafarAbdi/moveit/issues/1763>`_)
  * Example to launch C++ interface in a new thread
  * A better multithread example
  Start a new folder, src/cpp_interface_example
  * Update license formatting in new files only
  * JogROSInterface inherits from a base class
  * Base interface class is don
  * The new API half-works  :P
  * Sharing data between threads workks
  * It works! The arm moves
  * Add C++ interface launch file
  * Implement joint commands
  * Debug the demo transition from cartesian to joint commands
  * Add an example of retrieving the current joint state
  * Clang format
  * Satisfy linter re. function names
  * Ensure the library is available to other packages
  * Update license formatting again
  * Clang format
  * Switch pthread to std::thread, change C++14 compiler options
  * Clang format
* Merge `#1773 <https://github.com/JafarAbdi/moveit/issues/1773>`_: Fix compiler warnings
* fix unused parameter warnings
* Update license formatting (`#1764 <https://github.com/JafarAbdi/moveit/issues/1764>`_)
* Unify jog_arm package to be C++14 (`#1762 <https://github.com/JafarAbdi/moveit/issues/1762>`_)
* Fix jog_arm segfault (`#1692 <https://github.com/JafarAbdi/moveit/issues/1692>`_)
  Co-Authored-By: Robert Haschke <rhaschke@users.noreply.github.com>
* Fix double mutex unlock (`#1672 <https://github.com/JafarAbdi/moveit/issues/1672>`_)
* Rename jog_arm->moveit_jog_arm (`#1663 <https://github.com/JafarAbdi/moveit/issues/1663>`_)
  * Rename jog_arm->moveit_jog_arm
  * Address @rhaschke's feedback
  * apply clang-format
* Contributors: AndyZe, Dave Coleman, Henning Kayser, JafarAbdi, Mike Lautman, Robert Haschke
