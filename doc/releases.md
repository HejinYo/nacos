mvn clean install -Dmaven.test.skip=true
mvn clean deploy -P release-sign-artifacts -Dmaven.test.skip=true
