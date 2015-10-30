# recipe-web-service
RESTful web service for managing recipe

# setup
## git clone source code
git clone git@github.com:npu-tiger/recipe-web-service.git

## download and setup maven 2.2.1
- download and unzip http://archive.apache.org/dist/maven/binaries/apache-maven-2.2.1-bin.zip
- set MAVEN_HOME to the path where apache-maven-2.2.1/bin located
- make sure JAVA_HOME is also set
- set both MAVEN_HOME and JAVA_HOME to PATH
- mvn -v to check if maven setup is successful
- also check the reference for help https://maven.apache.org/install.html

## mvn eclipse:eclipse
- at the source code root directory where pom.xml presents, run "mvn eclipse:eclipse" from command line
- the mvn build should be successful

## mysql setup
- download and install mysql
- download and install mysql workbench
- run database schema create script https://github.com/npu-tiger/db-schema/blob/master/recipe_schema_creation.sql
- run user data seed script https://github.com/npu-tiger/db-schema/blob/master/user_data_seed.sql

## start jetty server
- at the source code root directory where pom.xml presents, run "mvn jetty:run"
- "[INFO] Started Jetty Server" should be seen for a successful launch

## test endpoints
- use browser or curl to hit the endpoint:
- http://localhost:8080/recipe/rest/api/users
- http://localhost:8080/recipe/rest/api/users/1
