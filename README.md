# set09119

Software Requirements:

* Latest stable CMake (GUI version helps)
* Visual Studio Community

Project Build Instructions:

* Run CMake
* Set Source Folder to the "code" directory
* Set Build Folder to a directory called "build", under "code" (e.g. /your/path/code/build)
* Run Configure, and just select default compilers, Visual Studio x64 should be the one that appears
* Run Generate
* Now, in the Build folder, you should see the solution file set09119.sln

How to add your own project into the solution, the CMake way

* Copy paste the project you want to work from, into a folder along side the original folder, e.g. /code/02_simulation to /code/02_simulation_v2
* Edit the file /code/CMakeLists.txt and add a "add_subdirectory" line to match the others
* Edit the CMakeLists file in the new folder, e.g. /code/02_simulation_v2/CMakeLists.txt, and search and replace the old project name with the new (e.g. 02_simulation to 02_simulation_v2)
* Re-run configure and generate in CMake

How to add a new source file into your project, the CMake way

* Go to the project's folder
* Create the file
* Edit CMakeLists.txt file and add your file in the appropriate list, if it's .h or .cpp
* In CMake, do Configure and Generate
