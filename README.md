# recipe-web-service
RESTful web service for managing recipe

# setup
## git clone source code
git clone git@github.com:npu-tiger/recipe-web-service.git

## download and setup maven 3.0.4
- download and unzip http://archive.apache.org/dist/maven/maven-3/3.0.4/binaries/apache-maven-3.0.4-bin.zip
- set MAVEN_HOME to the path where apache-maven-3.0.4/bin located
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
- run recipe data seed script https://github.com/npu-tiger/db-schema/blob/master/recipe_data_seed.sql
- run rank data seed script https://github.com/npu-tiger/db-schema/blob/master/rank_data_seed.sql

## start jetty server
- at the source code root directory where pom.xml presents, run "mvn jetty:run"
- "[INFO] Started Jetty Server" should be seen for a successful launch

## test endpoints
- use browser or curl to hit the endpoint: http://localhost:8080/recipe/rest/api
- if you see "welcome to recipe!" then your web service is running fine

# User Resource
## GET - get all
http://localhost:8080/recipe/rest/api/users

## GET - get by id
GET: http://localhost:8080/recipe/rest/api/users/1

## POST: create user
http://localhost:8080/recipe/rest/api/users
sample request payload for post: {"id":null,"username":"dummyuser1","password":"password123","email":"dummyuser1@recipe.com","nickname":"fun"}

# reference
http://www.eclipse.org/jetty/documentation/current/jetty-maven-plugin.html
