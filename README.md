# SonarQube_NOTES

install sonarqube and sonar-scanner
goto the root project diretory and make a new file = sonar-project.properties file

#########################
paste this code =
# must be unique in a given SonarQube instance
sonar.projectKey=my:projectName

sonar.sources=src/main/java

# Exclude test classes from the analysis
sonar.exclusions=src/test/java/**/*.java

# Exclude test classes (binaries) from the analysis
sonar.test.exclusions=target/test-classes/**, build/test/classes/**


# --- optional properties ---

# defaults to project key
#sonar.projectName=projectName
# defaults to 'not provided'
#sonar.projectVersion=1.0
 
# Path is relative to the sonar-project.properties file. Defaults to .
#sonar.sources=.
 
# Encoding of the source code. Default is default system encoding
#sonar.sourceEncoding=UTF-8

##########################################

go to the project directory and do cmd and then paste this code and give the path of sonar-scanner directory 
D:\sonar-scanner-5.0.1.3006-windows\bin\sonar-scanner.bat -D"sonar.projectKey=projectName" -Dsonar.java.binaries=**/* -D"sonar.host.url=http://localhost:9003" -D"sonar.login=6a55e1e99973678332932b8d2f6e"
