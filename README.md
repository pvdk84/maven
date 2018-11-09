Example of maven project. See instructions below:

=== INSTALLING MAVEN FROM TERMINAL (MAC) ===

download and install maven: 
https://maven.apache.org/download.cgi

open terminal

type "vim ~/.bash_profile" to go to environment variables

type "i" for insertion mode

go to new line somewhere

type "M2_HOME=[directory where you have installed maven, or simply drag and drop]

type "PATH=$PATH:$M2_HOME/bin

hit "esc"

type ":x" to save and quit, or ":q" to just quit

restart the terminal

type "mvn -version" to check

=== CREATE A NEW MAVEN PROJECT ===

go to the root directory where you want your new maven project

type "mvn archetype:generate -DgroupId=[package] -DartifactId=[usually last part of package] -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false"

=== BUILD, TEST, RUN ===

to build your project, type "mvn clean package" [in the root directory of the project]

to test your project, type "mvn test" [in the root directory of the project]

to run your project, type "mvn exec:java -Dexec.mainClass=[project package].[class with main]"