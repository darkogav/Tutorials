# Tutorials

###How To Install Setup Minecraft Forge on Linux###

This tutorial is based on a Debian wheezy installation, but it should work with any other Linux system. 

* Download the latest version of Oracle Java JRE. Download the tar.gz file version.
* Download and install java-package
* edit `/usr/share/java-package/oracle-j2re.sh`
  * add 
`
        "jre-8u"[0-9][0-9]"-linux-i586.tar.gz") # SUPPORTED
            j2se_version=1.8.0+update${archive_name:6:2}${revision}
            j2se_expected_min_size=94 #Mb
            j2se_priority=316
            found=true
            ;;
`

* make the Java package
* `make-jpkg jre-8u77-linux-i586.tar.gz` #confirmed working as on 3/26/2016 on Wheezy#
* download forge-1.8.9-11.15.1.1722-installer.jar
* run the installer
`java -jar forge-1.8.9-11.15.1.1722-installer.jar --installServer`
* edit eula.txt set `eula=true`
* java -Xmx2G -Xms2G -jar forge-1.8.9-11.15.1.1722-universal.jar
* Login to server.
