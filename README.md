#maven

Example of maven project. Below are some instructions.

=== INSTALLING MAVEN FROM TERMINAL (MAC) ===

Download and install maven from https://maven.apache.org/download.cgi.

You then need to set your home variables, so maven knows where it can drop and get its stuff.

To do this, first open your terminal and type "vim ~/.bash_profile". This takes you to the bash environment where you can set your home variables. 

Then type "i" for insertion mode, so that you can type stuff.

Go to new line somewhere, and type "M2_HOME=[directory], where "directory" is the directory where you have installed maven. Then type "PATH=$PATH:$M2_HOME/bin". This sets your home variables.

Hit "esc" and type ":x" to save and quit the bash mode.

This completes the installation. 

Restart the terminal, and type "mvn -version" to check whether it worked. You should get the version of maven that is installed on your computer.

=== CREATING A NEW MAVEN PROJECT ===

In the terminal, go to the root directory where you want your new maven project, and type the following: 

"mvn archetype:generate -DgroupId=[groupId] -DartifactId=[artifactId] -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false"

The "groupId" is the name of the package for your maven project (e.g., "com.somecompany.someprojectname") and the "artifactId" is then name of the project, usually the last part of the packagename (in this case, "someprojectname").

=== BUILD, TEST, RUN ===

To build your project, type "mvn clean package" [in the root directory of the project].

To test your project, type "mvn test" [in the root directory of the project].

To run your project, type "mvn exec:java -Dexec.mainClass=[package].[class]", whereby "package" is the name of the package (e.g., "com.somecompany.someprojectname") and "class" is the name of the class with the main method.