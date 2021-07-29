# Mule 4 application archetype example

This is a Maven archetype example for Mule 4 application. This archetype contains:
-   pom.xml with predefined dependencies
-   global configuration file
-   basic raml definition for the API
-   yaml file with application properties
-   basic flow implementation with functioning health endpoint


## Installation

Clone this repository and run `mvn install` command to install this archetype.

## Generating new application

To generate a new application using this archetype simply run the command:

```
mvn archetype:generate -DarchetypeGroupId=com.example -DarchetypeArtifactId=mule4-archetype-example -DgroupId=<groupId> -DartifactId=<artifactId> -Dversion=<version> -DapiArtifactId=<api_artifactId> -DappName=<app_name> -DapiName=<api_name> -DapiHost=<api_host> -DapiBasepath=<api_basepath> -DinteractiveMode=false
```

Parameters:
 - **groupId** - your application groupId (used in pom.xml)
 - **artifactId** - your application artifactId (used in pom.xml)
 - **version** - your application version (used in pom.xml)
 - **api_artifactId** - your API artifactId (used as file name for API raml)
 - **app_name** - your application name (used as a name for API and API Console flows names)
 - **api_name** - your API name (used as a title in API raml definition)
 - **api_host** - your API host (used as a part of baseUri in API raml definition)
 - **api_basepath** - your API basepath (used in HTTP Listener configuration and as a part of baseUri in API raml definition)

Example:

```
mvn archetype:generate -DarchetypeGroupId=com.example -DarchetypeArtifactId=mule4-archetype-example -DgroupId=com.example -DartifactId=my-mule4-app -Dversion=1.0.0 -DapiArtifactId=example-api -DappName=exampleMuleApp -DapiName="API Example" -DapiHost=myapi.com -DapiBasepath=/api/v1 -DinteractiveMode=false
```
