# Sample Wildfly/JBoss Applications

Sample EAR and WAR files for testing.

- kitchensink-angular.war use $URL/kitchensink-angular.
- kitchensink-ear.ear use $URL/kitchensink-ear-web.
- kitchensink-ear-root.ear has the pom.xml/contextRoot to use "/".

## Azure CLI Deployment

1. First update Azure CLI.

```bash

az extension add --name webapp

```

2. Deploy using the following command.

**WAR**

```bash

az webapp deploy --resource-group <rgName> --name <appName> --type war --src-url https://github.com/azureossd/jboss-quickstarts/raw/master/kitchensink-angularjs.war

```

**EAR**

```bash

az webapp deploy --resource-group <rgName> --name <appName> --type ear --src-url https://github.com/azureossd/jboss-quickstarts/raw/master/kitchensink-ear.ear

```

