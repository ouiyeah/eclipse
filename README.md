# download eclipse

open <https://www.eclipse.org/downloads/>
![eclipse_homepage](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/eclipse_homepage.png "eclipse_homepage")

download and uncompress eclipse ide
![eclipse_download](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/eclipse_download.png "eclipse_download")

***
# setup jdk

open <http://www.oracle.com/technetwork/java/javase/downloads/index.html>
![jdk_download](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/jdk_download.png "jdk_download")

install jdk and add the install path to the windows environment 'path' (for windows)
![jdk_path](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/jdk_path.png "jdk_path")

uncompress jdk package and source environments (for linux)

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
![c dt_repository](https://raw.githubusercontent.com/ouiyeah/eclipse/master/img/cdt_repository.png "cdt_repository")
input the repository url into eclipse's 'install new software' item as the instruction
