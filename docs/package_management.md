* **Package Management in Linux:**
    
      
  1. One of the most important function of any linux distribution is package management. Originally, most linux distributions like slackware were simply collections of tarball - 
     that is archives of either binaries or sources which needed to be compiled in order to install various applications and other system services etc.
  2. However, this method has many disadvantages:
  
       1. Removing all files from a package can be difficult.
       2. A developer may lose a track of what exact sources were used to build a particular binary packages.
       3. One might accidentally delete a package that other packages need or install a package that will not work because it needs other packages that have not been installed.
       4. Updates and upgrades can be very difficult for a number of reasons. If you do upgrade while the system is running, you can get all sorts of critical problems, even a crash. The order of upgrading packages might also be important.

  3. RPM Creation:

        The RPM packaging system separates its main functionality methods using two main programs:

        * rpm: Handles querying, installing, upgrading and erasing.
        * rpmbuild: Handles creating and manipulating source and binary packages.

        There are three basic ingredients required to assemble the source and binary packages:

        * A tarball file containing all source code, makefiles, default configuration files, documentation, etc.
        * Any patch files needed to be applied to the upstream source encapsulated in the tarball.
        * A spec file that must be written that describes the package and how to patch and build it, dependency information, etc.

        The RPM spec File:

        * A spec file is a collection of package information and shell scripts. Many of of the shell scripts are very short (one line scripts are common). Each script performs one           of the tasks necessary in building, installing, or uninstalling a package. 

