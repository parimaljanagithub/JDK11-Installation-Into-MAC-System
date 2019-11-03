# JDK11-Installation-Into-MAC-System
# Abstruction: 
 This document content the information about how to install JDK11 into mac system and switching between different system.
 
 # Install JDK 11:
 Step 1:
 go to below link and download latest JDK 11 version ( during this documentation current version is 11.0.5)
 
 https://www.oracle.com/technetwork/java/javase/downloads/index.html
 Step 2:go to your download folder and extract the file using below command
        tar xf jdk-11.0.5_osx-x64_bin.tar.gz
  
 Step 3: Move the file to java installation directory(i.e /Library/Java/JavaVirtualMachines)
         sudo mv jdk-11.0.5.jdk /Library/Java/JavaVirtualMachines
         
 Step 4: now the installation is completed and you can check the Java version using below command
         java -version  output = java version "11.0.5" 2019-10-15 LTS
         
 Step 5: List out all the java version installed in your computer
         /usr/libexec/java_home -V 
         output :
         Matching Java Virtual Machines (2):
            11.0.5, x86_64:	"Java SE 11.0.5"	/Library/Java/JavaVirtualMachines/jdk-11.0.5.jdk/Contents/Home
            1.8.0_181, x86_64:	"Java SE 8"	/Library/Java/JavaVirtualMachines/jdk1.8.0_181.jdk/Contents/Home
         In my system two Java version are intalled thats why in result two version are visible
         if you want to know the location where current java is installed then run the below command
         /usr/libexec/java_home -v
         
 Step 6: switching between different java version
         export JAVA_8_HOME=$(/usr/libexec/java_home -v1.8)
         java8='export JAVA_HOME=$JAVA_8_HOME'
         JAVA_11_HOME=$(/usr/libexec/java_home -v11)
         java11='export JAVA_HOME=$JAVA_11_HOME'
          run below command :
         java8
         java -version   output: java version "1.8.0_181"
         java11
         java -version    output: java version "1.8.0_181"
 
