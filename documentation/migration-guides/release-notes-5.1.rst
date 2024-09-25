.. SPDX-License-Identifier: CC-BY-SA-2.0-UK

Release notes for 5.1 (styhead)
---------------------------------

New Features / Enhancements in 5.1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Linux kernel 6.X, gcc 14.X, glibc 2.X, LLVM 18.X, and over XXX other recipe upgrades

-  New variables:

   - :term:`CVE_CHECK_MANIFEST_JSON_SUFFIX`: suffix for the CVE JSON manifest file.

   - :term:`PRSERVER_UPSTREAM`: Upstream PR service (host:port).

   - :term:`RECIPE_UPGRADE_EXTRA_TASKS`: space-delimited list of tasks to run after the new
     sources have been unpacked in scripts/lib/devtool/upgrade.py ugrade() method.

   - :term:`UNPACKDIR`: allow change of do_unpack directory.

-  Architecture-specific enhancements:

-  Kernel-related enhancements:

-  New core recipes:

   -  `fmt <https://fmt.dev>`__: an open-source formatting library for C++. (from meta-oe)

   -  `xcb-util-errors <http://xcb.freedesktop.org/XcbUtil/>`__: gives human readable
      names to error codes and event codes

-  QEMU / ``runqemu`` enhancements:

   - runqemu: :term:`QB_DRIVE_TYPE` now support for sd card (/dev/mmcblk)

-  Rust improvements:

-  SDK-related improvements:

-  Testing:

   -  Enable ptests for ``python3-cffi``, ``python3-idna``, ``python3-libarchive-c``,
      ``python3-mako``, ``python3-packaging``, ``python3-uritools`` and ``pythonn3-rpds-py``.

-  Utility script changes:

   -  New ``cve-json-to-text`` script that converts the cve-check result from the JSON format
      to the TEXT format as cve-check removed text format.

   -  New ``makefile-getvar`` script to extract value from a Makefile.

   -  New ``pull-spdx-licenses`` script to pull SPDX license data, update license list JSON
      data and update license directory.

   -  Several improvement in ``oe-build-perf-report`` report.

   -  ``oe-debuginfod`` add parameter "-d" to store debuginfod files in project sub-directory.

   -  ``resulttool`` support test report generation in JUnit XML format.


-  BitBake improvements:

   -  New go module fetcher (``gomod://``) for downloading module dependencies to the
      module cache from a module proxy.

   -  New go module fetcher (``gomodgit://``) for downloading module dependencies to the
      module cache directly from a git repository.

   -  Crate added check for latest upstream version.

   -  Syncrpc required a minimum version of the websockets module depend on python version.

   -  Improved bitbake-hashclient stress statistics reporting.

   -  bitbake-hashserv added ``reuseport`` parameter to enable SO_REUSEPORT, allowing
      multiple servers to bind to the same port for load balancing

   -  improved cloning speed with :term:`BB_GIT_SHALLOW` and :term:`BB_GENERATE_MIRROR_TARBALLS`.

   -  bitbake UI now include log paths for failed task.

   -  fetcher2 support for wget and wget2.

   -  fetcher2 support npm package name with '@' character.

   -  Codeparser now support shell substitution in quotes, for example::

         var1="$(cmd1 ...)"

-  devtool improvements:

-  recipetool improvements:

-  Packaging changes:

-  Security improvements:

   -  Improved with status information for each CVE under analysis.

-  Toaster Web UI improvements:

-  Prominent documentation updates:

-  Miscellaneous changes:

   -  Update to SPDX license version 3.24.0

   -  New :ref:`create-spdx-3.0` class to generate SPDX 3.0 output, :ref:`create-spdx-image-3.0`
      class that is used when generating images and :ref:`create-spdx-sdk-3.0` for sdk
      based recipes.

   -  New :ref:`nospdx` class that allows recipes to opt out of generating SPDX.

   -  New :ref:`Vex` class generates the minimum information that is necessary
      for VEX generation by an external CVE checking tool.

   -  New :ref:`retain` class creates a tarball of the work directory for a recipe
      when one of its tasks fails, or any other nominated directories.

   -  New :ref:`localpkgfeed` class create a subset of the package feed that just
      contain the packages depended on by this recipe.

   -  New :term:`PACKAGECONFIG` options for individual recipes:

      - appstream: qt6
      - cronie: inotify
      - gstreamer1.0-plugins-bad: gtk3
      - libsdl2: libsamplerate
      - mesa: tegra
      - pciutils: kmod zlib
      - piglit: wayland
      - pulseaudio: oss-output
      - python3: staticlibpython
      - python3-jsonschema: format-nongpl (previously "nongpl")
      - systemd: bpf-framework
      - util-linux: libmount-mountfd-support

   -  Stop referring :term:`WORKDIR` for :term:`S` and :term:`B`.

Known Issues in 5.1
~~~~~~~~~~~~~~~~~~~

Recipe License changes in 5.1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The following corrections have been made to the :term:`LICENSE` values set by recipes:

-  ``dejagnu``: update :term:`LICENSE` to ``GPL-3.0-only``.
-  ``gcr``: update :term:`LICENSE` to ``LGPL-2.0-only``.
-  ``glibc``: update :term:`LICENSE` to ``GPL-2.0-only & LGPL-2.1-or-later``.
-  ``gpgme``: update :term:`LICENSE` for different packages.
-  ``linux-firmware``: separate license ``Firmware-linaro`` for linaro-license package.
-  ``iw``: update :term:`LICENSE` to ``ISC``.
-  ``ppp``: add license ``RSA-MD`` .
-  ``tiff``: update :term:`LICENSE` to ``libtiff``.
-  ``unzip``: update :term:`LICENSE` to ``Info-ZIP``.
-  ``xz``: add :term:`LICENSE` ``PD`` for xz, xz-dev and xz-doc package.
-  ``zip``: update :term:`LICENSE` to ``Info-ZIP``.


Security Fixes in 5.1
~~~~~~~~~~~~~~~~~~~~~

Recipe Upgrades in 5.1
~~~~~~~~~~~~~~~~~~~~~~

Contributors to 5.1
~~~~~~~~~~~~~~~~~~~

Thanks to the following people who contributed to this release:

Repositories / Downloads for Yocto-5.1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
