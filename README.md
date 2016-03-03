# download eclipse

open <https://www.eclipse.org/downloads/>
![eclipse_homepage](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/eclipse_homepage.png "eclipse_homepage")
![eclipse_download](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/eclipse_download.png "eclipse_download")

download and install eclipse ide (for windows)

download and uncompress eclipse ide (for linux)

>$ cd eclipse-installer

>$ ./eclipse-inst

***
# setup jdk

open <http://www.oracle.com/technetwork/java/javase/downloads/index.html>
![jdk_download](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/jdk_download.png "jdk_download")

install jdk and add the install path to the windows environment 'path' (for windows)

![jdk_path](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/jdk_path.png "jdk_path")

uncompress jdk package and export environments at the end of '.bashrc' (for linux)

>$ sudo mv [jdk_dir] /usr/lib/jvm

>$ gedit ~/.bashrc

    export JAVA_HOME=/usr/lib/jvm
    export JRE_HOME=${JAVA_HOME}/jre
    export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
    export PATH=${JAVA_HOME}/bin:$PATH

***
# install cdt

open <http://www.eclipse.org/cdt/>
![cdt_download](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/cdt_download.png "cdt_download")
![cdt_repository](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/cdt_repository.png "cdt_repository")

input the repository url into eclipse's 'install new software' wizard as instruction
![cdt_install](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/cdt_install.png "cdt_install")
![cdt_config](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/cdt_config.png "cdt_config")

add cmake editor plugin in order to mark cmake keywords
![cmake_editor](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/cmake_editor.png "cmake_editor")

***
# setup catkin

do the catkin make with eclipse build options

>$ cd ~/catkin_ws

>$ catkin_make --force-cmake -G"Eclipse CDT4 - Unix Makefiles" -DCMAKE_BUILD_TYPE=Release

import and config catkin in eclipse
![open_import](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/open_import.png "open_import")
![select_import](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/select_import.png "select_import")
![import_catkin](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/import_catkin.png "import_catkin")
![config_catkin](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/config_catkin.png "config_catkin")
![build_catkin](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/build_catkin.png "build_catkin")

set environment 'PYTHONPATH' (e.g. /opt/ros/indigo/lib/python2.7/dist-packages for indigo)
![pythonpath_environment](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/pythonpath_environment.png "pythonpath_environment")

create terminal inside eclipse and run roscore
![new_terminal](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/new_terminal.png "new_terminal")

>$ roscore

set running configurations and environments
![run_configurations](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/run_configurations.png "run_configurations")
![new_environment](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/new_environment.png "new_environment")
note that the 'ROS_MASTER_URI' should link to roscore (e.g. http://localhost:11311)

remember to set catkin_make option 'DCMAKE_BUILD_TYPE' to 'Debug' in terminal if running debug

>$ cd ~/catkin_ws

>$ catkin_make --force-cmake -G"Eclipse CDT4 - Unix Makefiles" -DCMAKE_BUILD_TYPE=Debug

![run_debug](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/run_debug.png "run_debug")

remember to set catkin_make option 'DCMAKE_BUILD_TYPE' to 'Release' in terminal if running release
