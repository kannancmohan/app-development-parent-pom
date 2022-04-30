## app-development-parent-pom

## This pom includes following plugins
    * maven-compiler-plugin to build and compile in respective java version
    * maven-enforcer-plugin to enforce proper jave and maven versions are used
    * maven-checkstyle-plugin(with google checkstyle) 
    * git-code-format-maven-plugin to format code with google java format
    * jacoco-maven-plugin to generate test report . this report could be used by sonarqube etc 
    * openapi-generator-maven-plugin to generate openapi server code(spring)
