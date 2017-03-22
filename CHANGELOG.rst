^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package serial
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.2.2 (2017-03-22)
------------------
* Fix issue with write() and a timeout of 0. (`#137 <https://github.com/wjwwood/serial/issues/137>`_)
  * Fix issue with write() and a timeout of 0.
  * fix up style
* Update documentation (`#140 <https://github.com/wjwwood/serial/issues/140>`_)
  * Fix typo and missing dependency in README
  * [docs] Update docs: fix deprecation warnings + add missing deps to README
* fixing unix timeouts handling ("timer_tests.short_interval" failure) (`#147 <https://github.com/wjwwood/serial/issues/147>`_)
* fix timeouts handling on Unix systems (`#142 <https://github.com/wjwwood/serial/issues/142>`_)
  fixed "singed long" overflow that took place on attempt
  to use ~3000ms or bigger timeouts on Unix systems
* resource leak if exception in SerialImpl constructor (`#146 <https://github.com/wjwwood/serial/issues/146>`_)
* Const corrections. (`#141 <https://github.com/wjwwood/serial/issues/141>`_)
* Merge pull request `#118 <https://github.com/wjwwood/serial/issues/118>`_ from Rimco/patch-1
  Updated serial.cc for FreeBSD 9 compatibility.
* Updated serial.cc for FreeBSD 9 compatibility.
* Merge pull request `#116 <https://github.com/wjwwood/serial/issues/116>`_ from pao/patch-1
  Use CLOCK_MONOTONIC (Linux)/SYSTEM_CLOCK (OS X) to time select()
* on OS X, use SYSTEM_CLOCK, not CALENDAR_CLOCK
  Analogously to using `CLOCK_MONOTONIC` on Linux to time events in favor of `CLOCK_REALTIME`, `SYSTEM_CLOCK` should be used in favor of `CALENDAR_CLOCK` on OS X.
  Ref: http://stackoverflow.com/questions/11680461/monotonic-clock-on-osx
* on Linux, use CLOCK_MONOTONIC for clock_gettime()
  On Linux systems which are being driven by an external time source (NTP or PTP), it is possible that time appears to slew in reverse under `CLOCK_REALTIME`. Since the timer function is used to time durations of events (calls to `select()`), it is better to use `CLOCK_MONOTONIC`, which isn't subject to slewing.
* Merge pull request `#113 <https://github.com/wjwwood/serial/issues/113>`_ from vladimirgamalian/patch-1
  Comment unreferenced formal parameters
* Comment unreferenced formal parameter
  Fix warning from static analysis tools.
* Merge pull request `#112 <https://github.com/wjwwood/serial/issues/112>`_ from linquize/vs2015
  Support VS2015
* Can use the toolsets from Visual Studio 2010, 2012, 2013, 2015
* Merge pull request `#106 <https://github.com/wjwwood/serial/issues/106>`_ from ramirahikkala/master
  AdditionalIncludeDirectories must be relative for project not solution
* AdditionalIncludeDirectories must be relative for project not solution
  Fixes `#105 <https://github.com/wjwwood/serial/issues/105>`_
  Signed-off-by: Rami <rami.rahikkala@jotautomation.com>
* Merge pull request `#103 <https://github.com/wjwwood/serial/issues/103>`_ from drummist180/master
  Fix include directory paths in Visual Studio projects.
* Fix include directory paths in Visual Studio projects.
  Remove previously ignored *.user file.
* Merge pull request `#98 <https://github.com/wjwwood/serial/issues/98>`_ from wjwwood/fix_issue_97
  fix warning on Windows
* fix warning on Windows
* Contributors: Brandon Morton, Christopher Baker, Linquize, Patrick O'Leary, Rami, Rimco, Stephane Poirier, Vladimir Gamalian, William Woodall, aleksey-sergey, dontsovcmc, rhd

* Fix issue with write() and a timeout of 0. (`#137 <https://github.com/wjwwood/serial/issues/137>`_)
  * Fix issue with write() and a timeout of 0.
  * fix up style
* Update documentation (`#140 <https://github.com/wjwwood/serial/issues/140>`_)
  * Fix typo and missing dependency in README
  * [docs] Update docs: fix deprecation warnings + add missing deps to README
* fixing unix timeouts handling ("timer_tests.short_interval" failure) (`#147 <https://github.com/wjwwood/serial/issues/147>`_)
* fix timeouts handling on Unix systems (`#142 <https://github.com/wjwwood/serial/issues/142>`_)
  fixed "singed long" overflow that took place on attempt
  to use ~3000ms or bigger timeouts on Unix systems
* resource leak if exception in SerialImpl constructor (`#146 <https://github.com/wjwwood/serial/issues/146>`_)
* Const corrections. (`#141 <https://github.com/wjwwood/serial/issues/141>`_)
* Merge pull request `#118 <https://github.com/wjwwood/serial/issues/118>`_ from Rimco/patch-1
  Updated serial.cc for FreeBSD 9 compatibility.
* Updated serial.cc for FreeBSD 9 compatibility.
* Merge pull request `#116 <https://github.com/wjwwood/serial/issues/116>`_ from pao/patch-1
  Use CLOCK_MONOTONIC (Linux)/SYSTEM_CLOCK (OS X) to time select()
* on OS X, use SYSTEM_CLOCK, not CALENDAR_CLOCK
  Analogously to using `CLOCK_MONOTONIC` on Linux to time events in favor of `CLOCK_REALTIME`, `SYSTEM_CLOCK` should be used in favor of `CALENDAR_CLOCK` on OS X.
  Ref: http://stackoverflow.com/questions/11680461/monotonic-clock-on-osx
* on Linux, use CLOCK_MONOTONIC for clock_gettime()
  On Linux systems which are being driven by an external time source (NTP or PTP), it is possible that time appears to slew in reverse under `CLOCK_REALTIME`. Since the timer function is used to time durations of events (calls to `select()`), it is better to use `CLOCK_MONOTONIC`, which isn't subject to slewing.
* Merge pull request `#113 <https://github.com/wjwwood/serial/issues/113>`_ from vladimirgamalian/patch-1
  Comment unreferenced formal parameters
* Comment unreferenced formal parameter
  Fix warning from static analysis tools.
* Merge pull request `#112 <https://github.com/wjwwood/serial/issues/112>`_ from linquize/vs2015
  Support VS2015
* Can use the toolsets from Visual Studio 2010, 2012, 2013, 2015
* Merge pull request `#106 <https://github.com/wjwwood/serial/issues/106>`_ from ramirahikkala/master
  AdditionalIncludeDirectories must be relative for project not solution
* AdditionalIncludeDirectories must be relative for project not solution
  Fixes `#105 <https://github.com/wjwwood/serial/issues/105>`_
  Signed-off-by: Rami <rami.rahikkala@jotautomation.com>
* Merge pull request `#103 <https://github.com/wjwwood/serial/issues/103>`_ from drummist180/master
  Fix include directory paths in Visual Studio projects.
* Fix include directory paths in Visual Studio projects.
  Remove previously ignored *.user file.
* Merge pull request `#98 <https://github.com/wjwwood/serial/issues/98>`_ from wjwwood/fix_issue_97
  fix warning on Windows
* fix warning on Windows
* Contributors: Brandon Morton, Christopher Baker, Linquize, Patrick O'Leary, Rami, Rimco, Stephane Poirier, Vladimir Gamalian, William Woodall, aleksey-sergey, dontsovcmc, rhd

1.2.1 (2015-04-21)
------------------
* Removed the use of a C++11 feature for compatibility with older browsers.
* Fixed an issue with cross compiling with mingw on Windows.
* Restructured Visual Studio project layout.
* Added include of ``#include <AvailabilityMacros.h>`` on OS X (listing of ports).
* Fixed MXE for the listing of ports on Windows.
* Now closes file device if ``reconfigureDevice`` fails (Windows).
* Added the MARK/SPACE parity bit option, also made it optional.
  Adding the enumeration values for MARK and SPACE was the only code change to an API header.
  It should not affect ABI or API.
* Added support for 576000 baud on Linux.
* Now releases iterator properly in listing of ports code for OS X.
* Fixed the ability to open COM ports over COM10 on Windows.
* Fixed up some documentation about exceptions in ``serial.h``.

1.2.0 (2014-07-02)
------------------
* Removed vestigial ``read_cache_`` private member variable from Serial::Serial
* Fixed usage of scoped locks
  Previously they were getting destroyed immediately because they were not stored in a temporary scope variable
* Added check of return value from close in Serial::SerialImpl::close () in unix.cc and win.cc
* Added ability to enumerate ports on linux and windows.
  Updated serial_example.cc to show example of port enumeration.
* Fixed compile on VS2013
* Added functions ``waitReadable`` and ``waitByteTimes`` with implemenations for Unix to support high performance reading
* Contributors: Christopher Baker, Craig Lilley, Konstantina Kastanara, Mike Purvis, William Woodall

1.1.7 (2014-02-20)
------------------
* Improved support for mingw (mxe.cc)
* Fix compilation warning
  See issue `#53 <https://github.com/wjwwood/serial/issues/53>`_
* Improved timer handling in unix implementation
* fix broken ifdef _WIN32
* Fix broken ioctl calls, add exception handling.
* Code guards for platform-specific implementations. (when not using cmake / catkin)
* Contributors: Christopher Baker, Mike Purvis, Nicolas Bigaouette, William Woodall, dawid

1.1.6 (2013-10-17)
------------------
* Move stopbits_one_point_five to the end of the enum, so that it doesn't alias with stopbits_two.

1.1.5 (2013-09-23)
------------------
* Fix license labeling, I put BSD, but the license has always been MIT...
* Added Microsoft Visual Studio 2010 project to make compiling on Windows easier.
* Implemented Serial::available() for Windows
* Update how custom baudrates are handled on OS X
  This is taken from the example serial program on Apple's developer website, see:
  http://free-pascal-general.1045716.n5.nabble.com/Non-standard-baud-rates-in-OS-X-IOSSIOSPEED-IOCTL-td4699923.html
* Timout settings are now applied by reconfigurePort
* Pass LPCWSTR to CreateFile in Windows impl
* Use wstring for ``port_`` type in Windows impl

1.1.4 (2013-06-12 00:13:18 -0600)
---------------------------------
* Timing calculation fix for read and write.
  Fixes `#27 <https://github.com/wjwwood/serial/issues/27>`_
* Update list of exceptions thrown from constructor.
* fix, by Thomas Hoppe <thomas.hoppe@cesys.com>
  For SerialException's:
  * The name was misspelled...
  * Use std::string's for error messages to prevent corruption of messages on some platforms
* alloca.h does not exist on OpenBSD either.

1.1.3 (2013-01-09 10:54:34 -0800)
---------------------------------
* Install headers

1.1.2 (2012-12-14 14:08:55 -0800)
---------------------------------
* Fix buildtool depends

1.1.1 (2012-12-03)
------------------
* Removed rt linking on OS X. Fixes `#24 <https://github.com/wjwwood/serial/issues/24>`_.

1.1.0 (2012-10-24)
------------------
* Previous history is unstructured and therefore has been truncated. See the commit messages for more info.
