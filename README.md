spring-tomcat
=============

Deploying spring web application on tomcat directly as we do any other web application

1) Download maven plugin for eclipse. My eclipse version was Juno so I downloaded m2e-wtp for eclipse from help --> Eclipse marketplace

2) Running a spring application in eclipse needs proper import of maven project if it is existing in source version control. 
   The above statement can be confusing as their can be many folders. The general structure of maven, spring project would be of structure
   
   spring-proj
        |--------src
        |         |---------main
        |         |--------test
        |         |---------target
        |
        |-------other folders needed
        |-------pom.xml 
        
pom.xml's parent directory should be imported into eclipse as maven project otherwise it wouldn't be recognised as maven project

3) After importing the project make a build using maven install command

4) mvn install command copies all the classes and files to target folder

5) Now right click on project properties, click on deployment assembly assign the folder where all the classes and files are created. 
  For example if the pom.xml has a command to create xyz-abc then all the classes are copied into that folder. 
6) After configuring deployment assembly in properties enable maven repo jars by clicking on add button and selecting java dependencies. 

7) If they are not available then you need to right click on project ----> Maven -----> Update project and repeat step 6

8) Deploy your webapp in tomcat. You can setup debug easily without remote debugging. 


