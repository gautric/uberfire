##Deploy on Tomcat
This guide will help you install an UberFire demo application on your own computer. This will help let you try out an UberFire application in Tomcat, and prove the UberFire apps work with your setup.

##Building our App
This demo will be based on UF tasks app from previous section. If you didn't work through the tutorial and build this App, feel free to download it and build it from source code:

```
git clone https://github.com/uberfire/uberfire-tutorial.git
cd uftasks
mvn clean install
```
##Get an app server
UFTasks was generated from Uberfire Archetype. So inside uftasks-showcase, there is a directory called uftasks-distributions-wars that has, inside its target directory, WAR files for JBoss EAP 6.4, Tomcat 7.0 and Wildfly 8.1. Let's install this app on Tomcat 7.0.

If you don't already have Tomcat 7.0 installed on your computer, you can [download](http://tomcat.apache.org/download-70.cgi) and install it. Installing is as easy as downloading and unzipping.

##Start the app server
Now start the app server using a command line terminal. Use the cd command to change the working directory of your terminal to the place where you unzipped the application server, then execute one of the following commands, based on your operating system and choice of app server:

| *nix, Mac OS X | Windows |
| -- | -- |
| bin/startup.sh | bin\startup.bat |

Then point your favorite web browser to the URL http://localhost:8080/ and you should see a webpage confirming that the app server is running.

##Deploy the WAR
Rename the UFtasks tomcat WAR file to uftasks.war and copy it into the auto-deployment directory for your app server. For example on Unix/Linux/Mac:
```
mv uftasks-showcase-1.0-SNAPSHOT-tomcat7.0.war /~/bin/apache-tomcat-7.0.57/webapps/uftasks.war
```
##See it work!
Now visit http://localhost:8080/uftasks/ and sign in with username admin, password admin.

