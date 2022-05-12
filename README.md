## app-development-parent-pom

## This pom includes following plugins
    * maven-compiler-plugin to build and compile in respective java version
    * maven-enforcer-plugin to enforce proper jave and maven versions are used
    * maven-checkstyle-plugin(with google checkstyle) 
    * git-code-format-maven-plugin  used to autoformat code at git commit and also to verify the code format at mvn verify
    * jacoco-maven-plugin to generate test report . this report could be used by sonarqube etc 
    * openapi-generator-maven-plugin to generate openapi server code(spring)

## TODO
    Add owasp dependency-check-maven plugin
    Add sonar-maven-plugin
    Add enforcement of junit5 using maven-enforcer-plugin 
    Exclude scanning of generated source folder from spotbugs plugin
    Finalize the configuration and verify generation of client code by openapi-generator-maven-plugin
    replace spring-boot-starter-parent dependency with spring-boot bom 
    Add pitest mutation with its maven plugin
