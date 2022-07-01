## app-development-parent-pom

parent pom that supports building spring-boot based applications

## supported versions
    java - 17
    maven 3.5.4+
    spring-boot 2.7.0
    spring-cloud-stream 3.2.3
    spring-cloud-aws 2.4.1

## This pom includes following dependencies

## This pom includes following plugins

    * maven-compiler-plugin: to build and compile in respective java version
    * maven-enforcer-plugin: to enforce proper jave, maven versions and other compliances
    * maven-checkstyle-plugin(with google checkstyle): does checkstyle analysis on code 
        - for manula code formatting use 'mvn git-code-format:format-code'
    * git-code-format-maven-plugin:  used to autoformat code at git commit and also to verify the code format at mvn verify
    * jacoco-maven-plugin: to generate test report . this report could be used by sonarqube etc 
    * openapi-generator-maven-plugin: to generate openapi server code(spring)
        - plugin to generate openapi server code(spring)
        - plugin to generate openapi client code(java)
        please note that the openapi-generator doesnt supports open-api version 3.1.0+ yet,so the api spec version should be 3.0.3 until openapi-generator support it(https://github.com/OpenAPITools/openapi-generator/issues/9083)
    * spotbugs-maven-plugin: SpotBugs looks for bugs in Java programs
    * arch-unit-maven-plugin: enables you to make sure that your projects follow the same architecture rules
        check project app-development-archunit-rule for custom archunit rules
    * maven-dependency-plugin: used to unpack shared resources to project 
    * owasp dependency-check-maven: to check vulnerabilities contained within a project dependencies

## TODO
    Add sonar-maven-plugin
    Add enforcement of junit5 using maven-enforcer-plugin 
    Exclude scanning of generated source folder from spotbugs plugin
    Finalize the configuration and verify generation of client code by openapi-generator-maven-plugin
    replace spring-boot-starter-parent dependency with spring-boot bom 
    Add pitest mutation with its maven plugin
