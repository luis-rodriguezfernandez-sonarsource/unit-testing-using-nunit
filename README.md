```
$ dotnet sonarscanner begin /k:"unit-testing-using-nunit" /d:sonar.token="xxxx" /d:sonar.cs.opencover.reportsPaths="**/**/coverage.opencover.xml" /d:sonar.host.url="https://lurodrig-sonarqube.ngrok.io" /d:sonar.scanner.scanAll="false" /d:sonar.verbose="true"

$ dotnet build --no-incremental

$ dotnet test --collect:"XPlat Code Coverage" -- DataCollectionRunSettings.DataCollectors.DataCollector.Configuration.Format=opencover

$ dotnet sonarscanner end /d:sonar.token="xxxxx"
```
