﻿# PKGBUILDs
##### Package descriptions for the Arch Linux distribution and its spins.

  This is a catalogue of package descriptions with the intent of: patching issues in packages released to the public by the distribution's maintainers, updating packages in the AUR or customising them to better meet my own needs. One has adhered to the Arch packaging standards (https://wiki.archlinux.org/index.php/Arch_packaging_standards) as closely as possible.
  The Arch wiki article on creating packages (https://wiki.archlinux.org/index.php/creating_packages) and the PKGBUILD manual page (https://www.archlinux.org/pacman/PKGBUILD.5.html) should be used as primary references and will answer most questions.

### Table of Contents
* **cadence-git**: Customised AUR recipe for building cadence from the master branch at github. Optional dependencies are clearer and package versioning is more conducive to detecting updates than the AUR package which abuses the epoch variable.
* **carla-git**: Reworked PKGBUILD from the AUR that more accurately represents the software's dependencies and builds the experimental plugins.
* **dstep**: Pseudo-git adaptation of the AUR package tracking the master branch as the available releases fail to build against the tooling currently available via the core Arch Linux repositories.
* **heirloom-cvs**: Package description for the Heirloom Toolchest from the AUR that has been modified to isolate the package's files in a more appropriate, self-contained location: (/opt/heirloom). Pacman doesn't support CVS as a VCS source. Created specialised prepare() function to mimic pacman's behaviour with supported VCS sources. pkgver() added utilising the date fallback as CVS provides no satisfactory method of deriving a package version from the repository data. Package licences were edited to include ALL of the licences the software ships with. ed added as a makedepend as there is a call to it during the build where it will fail if ed is not present.
* **heirloom-devtools-cvs**: Package description for the Heirloom Development Tools from the AUR that has been modified to isolate the package's files ina  more appropriate, self-contained location: (/opt/heirloom). Pacman doesn't support CVS as a VCS source. Created specialised prepare() function to mimic pacman's behaviour with supported VCS sources. pkgver() added utilising the date fallback as CVS provides no satisfactory method of deriving a package version from the repository data. Dependency array was expanded to include gcc-libs. Package licences were edited to include ALL of the licences the software ships with.
* **heirloom-doctools-cvs**: Package description for the Heirloom Documentation Tools that from the AUR has been modified to isolate the package's files in a more appropriate, self-contained location: (/opt/heirloom). Pacman doesn't support CVS as a VCS source. Created specialised prepare() function to mimic pacman's behaviour with supported VCS sources. pkgver() added utilising the date fallback as CVS provides no satisfactory method of deriving a package version from the repository data. Dependency array added including gcc-libs and heirloom-sh-cvs. Package licences were edited to include ALL of the licences the software ships with.
* **heirloom-pkgtools-cvs**: Package description for the Heirloom Packaging Tools from the AUR that has been modified to isolate the package's files in a more appropriate, self-contained location: (/opt/heirloom). Pacman doesn't support CVS as a VCS source. Created specialised prepare() function to mimic pacman's behaviour with supported VCS sources. pkgver() added utilising the date fallback as CVS provides no satisfactory method of deriving a package version from the repository data. Un-fuzzed the patch to mk.config, correcting the placement of VSADMDIR. 
* **heirloom-mailx-cvs**: Package description for Heirloom mailx (previously known as nail) from the AUR that has been modified to isolate the package's files in a more appropriate, self-contained location: (/opt/heirloom). Pacman doesn't support CVS as a VCS source. Created specialised prepare() function to mimic pacman's behaviour with supported VCS sources. pkgver() added utilising the date fallback as CVS provides no satisfactory method of deriving a package version from the repository data. Dependency array was expanded to include krb5 and openssl. Modern versions of OpenSSL have/plan to remove a number of symbols used in the OpenSSL implementation. SSLv2_client_method() and SSLv3_client_method() are the most noteworthy as support for these was dropped after vulnerabilities were discovered that rendered them insecure. These methods have been removed and replaced with comparable counterparts to preserve and extend the original functionality of the software. The manual entry was updated to reflect changes to the values accepted by ssl-method.
* **heirloom-sh-cvs**: Package description for the Heirloom Bourne Shell from the AUR that has been modified to isolate the package's files in more self-contained location: (/opt/heirloom). Pacman doesn't support CVS as a VCS source. Created specialised prepare() function to mimic pacman's behaviour with supported VCS sources. pkgver() added utilising the date fallback as CVS provides no satisfactory method of deriving a package version from the repository data. Dependency array added with glibc as its first entry. Package lacked the opensolaris licence from the source in the final package even though it was declared in the licence array: fixed.
* **ldc**: Updated description to build the current release as this actually compiles against the version of llvm distributed via the Arch Linux Extra repository. Enabled multilib build, including lib32-liblphobos as part of the package split to avoid unnecessarily repeating the build in a separate package.
* **lib32-networkmanager**: Recipe to package 32-bit compatibility libraries that closely mirrors the build provided by the package in Arch's Extra repository.
* **lib32-libxpm**: 32-bit compatibility package based on the libxpm package from the Arch Linux Extra repository modified to include verification of the source via a PGP signature. 
* **libc++**: Updated package description to match the current release of LLVM & clang in Arch Linux's Extra repository.
* **libc++abi**: Updated package description to match the current release of LLVM & clang in Arch Linux's Extra repository. Switched to cmake as the buildit script fails.
* **libjson-rpc-cpp-git**: AUR package description modified to include a more appropriate pkgver function and place the licence in a folder matching the package name.
* **libpng12**: Mirror of the libpng12 package description from the Arch Linux Community repository modified for compatibility with legacy sources as well as binaries. **carla-git** uses this.
* **lumina-desktop**: Tuned variant of the PKGBUILD in AUR that passes the compiler flags from makepkg.conf into qmake.
* **lumina-desktop-git**: Tuned variant of the PKGBUILD in AUR that passes the compiler flags from makepkg.conf into qmake.
