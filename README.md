﻿# PKGBUILDs
##### Package descriptions for the Arch Linux distribution and its spins.

  This is a catalogue of package descriptions with the intent of: patching issues in packages released to the public by the distribution's maintainers, updating packages in the AUR or customizing them to better meet my own needs. One has adhered to the Arch packaging standards (https://wiki.archlinux.org/index.php/Arch_packaging_standards) as closely as possible.
  The Arch wiki article on creating packages (https://wiki.archlinux.org/index.php/creating_packages) and the PKGBUILD manual page (https://www.archlinux.org/pacman/PKGBUILD.5.html) should be used as primary references and will answer most questions.

### Table of Contents
* **cadence-git**: Customized recipe for building cadence from the master branch at github. Optional dependencies are clearer and package versioning is more conducive to detecting updates than the AUR package which abuses the epoch variable.
* **carla-git**: Reworked PKGBUILD from the AUR that more accurately represents the software's dependencies.
* **cpp-ethereum-git**:
* **heirloom-cvs**: Package description for the Heirloom Toolchest that has been modified to isolate the package's files in more self-contained location: (/opt/heirloom). pkgver() added utilizing the date fallback as CVS provides no satisfactory method of deriving a package version from the repository data. Package licences were edited to include ALL of the licences the software ships with. ed added as a makedepend as there is a call to it during the build where it will fail if ed is not present.
* **heirloom-devtools-cvs**: Package description for the Heirloom Development Tools that has been modified to isolate the package's files in more self-contained location: (/opt/heirloom). pkgver() added utilizing the date fallback as CVS provides no satisfactory method of deriving a package version from the repository data. Dependency array was expanded to include gcc-libs. Package licences were edited to include ALL of the licences the software ships with.
* **heirloom-doctools-cvs**: Package description for the Heirloom Documentation Tools that has been modified to isolate the package's files in more self-contained location: (/opt/heirloom). pkgver() added utilizing the date fallback as CVS provides no satisfactory method of deriving a package version from the repository data. Dependency array added including gcc-libs and heirloom-sh-cvs. Package licences were edited to include ALL of the licences the software ships with.
* **heirloom-sh-cvs**: Package description for the Heirloom Bourne Shell that has been modified to isolate the package's files in more self-contained location: (/opt/heirloom). pkgver() added utilizing the date fallback as CVS provides no satisfactory method of deriving a package version from the repository data. Dependency array added with glibc as its first entry. Package lacked the opensolaris licence from the source in the final package even though it was declared in the licence array: fixed.
* **lib32-libnm-glib**: Recipe to package 32-bit compatibility library that closely mirrors the build provided by the package in Arch's Extra repository. 
* **libjson-rpc-cpp-git**: Modified package description to include a more appropriate pkgver funciton and place the licence in a folder matching the package name.
* **mist**:
